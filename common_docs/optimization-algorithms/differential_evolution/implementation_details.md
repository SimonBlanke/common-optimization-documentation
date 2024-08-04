## Implementation Details

The differential evolution optimizer inherits from the evolutionary algorithm class. Therefore it is similar to the genetic algorithm or evolution strategy, like using a crossover step to mix individuals in the population by e.g. discrete recombination. But it sets itself apart in the iteration loop by always doing a mutation step and crossover step to mix the target- and mutant-vector.
