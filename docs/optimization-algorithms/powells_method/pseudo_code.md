## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function PowellsMethod(objective_function, initial_solution, directions)
    current_solution = initial_solution
    while not stopping_condition:
        for direction in directions:
            current_solution = line_search(objective_function, current_solution, direction)
        new_directions = update_directions(directions, current_solution)
        directions = new_directions
    return current_solution
```