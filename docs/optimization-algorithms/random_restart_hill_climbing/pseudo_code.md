## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function RandomRestartHillClimbingOptimizer(objective_function, num_restarts)
    best_solution = None
    best_value = -Infinity
    for i = 1 to num_restarts:
        initial_solution = random_solution()
        solution = HillClimbingOptimizer(objective_function, initial_solution)
        value = objective_function(solution)
        if value > best_value:
            best_solution = solution
            best_value = value
    return best_solution
```