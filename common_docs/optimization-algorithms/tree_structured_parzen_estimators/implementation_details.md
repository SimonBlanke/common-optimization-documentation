## Implementation Details

Similar to other sequence-model-based optimization algorithms the positions and scores 
of previous evaluations are saved as features and targets to train a machine learning algorithm.
For the tree structured parzen estimators we use two separate kernel density estimators one receiving the best positions, while the other gets the worst positions to calculate the acquisition function. 

The separation of the position into best and worst is very simple. First we sort the positions by their scores. We split this list at the following index:

$$
i_{split} = \max( n_{samples} \gamma, 1)
$$

where:

- $\gamma$ **=>** `gamma_tpe`
- $n_{samples}$ **=>** the number of positions in the list

