# Deep Convolutional Q-Learning for Pac-Man

![](https://github.com/anandkaranubc/deep_convolutional_q/blob/main/pacman.gif)


Welcome to the Deep Convolutional Q-Learning for Pac-Man project! This project aims to develop an intelligent Pac-Man player using deep reinforcement learning techniques. The goal is to enable Pac-Man to learn optimal strategies for navigating the maze, avoiding ghosts, and maximizing its score by eating pellets and power-ups.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithm](#algorithm)
- [Project Structure](#project-structure)
- [Results](#results)

## Introduction
This project uses Deep Convolutional Q-Learning (DQN) to train an AI agent to play Pac-Man. The DQN algorithm combines Q-learning with deep neural networks to approximate the Q-values, which represent the expected future rewards of taking certain actions in given states. By using convolutional layers, the model can efficiently process the visual input from the game environment.

## Installation
To run this project, you'll need Python and several dependencies. Follow the steps below to set up your environment:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/deep-convolutional-q-learning-for-pac-man.git
    cd deep-convolutional-q-learning-for-pac-man
    ```

2. Create and activate a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
To train the Pac-Man agent, run the following command:
```bash
python deep_convolutional_q_learning_for_pac_man.py
```
This will start the training process, where the agent interacts with the Pac-Man environment and learns over time. The training parameters, such as the number of episodes, learning rate, and discount factor, can be adjusted in the script.

## Algorithm
The DQN algorithm works as follows:
1. **Initialization**: Initialize the replay memory and the Q-network with random weights.
2. **Experience Replay**: Store the agent's experiences (state, action, reward, next state) in the replay memory.
3. **Mini-Batch Training**: Randomly sample a mini-batch of experiences from the replay memory and use them to train the Q-network.
4. **Target Network**: Periodically update a separate target network to stabilize training.
5. **Action Selection**: Use an epsilon-greedy policy to balance exploration and exploitation.

The convolutional layers in the Q-network process the game frames to extract useful features, which are then used to predict the Q-values for each possible action.

## Project Structure
```
deep-convolutional-q-learning-for-pac-man/
├── assets/
│   └── ... (game assets and sprites)
├── models/
│   └── dqn_model.py (Q-network definition)
├── utils/
│   └── replay_memory.py (Experience replay memory implementation)
├── deep_convolutional_q_learning_for_pac_man.py (Main script)
├── requirements.txt (Dependency list)
└── README.md (Project documentation)
```

## Results
After training for a sufficient number of episodes, the agent should be able to play Pac-Man with improved strategies. The performance of the agent can be evaluated based on its average score, survival time, and ability to avoid ghosts while collecting pellets.
