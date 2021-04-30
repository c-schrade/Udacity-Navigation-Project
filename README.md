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

    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

After downloading the file you have to unzip it. Then follow the instructions on the top of the Jupyter Notebook to instantiate the environment. Note that in the code the visualization of the environment is turned off. Ofcourse this can be changed. 

### Instructions

Follow the instructions in `Navigation.ipynb` to get started with training your own agent!  

### (Optional) Challenge: Learning from Pixels

After you have successfully completed the project, if you're looking for an additional challenge, you have come to the right place!  In the project, your agent learned from information such as its velocity, along with ray-based perception of objects around its forward direction.  A more challenging task would be to learn directly from pixels!

To solve this harder task, you'll need to download a new Unity environment.  This environment is almost identical to the project environment, where the only difference is that the state is an 84 x 84 RGB image, corresponding to the agent's first-person view.  (**Note**: Udacity students should not submit a project with this new environment.)

You need only select the environment that matches your operating system:
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana_Windows_x86_64.zip)

Then, place the file in the `p1_navigation/` folder in the DRLND GitHub repository, and unzip (or decompress) the file.  Next, open `Navigation_Pixels.ipynb` and follow the instructions to learn how to use the Python API to control the agent.

(_For AWS_) If you'd like to train the agent on AWS, you must follow the instructions to [set up X Server](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above.
