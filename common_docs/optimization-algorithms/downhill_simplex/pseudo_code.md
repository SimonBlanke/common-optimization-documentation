## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function DownhillSimplexOptimizer(objective_function, initial_simplex)
    simplex = initial_simplex
    while not stopping_condition:
        sort_simplex(simplex, objective_function)
        centroid = compute_centroid(simplex)
        reflected = reflect(centroid, simplex)
        if objective_function(reflected) < objective_function(simplex[0]):
            expanded = expand(centroid, reflected)
            if objective_function(expanded) < objective_function(reflected):
                simplex[-1] = expanded
            else:
                simplex[-1] = reflected
        else:
            if objective_function(reflected) < objective_function(simplex[-2]):
                simplex[-1] = reflected
            else:
                contracted = contract(centroid, simplex)
                if objective_function(contracted) < objective_function(simplex[-1]):
                    simplex[-1] = contracted
                else:
                    shrink(simplex)
    return best_solution_in_simplex(simplex)
```