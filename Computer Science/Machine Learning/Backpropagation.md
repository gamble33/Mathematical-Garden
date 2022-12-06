#CompSci

# Backpropagation
---
## Introduction
Consider a very simple [[Artificial Neural Network|neural network]]
![[very_simple_neural_network.png#invert_W|500]]
that is determined by three [[Weight|weights]] and three [[Bias|biases]].
![[neural_net_weights_biases.png#invert_W|500]]
Therefore, the [[Cost Function|cost function]], $C(w_1, b_1, w_2, b_2, w_3, b_3)$, is determined by these weights and biases. We want to determine how sensitive each of these [[Variable|variables]] are to the cost function. Doing so will tell us which adjustments will cause the greatest decrease in the cost function.