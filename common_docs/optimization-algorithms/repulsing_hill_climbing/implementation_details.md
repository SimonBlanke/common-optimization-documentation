## Implementation Details

Similar to other hill climbing based algorithms the **repulsing hill climbing**
inherits the methods from the regular hill climbing and adds a functionality to
escape local optima. The repulsing hill climbing temporally increases `epsilon`
by multiplying it with the `repulsion_factor` for the next iteration. 

$$
\sigma = \text{dim-size} * \epsilon * \text{repulsion_factor}
$$


This way the algorithm *jumps* away from the current position to explore other regions of the search-space. So the repulsing hill climbing is different from stochastic hill climbing and simulated annealing in that it **always** activates its methods to espace local optima instead of activating them with a certain **probability**.


