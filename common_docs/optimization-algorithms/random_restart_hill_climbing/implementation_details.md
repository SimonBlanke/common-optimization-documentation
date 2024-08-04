## Implementation Details

The random restart hill climbing inherits its behaviour from the regular hill climbing and 
expands it by jumping to a random position during the iteration step if the following criteria is meet:

$$
\text{iter}_i  \mathrm{\%}  \text{n_iter_restart} = 0
$$

