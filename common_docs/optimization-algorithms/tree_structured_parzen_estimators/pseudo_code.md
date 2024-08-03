## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function TreeStructuredParzenEstimators(objective_function, initial_samples, num_iterations)
    samples = initial_samples
    for i in 1 to num_iterations:
        good_samples, bad_samples = split_samples(samples)
        candidate = sample_from_model(good_samples, bad_samples)
        samples.append(candidate)
    return best_sample(samples, objective_function)
```