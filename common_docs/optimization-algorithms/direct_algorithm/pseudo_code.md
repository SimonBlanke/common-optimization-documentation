## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function DirectAlgorithm(objective_function, search_space, num_iterations)
    partitions = [search_space]
    best_solution = None
    best_value = -Infinity
    for i = 1 to num_iterations:
        best_partition = select_best_partition(partitions, objective_function)
        new_partitions = divide_partition(best_partition)
        partitions.remove(best_partition)
        partitions.extend(new_partitions)
        for partition in new_partitions:
            candidate = midpoint(partition)
            value = objective_function(candidate)
            if value > best_value:
                best_solution = candidate
                best_value = value
    return best_solution
```