## Implementation Details

The forest-optimizer shares most of its code base with the bayesian-optimizer. Only its model to 
calculate the expected score $\mu$ and its standard deviation $\sigma$ is different. Tree based models do not 
calculate the standard deviation by them self. A modification is necessary to determine the
standard deviation from the impurity of the trees in the ensemble. This modification is taken from the paper *"Algorithm Runtime Prediction: Methods & Evaluation"* chapter *4.3.3*.

