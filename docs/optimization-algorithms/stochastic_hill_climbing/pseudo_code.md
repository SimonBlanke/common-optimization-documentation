## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function StochasticHillClimbingOptimizer(objective_function, initial_solution)
    current_solution = initial_solution
    while not stopping_condition:
        neighbor = get_random_neighbor(current_solution)
        if objective_function(neighbor) > objective_function(current_solution):
            current_solution = neighbor
    return current_solution
```