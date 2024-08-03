## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function RandomSearchOptimizer(objective_function, search_space, num_iterations)
    best_solution = None
    best_value = -Infinity
    for i = 1 to num_iterations:
        candidate = random_solution(search_space)
        value = objective_function(candidate)
        if value > best_value:
            best_solution = candidate
            best_value = value
    return best_solution
```