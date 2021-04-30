[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Udacity-Navigation-Project

The Jupyter-Notebook-File [Navigation.ipynb](Navigation.ipynb) includes my solution to the Navigation-Project in the Deep-Reinforcement-Learning-Nanodegree.

### Introduction

In this project I trained an agent to navigate in a square world (with yellow and blue bananas in it) and collect as many yellow bananas as possible while avoiding the blue ones. The training is done by adapting the deep Q-learning algorithm from the Nature article ["Human-level control through deep reinforcement learning"](https://web.stanford.edu/class/psych209/Readings/MnihEtAlHassibis15NatureControlDeepRL.pdf) to this "Banana-Environment".

![Trained Agent][image1]

### Description of the Environment

The agent gets a reward of +1 for collecting a yellow banana and a reward of -1 for collecting a blue banana.  Since the goal is to get maximal cumulative reward per episode, the agent therefore gets trained to collect as many yellow and as few blue bananas as possible.

The state space is 37-dimensional, while the action space is discrete and consists of the integers from 0 to 3 (inclusive), where "0" corresponds to moving forward, "1" to moving backward, "2" to turning left and "3" to turning right.

The task is episodic (every episodes lasts for at most 300 timesteps).
The environment is said to be solved if the agent has an average score of at least +13 over 100 consecutive epsidodes.

### Installation

If you want to use the [Navigation.ipynb](Navigation.ipynb)-notebook to train an agent on your own you first have to download several packages and the environment. 

To install all the necessary packages and dependencies you can set up a new python environment as explained in the README.md in the [DRLND Github repository](https://github.com/udacity/deep-reinforcement-learning#dependencies).
Depending on your operating system you can download the environment using one of the following links:

 * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
 * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
 * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
 * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

After downloading the file you have to unzip it. Then follow the instructions in the first part of the Jupyter Notebook to instantiate the environment. Note that in the code the visualization of the environment is turned off. Ofcourse this can be changed. 

### Instructions on [Navigation.ipynb](Navigation.ipynb)-notebook

After you instantiated the environment in the first part you can examine the state and action space in the second part. In the third part you can check how a random agent performs in the environment.

By running the cells in the fourth part you can train an agent on the environment and test the intelligent agent afterwards. 
After defining the necessary classes and functions one first sets up the agent by creating an instance of the Agent-class. Then (by running the dqn()-function) the deep Q-learning algorithm is carried out with this agent. 

The agent stops learning after the goal of an average total reward of +13 over 100 consecutive is reached. You can then plot the improving performance of your agent that was achieved during training.

At the end of the notebook you can then test your trained agent on 100 episodes and check his performance by looking at the score-plot and the averahe score it got in these 100 last episodes.




