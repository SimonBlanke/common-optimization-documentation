## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function HillClimbingOptimizer(objective_function, initial_solution)
    current_solution = initial_solution
    while not stopping_condition:
        neighbor = get_best_neighbor(current_solution)
        if objective_function(neighbor) > objective_function(current_solution):
            current_solution = neighbor
        else:
            break
    return current_solution
```