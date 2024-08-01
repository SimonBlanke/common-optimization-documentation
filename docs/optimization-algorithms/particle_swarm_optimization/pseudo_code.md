## Pseudo Code

!!! abstract inline "Pseudo Code"

```
function ParticleSwarmOptimizer(objective_function, swarm_size, num_iterations)
    swarm = initialize_swarm(swarm_size)
    global_best = None
    global_best_value = -Infinity
    for i = 1 to num_iterations:
        for particle in swarm:
            particle.update_velocity(global_best)
            particle.update_position()
            value = objective_function(particle.position)
            if value > particle.best_value:
                particle.best_position = particle.position
                particle.best_value = value
            if value > global_best_value:
                global_best = particle.position
                global_best_value = value
    return global_best
```