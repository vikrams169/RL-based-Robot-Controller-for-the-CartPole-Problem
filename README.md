# RL-based-Robot-Controller-for-the-CartPole-Problem
A set of reinforcement learning techniques used to design controllers to run and evaluate the simulation of the CartPole Problem on Webots
<br>
<br>
The Cart Pole environment can be better explained or reviwed by going through the priginal souce code by Open AI Gym <a href="https://github.com/openai/gym/blob/master/gym/envs/classic_control/cartpole.py">here</a>.
<br><br>
In this environment, there exists a pole on a mobile system (with minimal friction), and the goal is to keep it moving without collapsing for as long as possible. The reward for standing each timestep is +1, and if the pole moves more than 15 degrees from the vertical, the episode ends (so basically no negative rewards). There are only two possible actions that are moving the point on the pole on the mobile system right or left, every timestep.
<br><br>
This environment has been solved with the objective of reaching maximum reward (thus reaching the final goal), and has been done so, by using three deep reinforcement learning techniques (all use a neural network function approximator having same architecture, mapping form state to action/policy), each trained on 1,000 episodes.
<br><br>
The programs here are developed with the intent of being run in the <b>Webots</b> Simulator. More information about Webots can be found <a href="https://cyberbotics.com/">here</a>. To use RL algorithms in the CartPole environment, I have used the <b>Deepbots</b> framework, more about which can be found <a href="https://github.com/aidudezzz/deepbots">here</a>. The robot and the CartPole Environment have been implemented as given in the Deepbots <a href="https://github.com/aidudezzz/deepbots-tutorials/blob/master/robotSupervisorSchemeTutorial/README.md">tutorial</a>. All controller algorithms (Deep Q-Learning, Reinforce, and Advantage Actor-Critic (A2C)) have been implemented originally and from scratch.
<br><br>
To navigate and view the controller codes, navigate to the CartPole/controllers directory and go into the directory of the relevant controller. The CartPole/worlds directory has the robot design as given by the Deepbots framework.
<br><br>
To run the controllers and view the simulation, you would need installations of Webots, Deepbots, Python 3, and Tensorflow. The versions I ran and tested them on (which work) are:
<ul><li> Webots R2022a
<li>Deepbots 0.1.3 (currently the dev version)
<li>Python 3.1.0
<li>Tensorflow 2.3.1</ul>
A training simulation GIF of the configuration looks like:


https://user-images.githubusercontent.com/56220919/179799841-af8dd013-4517-4718-838c-e15d05728022.mp4




Three RL algorithms have been implemented and tested. They (in the order of their effectiveness based on visual simulation results and cumulative reward) are:
<ul><li> Advantage Actor-Critic (A2C)
<li>Deep Q-Learning
<li>Reinforce Policy Gradient</ul>
