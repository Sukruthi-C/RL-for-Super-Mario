
# RL-for-Super-Mario
## Description
This project demonstrates the application of reinforcement learning (RL) to play the Super Mario Bros game using the Proximal Policy Optimization (PPO) algorithm. The game environment undergoes pre-processing steps to prepare the state inputs for the RL agent. 

<p float="left">
  <img src="videos/mario1.gif" alt="Alt text for GIF 1" width="48%"/>
  <img src="videos/mario2.gif" alt="Alt text for GIF 2" width="48%"/>
</p>


### Pre-processing Steps
1. **Grayscale Conversion**: The original game images are converted to grayscale, which reduces the computational load by simplifying the input data. This is crucial for enhancing the performance of the learning algorithm.
   
 <p align="center">
  <img src="videos/grayscale.png" alt="Grayscale Example" width="20%"/>
</p>


2. **Frame Stacking**: Multiple consecutive frames are stacked together. This technique provides a temporal dimension to the inputs, allowing the agent to understand and predict the trajectory and velocity of Mario and his enemies.

   ![Frame Stacking Example](videos/stacking.png)

These preprocessing techniques are essential for efficient training of the RL agent, enabling it to perform better by understanding the dynamics of the game environment.

### Instructions
1. Clone the repository. 

```
git clone git@github.com:Sukruthi-C/RL-for-Super-Mario.git
```
2. Install the pre-requisities.
```
cd RL-for-Super-Mario
```
3. Install dependencies
```
pip install gym_super_mario_bros
pip install stable-baselines3[extra]
pip install matplotlib
pip install pytorch
```
5. Run all code the blocks on jupyter notebook

### Results
The model was trained for 1000000 iterations with a learning rate of 1e-7 with cnn policy and 2000000 iterations with a learning rate of 1e-6 with a mlp policy, batch size of 64 and number of steps of 512. The one with the lower learning rate performed better. However, the model needs to be trained more than this to perform better. As you can see in the gifs attached above that Mario cannot pass the first level with this. Due to GPU limitations, this remains a work for the future.
