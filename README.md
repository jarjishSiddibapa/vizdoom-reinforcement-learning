# VizDoom Reinforcement Learning Agent

This repository contains the code and resources for my final year project in **Computer Engineering** at **A. P. Shah Institute of Technology**. The project involves training a **Reinforcement Learning (RL)** agent in a 3D environment using the **VizDoom** engine. The agent is trained using the **PPO (Proximal Policy Optimization)** algorithm and will be further tested using other algorithms such as **DQN, A3C,** and **DDPG**.

## Project Overview

The goal of the project is to create an RL agent that can complete various levels in the VizDoom environment. The agent is currently trained on three levels:

1. **BASIC**: A simple environment designed to test fundamental AI functionality.
    - **Scenario**: The agent can only move left/right and shoot. It needs to kill a monster spawned on the opposite side of the map.
    - **Training Steps**: 60,000
    - **Notebook**: [`basic-doom.ipynb`](basic-doom.ipynb)

2. **DEFEND THE CENTER**: A survival scenario where the agent must fend off respawning monsters.
    - **Scenario**: The agent stands in the center of a circular map and must shoot monsters as they approach. Limited ammo adds complexity.
    - **Training Steps**: 100,000
    - **Notebook**: [`defend-the-center-doom.ipynb`](defend-the-center-doom.ipynb)

3. **DEADLY CORRIDOR**: A challenging scenario where the agent must navigate a monster-filled corridor while moving toward a vest.
    - **Scenario**: Monsters attack from the sides, and the agent must avoid dying while getting closer to the vest.
    - **Training Steps**: 400,000
    - **Notebook**: [`deadly-corridor-doom.ipynb`](deadly-corridor-doom.ipynb)

## Algorithms Implemented

- **PPO (Proximal Policy Optimization)**: Currently used for training the agent across all three levels.
  
  Future plans include:
  - **DQN (Deep Q-Networks)**
  - **A3C (Advantage Actor-Critic)**
  - **DDPG (Deep Deterministic Policy Gradient)**

## Installation

To run and train the agent on your machine, follow these steps:

### Prerequisites

- Python 3.8+
- Conda or Miniconda
- Jupyter Notebook

### Setup Steps

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/vizdoom-rl-agent.git
    cd vizdoom-rl-agent
    ```

2. **Create and Activate the Environment**:
    Use the `environment.yaml` file to create the necessary environment:
    ```bash
    conda env create -f environment.yaml
    conda activate vizdoom-rl
    ```

3. **Run Jupyter Notebook**:
    To train the agent and visualize performance:
    ```bash
    jupyter notebook
    ```
    Open any of the provided `.ipynb` files (e.g., `basic-doom.ipynb`) to see training progress or start new training.

## Repo Structure

- **`basic-doom.ipynb`**: Jupyter Notebook for training on the BASIC level.
- **`deadly-corridor-doom.ipynb`**: Jupyter Notebook for training on the DEADLY CORRIDOR level.
- **`defend-the-center-doom.ipynb`**: Jupyter Notebook for training on the DEFEND THE CENTER level.
- **`environment.yaml`**: Conda environment file containing all the necessary libraries to run and train the agent.
- **`.gitignore`**: Standard Git ignore file.

## Performance Visualization

Each Jupyter notebook contains visualizations of the agent’s performance, including:
- Rewards vs. Timesteps
- Survival Time vs. Episodes
- Actions taken by the agent over time

These visualizations help in understanding how the agent is learning and adapting to the environment over time.

## Future Work

- Implement and compare results of other RL algorithms: **DQN**, **A3C**, and **DDPG**.
- Experiment with additional VizDoom scenarios.
- Optimize agent performance and reduce training time by tuning hyperparameters.

## Contributions

Feel free to fork the repo and submit pull requests if you'd like to contribute to this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
