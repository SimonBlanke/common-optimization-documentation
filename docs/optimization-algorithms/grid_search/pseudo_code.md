## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function GridSearchOptimizer(objective_function, parameter_grid)
    best_solution = None
    best_value = -Infinity
    for each combination in parameter_grid:
        value = objective_function(combination)
        if value > best_value:
            best_solution = combination
            best_value = value
    return best_solution
```