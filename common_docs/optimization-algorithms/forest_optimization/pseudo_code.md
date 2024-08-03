## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function ForestOptimizer(objective_function, initial_samples, num_iterations)
    samples = initial_samples
    for i in 1 to num_iterations:
        model = fit_forest_model(samples, objective_function)
        candidate = predict_best_candidate(model)
        samples.append(candidate)
    return best_sample(samples, objective_function)
```