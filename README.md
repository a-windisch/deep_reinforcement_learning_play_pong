# Deep Reinforcement Learning - Playing Pong

---

[Andreas Windisch, Feb. 2019](https://www.linkedin.com/in/andreas-windisch-physics/)

This notebook contains the documentation for a project that is part of the [Udacity's Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893). The code presented here is mostly the one used in the exercise, with slight alterations and comments. In case you have any questions or comments, or simply want to contact me, use the link to my LinkedIn profile above, or write me directly using [andreas.windisch@yahoo.com](andreas.windisch@yahoo.com). Have fun exploring this nice project! :-)

Below, we will implement and train a policy to play atari-pong, using only the pixels as input. We will use convolutional neural nets and pytorch to implement and train our policy.

### 0. Synopsis

In this project, we will train an Agent to play the Atari game pong using Proximal Policy Optimization (PPO). The environment is provided by OpenAI. The Agent percieves the world through pixels, and we will use a Convolutional Neural Network for training the Agent. The code in this repo should be self-contained, apart from a few dependencies that are installed dynamically using pip.   

#### Action Space
The Agent can choose from six different actions:
- NOOP
- FIRE
- LEFT
- RIGHT
- LEFTFIRE
- RIGHTFIRE

However, it is sufficient to train the Agent using only the actions LEFTFIRE and RIGHTFIRE. 

#### Observation Space
The size of the observation space determined by two temproally adjacent, cropped, downscaaled 80x80 greyscale screenshots of the game screen.

#### Rewards
The reward is given by the game score.


### 1. Files in this repository

* README.md - This file
* pong-PPO.ipynb - A Jupyter Notebook containing the main code for training the Agent 
* pong_utils.py - Utilities for this project
* parallelEnv.py - Environment definitions
* PPO.policy - The saved status of the network


### 2. Running the code
The code is this repository requires numpy, PyTorch, OpenAI and Jupyter. Make sure that those are installed, some of the dependencies are installed directly using pip. Then, just open the Notebook 'pong-PPO.ipynb'. Follow the instructions within the notebook to train the Agent.
