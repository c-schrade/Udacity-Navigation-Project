# Report

This is the detailed report on my implementation of the deep Q-learning algorithm for the Banana-Collector environment. I will just go through part 4 of the [Navigation.ipynb](Navigation.ipynb)-notebook because the learning algorithm is implemented there. Note that in part 4 I mostly adapted the code from the exercise in the Deep Q-networks lesson. Note also that the environment is already instantiated in part 1 of the notebook and referenced by the name "env".

Now to part 4:

First of all (in cell 11) the necessary packages are imported; most importantly torch and several subpackages of torch which will be used to build the neural network later.

In the next cell (with number 12) the QNetwork class is created in which the neural network, that will approximate the action value function Q, is set up. In lines 17-19 (in the __init__-function) one can see the architecture of the network. The input size is 37-dimensional which fits the size of the state vectors that will be the inputs for the network. Then we have two linear hidden layers of size 64 and one linear output layer of size 4 (which is the same as the number of possible actions). The idea here is that for each state input the four output values estimate the action values of the four possible actions in that state.
In the forward-function the forward pass of the neural network is defined. One can see here (lines 25-27) that a relu-activation function is used for the two hidden layers whereas no activation function is applied to the output layer.









![image info](./Pictures/training.png)
![image info](./Pictures/test.png)
