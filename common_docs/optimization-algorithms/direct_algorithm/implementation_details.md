## Implementation Details

The DIRECT algorithm calculates the upper-bound based on the distance between the center position of the subspace and the furthest position:

$$
U = score_{c} + k \cdot || x_c-x_{furthest} ||_2
$$

where:

- $score_{c}$ **=>** score of center position
- $k$ **=>** is the slope parameter (hard-coded to 1 in v1.2)
- $|| x_c-x_{furthest} ||_2$ **=>** distance between the center position of the subspace and the furthest position from the center

Compared to other smbo the DIRECT algorithm does not need to do calculations based on all positions in the search-space but only a small subset. This makes this algorithm less computationally expensive, than bayesian- or lipschitz-optimization.