## Implementation Details

The spiral optimization is very similar to the particle swarm optimization algorithm. Both algorithms are population based and imitate physics based movement by calculating n-dimensional vectors. The spiral optimization calculates the new position in the search space with the following equation:

$$
x_i (k+1) = x^* (k) r(k) R(\theta) (x_i(k)- x^*(k))
$$

where:

- k **=>** nth iteration
- r **=>** `decay_rate`
- R **=>** rotation matrix
- $x_i$ **=>** current position
- $x^*$ **=>** center position (known best position of all particles)




The rotation matrix used for n-dimensional optimization problems is defined as:

$$
R(\theta) = \left[ \begin{matrix}
0^{\top}_{n-1} & -1 \\
I_{n-1} & 0_{n-1}
\end{matrix} \right]
$$

