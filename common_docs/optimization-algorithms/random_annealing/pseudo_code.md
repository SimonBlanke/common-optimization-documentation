## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function RandomAnnealingOptimizer(objective_function, initial_solution, initial_temperature, cooling_rate)
    current_solution = initial_solution
    temperature = initial_temperature
    while temperature > minimum_temperature:
        candidate = random_solution_near(current_solution)
        delta = objective_function(candidate) - objective_function(current_solution)
        if delta > 0 or random() < exp(delta / temperature):
            current_solution = candidate
        temperature *= cooling_rate
    return current_solution
```