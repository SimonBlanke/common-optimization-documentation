## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function GeneticAlgorithmOptimizer(objective_function, population_size, num_generations, mutation_rate)
    population = initialize_population(population_size)
    for generation in 1 to num_generations:
        evaluate_fitness(population, objective_function)
        new_population = []
        while len(new_population) < population_size:
            parent1, parent2 = select_parents(population)
            offspring = crossover(parent1, parent2)
            if random() < mutation_rate:
                mutate(offspring)
            new_population.append(offspring)
        population = new_population
    return best_individual(population, objective_function)
```