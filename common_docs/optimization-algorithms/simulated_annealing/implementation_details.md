## Implementation Details

The **simulated annealing** algorithm inherits the methods to get new positions from hill-climbing and the methods to accept the new position from stochastic-hill-climbing.
Similar to stochastic hill climbing it may accept a worse position with the goal of
escaping a local optimum. The `start_temp` is a factor for the probability of accepting 
a worse position. 


$$
p = \exp^{-\frac{\text{score}_{normalized}}{\text{temp}}}
$$

This probability decreases over time, because of the `annealing_rate` decreasing the `start_temp` over time.

$$
\text{start_temp} \leftarrow  \text{start_temp} * \text{annealing_rate}
$$
