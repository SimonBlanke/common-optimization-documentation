## Implementation Details

The **stochastic hill climbing** inherits the behaviour of the regular hill climbing algorithm and
adds its additional functionality after the evaluation of the score is done. 
If the new score is not better than the previous one the algorithm starts the following calculation:

$$
\text{score}_{normalized} = \text{norm} * \frac{\text{score}_{current} - \text{score}_{new}}{\text{score}_{current} + \text{score}_{new}}
$$

$$
p = \exp^{-\text{score}_{normalized}}
$$

If $p$ is smaller than a random number between 0 and `p_accept` the new position gets accepted anyways.

