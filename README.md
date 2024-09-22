# Reinforcement-Learning
---
# 10-Armed Bandit Simulations

This repository contains Python implementations of the 10-armed bandit problem, focusing on reinforcement learning concepts such as optimistic initial values and epsilon-greedy action selection. The code is modular, implements good coding practices, and leverages parallel processing for computational efficiency.

## Table of Contents

- [Introduction](#introduction)
- [Files](#files)
- [Requirements](#requirements)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [License](#license)

## Introduction

The 10-armed bandit problem is a classic reinforcement learning problem where an agent must learn to select the optimal action from multiple possible actions (arms) based on rewards. This repository includes two Python scripts:

1. **Optimistic Initial Values Simulation**: Demonstrates the effect of optimistic initial action-value estimates on exploration and performance.
2. **Epsilon-Greedy Agents Simulation**: Implements epsilon-greedy agents with different exploration rates and compares their performance in terms of rewards and optimal action selection.

Both simulations use parallel processing to run multiple independent trials efficiently, and they provide visualizations of the results.

## Files

### 1. `optimistic_initial_values.py`

#### Description:

This script simulates the effect of optimistic initial values on the 10-armed bandit problem, comparing two methods:
- **Optimistic Greedy (Q₁=5, ε=0)**: The agent starts with an optimistic estimate of the action values (Q₁=5), encouraging exploration.
- **Realistic ε-Greedy (Q₁=0, ε=0.1)**: The agent starts with a realistic estimate of zero for the action values, combined with an exploration strategy (ε=0.1).

#### Features:
- Uses a constant step-size parameter (α=0.1) to update action-value estimates.
- Implements parallel processing to simulate multiple runs, improving computational efficiency.
- Visualizes the percentage of optimal action selections over time for both methods.

#### Code Overview:
- **Bandit Class**: Represents the environment, where each arm has a randomly assigned true value.
- **Agent Class**: Implements an agent that uses either the optimistic or epsilon-greedy strategy.
- **Simulation**: Runs multiple independent trials in parallel to compute the percentage of optimal actions selected by the agents.
- **Plotting**: Generates line plots comparing the performance of both methods over time.

### 2. `epsilon_greedy_bandit.py`

#### Description:

This script compares the performance of epsilon-greedy agents with different exploration rates (ε=0, 0.01, 0.1) in the 10-armed bandit problem. The agents are evaluated based on:
- Average rewards obtained over time.
- Percentage of times the optimal action is selected.

#### Features:
- Supports parallel execution of multiple simulation runs for improved performance.
- Visualizes the average reward and percentage of optimal action selection for each epsilon value over time.
- Implements good coding practices, such as modularity and detailed docstrings.

#### Code Overview:
- **TenArmedBandit Class**: Represents the multi-armed bandit environment.
- **EpsilonGreedyAgent Class**: Implements an agent that uses an epsilon-greedy strategy to balance exploration and exploitation.
- **Single Run Simulation**: Simulates multiple agents with different epsilon values interacting with the bandit, and records rewards and optimal action selections.
- **Parallel Processing**: Runs multiple independent trials using `joblib.Parallel` for efficiency.
- **Plotting**: Displays two plots:
  - Average reward vs. time steps.
  - Percentage of optimal actions selected vs. time steps.

## Requirements

To run these simulations, you need the following Python libraries:

- `numpy`
- `matplotlib`
- `joblib`

You can install the required dependencies using `pip`:

```bash
pip install numpy matplotlib joblib
```

## Usage

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/10-armed-bandit-simulations.git
cd 10-armed-bandit-simulations
```

2. **Run the Optimistic Initial Values Simulation**:

```bash
python optimistic_initial_values.py
```

This will run the optimistic greedy and realistic epsilon-greedy simulations and plot the percentage of optimal action selections over time.

3. **Run the Epsilon-Greedy Agents Simulation**:

```bash
python epsilon_greedy_bandit.py
```

This will compare agents with different epsilon values, plotting both the average rewards and the percentage of optimal action selections over time.

## Visualizations

### Optimistic Initial Values Simulation:

- **Optimistic Greedy vs. Realistic ε-Greedy**:
  - A plot showing how the optimistic initial values affect exploration and the eventual percentage of optimal action selections.

### Epsilon-Greedy Agents Simulation:

- **Average Reward vs. Steps**:
  - A plot comparing the average rewards obtained by agents using different epsilon values over time.
  
- **Optimal Action Percentage vs. Steps**:
  - A plot comparing how often agents with different epsilon values select the optimal action over time.

## License

This repository is licensed under the MIT License. See the `LICENSE` file for more details.

---

By using these scripts, you can demonstrate your knowledge of reinforcement learning, simulation techniques, and efficient coding practices like parallel processing.

---
