## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function PatternSearch(objective_function, initial_solution, step_size)
    current_solution = initial_solution
    while not stopping_condition:
        for direction in directions:
            candidate = current_solution + step_size * direction
            if objective_function(candidate) > objective_function(current_solution):
                current_solution = candidate
            else:
                step_size /= 2
    return current_solution
```