## Implementation Details

Similar to the downhill simplex algorithm the pattern search has a list of positions and their scores to form the pattern. As the pattern moves through the search space this information gets updated.

At first all positions that form the cross are evaluated. After that the center of the cross moves
to the best position. This leads to new positions inside the cross that have not been
evaluated, yet. So the algorithm restarts evaluating all of the positions in the cross. If non of the positions have a better score than the center position the cross shrinks by the `reduction`-factor creating new positions inside the cross.

The pattern-search can be seen as a special case of the hill-climbing algorithm. The pattern-search will also try to move locally through the search-space by evaluating positions within its neighbourhood (the cross-shape), but it does so by choosing positions that each extend into different dimensions and equal distance to the center. The hill-climbing algorithm chooses the neighbour positions more randomly.
