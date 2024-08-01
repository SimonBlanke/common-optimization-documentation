## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function DifferentialEvolutionOptimizer(objective_function, population_size, num_generations, crossover_rate, differential_weight)
    population = initialize_population(population_size)
    for generation in 1 to num_generations:
        for i in range(population_size):
            a, b, c = select_three_random_individuals(population, i)
            mutant_vector = a + differential_weight * (b - c)
            trial_vector = crossover(population[i], mutant_vector, crossover_rate)
            if objective_function(trial_vector) > objective_function(population[i]):
                population[i] = trial_vector
    return best_individual(population, objective_function)
```