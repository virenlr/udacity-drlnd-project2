# udacity-drlnd-project2
This is the second project done as part of Udacity's Deep Reinforcement Learning Nanodegree.

## Project Details

This project uses the Reacher environment in Unity's ML toolkit.

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The GIF below was taken directly from Udacity's project page.

![Project Demo](https://raw.githubusercontent.com/virenlr/udacity-drlnd-project2/main/Demo.gif "Project Demo")

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically, after each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores. This yields an average score for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. 

## Getting Started

#### Step 1: Clone my repository

You will need the Report.ipynb file, as well as the Python files titled `ddpg_agent.py` and `model.py`. Please ensure these are all placed in the same folder.

#### Step 2: Setup the required dependencies

1. Create (and activate) a new environment with Python 3.6.

Linux or Mac:

```
conda create --name drlnd python=3.6
source activate drlnd
```

Windows:

```
conda create --name drlnd python=3.6 
activate drlnd
```

2. Perform a minimal installation of OpenAI Gym

```
pip install gym
```

3. Clone the repository from [Udacity's GitHub page](https://github.com/udacity/deep-reinforcement-learning), and navigate to the python/ folder. Then, install several dependencies.

```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create an IPython kernel for the `drlnd` environment.

```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. You may have to install other dependencies with pip, like Unity ML and PyTorch. You will know when you start executing the cells in my notebook.

6. Before running the code in the notebook, change the kernel to match the drlnd environment by using the drop-down Kernel menu.

#### Step 3: Download the environment

Download the Unity environment corresponding to your operating system with the links provided by Udacity.

Linux: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
Mac OSX: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
Windows 32-bit: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
Windows 64-bit: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Then, place the file in the same folder as the other files you downloaded from my repo and unzip (or decompress) it.

## Instructions

With the environment set up, you can simply open and execute the cells of the Jupyter notebook, one by one. Feel free to take a look at the code in `ddpg_agent.py` and `model.py` as well.
