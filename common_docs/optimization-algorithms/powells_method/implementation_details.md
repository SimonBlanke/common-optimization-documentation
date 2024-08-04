## Implementation Details

The powell's method implemented in Gradient-Free-Optimizers does only see one dimension at a time.
This differs from the original idea of creating (and searching through) 
one search-vector at a time, that spans through multiple dimensions.
After `iters_p_dim` iterations the next dimension is searched, while the 
search space range from the previously searched dimension is set to the best position,
This way the algorithm finds new best positions one dimension at a time.

