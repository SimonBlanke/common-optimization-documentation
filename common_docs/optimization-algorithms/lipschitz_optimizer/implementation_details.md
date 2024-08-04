## Implementation Details

The lipschitz optimization is very similar to sequence-model-based optimizers. The upper bound is an acquisition function that is calculated for every position in the search space with the following equation:

$$
U(x) = \min_{i=1...t}(f(x_i) + k \cdot || x-x_i ||_2)
$$

where:

- $f(x_i)$ **=>** is the score of a known position
- $k$ **=>** is the maximum slope between known positions
- $|| x-x_i ||_2$ **=>** is the distance between a known position $x_i$ and a position in the search space $x$
- $\min_{i=1...t}$ **=>** returns the minimum value of the calculations for the known positions $i=1...t$

The equation above results in an upper bound that looks like the known positions in the search space are connected with pyramid shaped lines, where the peaks are between the known positions. 
