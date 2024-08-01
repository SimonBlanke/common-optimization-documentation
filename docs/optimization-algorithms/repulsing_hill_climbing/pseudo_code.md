## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function RepulsingHillClimbingOptimizer(objective_function, initial_solution)
    current_solution = initial_solution
    visited = set()
    while not stopping_condition:
        neighbor = get_best_neighbor(current_solution)
        if objective_function(neighbor) > objective_function(current_solution):
            current_solution = neighbor
            visited.add(current_solution)
        else:
            current_solution = get_random_solution(visited)
    return current_solution
```