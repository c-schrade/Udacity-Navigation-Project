# Report

This is the detailed report on my implementation of the deep Q-learning algorithm for the Banana-Collector environment. I will just go through part 4 of the [Navigation.ipynb](Navigation.ipynb)-notebook because the learning algorithm is implemented there. Note that in part 4 I mostly adapted the code from the exercise in the Deep Q-networks lesson. Note also that the environment is already instantiated in part 1 of the notebook and referenced by the name "env".

Now to part 4:

First of all (in cell 11) the necessary packages are imported; most importantly torch and several subpackages of torch which will be used to build the neural network later.

In the next cell (with number 12) the QNetwork class is created in which the neural network, that will approximate the action value function Q, is set up. In lines 17-19 (in the \_\_init\_\_-function) one can see the architecture of the network. The input size is 37-dimensional which fits the size of the state vectors that will be the inputs for the network. Then we have two linear hidden layers of size 64 and one linear output layer of size 4 (which is the same as the number of possible actions). The idea here is that for each state input the four output values will estimate the action values of the four possible actions in that state.
In the forward-function the forward pass of the neural network is defined. One can see here (lines 25-27) that a relu-activation function is used for the two hidden layers whereas no activation function is applied to the output layer.

In cell 13 the Agent and ReplayBuffer classes are created. But first some of the hyperparameters are already fixed here, namely:

* BUFFER_SIZE = 100000    (number of stored experiences for the experience replay)
* BATCH_SIZE = 64         (batchsize of the batches that will be taken from the stored experiences during learning)
* GAMMA = 0.99            (discount rate)
* TAU = 0.001             (we will update the weights of the target network softly with factor TAU)
* LR = 0.0005             (learning rate)
* UPDATE_EVERY = 4        (the weights of target network will onlybe updated every 4 steps)

Then it is checked if a GPU is available and the device is set to GPU if that's the case; otherwise we will continue with CPU.
In the Agent class (lines 10-110) there are 5 functions:
In the \_\_init\_\_-function two neural networks are instantiated (respectively will get instantiated when an instance of type Agent gets created); one that will be updated in every timestep (that is the qnetwork_local), one that will be updated only all 4 steps and will serve as an approximation to the target function (that is the network qnetwork_target) and the optimizer for the backward propagation step is set to "Adam" (see lines 27-29). Furthermore the experience replay memory is initialized by creating a ReplayBuffer object (line 32).









![image info](./Pictures/training.png)
![image info](./Pictures/test.png)
