## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function BayesianOptimizer(objective_function, initial_samples, num_iterations, acquisition_function)
    samples = initial_samples
    surrogate_model = fit_surrogate_model(samples, objective_function)
    for i in 1 to num_iterations:
        candidate = acquisition_function(surrogate_model)
        samples.append(candidate)
        surrogate_model = fit_surrogate_model(samples, objective_function)
    return best_sample(samples, objective_function)
```