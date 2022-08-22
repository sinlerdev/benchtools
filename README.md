# benchtools
benchtools are intended to be a powerful module that let's you precisely calculate your functions speed. Currently, it lacks some features other plugins offer like profiler, however, I am planning to add them.

## use benchtools
**keep in mind that all numerical results from this module are in microseconds**

To benchmark a function, consider using `benchtools.benchmark", a function that accepts an amount of calls, a function to measure, and the parmaters for that function. This function returns two tables, the first containing the time taken for each call, and the latter containing a helpful amount of metrics.

```lua
local measuredTable, metrixTable = benchtools.benchmark(1000, function(t) 
  print(t)
end, "hi")
```

To compare two functions, consider using `benchtools.compare`, a function that takes an amount of calls, and two functions to measure, with the paramters for those functions. This function returns a metric table specifcing which one is faster

```lua
local result = benchtools.compare(1000, fn1, fn2, paramaters)
```
