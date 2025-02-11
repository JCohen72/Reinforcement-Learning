# Reinforcement Learning

This repository contains 14 Jupyter Notebook projects that implement a wide range of reinforcement learning (RL) experiments—from classical bandit simulations and gridworld dynamic programming to advanced methods like state aggregation in TD learning and policy gradient baselines. The notebooks include detailed inline comments and docstrings, making them a practical resource for learning and research.

## Table of Contents

- [Repository Structure](#repository-structure)
  - [Editor Configurations](#editor-configurations)
  - [License](#license)
- [Project Notebooks](#project-notebooks)
  - [UCB_vs_epsilon_greedy_bandit.ipynb](#ucb_vs_epsilon_greedy_banditipynb)
  - [bandit_algorithm_parameter_study.ipynb](#bandit_algorithm_parameter_studyipynb)
  - [cliff_walking_sarsa_qlearning.ipynb](#cliff_walking_sarsa_qlearningipynb)
  - [epsilon_greedy_bandit.ipynb](#epsilon_greedy_banditipynb)
  - [gridworld_policy_evaluation_basic.ipynb](#gridworld_policy_evaluation_basicipynb)
  - [gridworld_value_iteration_basic.ipynb](#gridworld_value_iteration_basicipynb)
  - [mdp_policy_iteration_gridworld.ipynb](#mdp_policy_iteration_gridworldipynb)
  - [n_step_td_random_walk_plot.ipynb](#n_step_td_random_walk_plotipynb)
  - [off_policy_mc_simulation.ipynb](#off_policy_mc_simulationipynb)
  - [optimistic_vs_epsilon_greedy_bandit.ipynb](#optimistic_vs_epsilon_greedy_banditipynb)
  - [q_learning_vs_double_q_learning.ipynb](#q_learning_vs_double_q_learningipynb)
  - [td_mc_random_walk_simulation.ipynb](#td_mc_random_walk_simulationipynb)
  - [state_aggregation_in_large_scale_td.ipynb](#state_aggregation_in_large_scale_tdipynb)
  - [reinforce_short_corridor_baseline_comparison.ipynb](#reinforce_short_corridor_baseline_comparisonipynb)
- [Installation & Requirements](#installation--requirements)
- [Usage](#usage)
- [License Details](#license-details)

---

## Repository Structure

### Editor Configurations

- **.vscode/**  
  Contains VS Code settings and launch configurations to ensure a consistent development environment. (Not part of the core experiments.)

### License

- **LICENSE**  
  The repository is distributed under the MIT License. See the LICENSE file for details on reuse, modification, and distribution.

---

## Project Notebooks

Below is a brief description of each of the 14 notebooks based on my detailed review:

### UCB_vs_epsilon_greedy_bandit.ipynb

**Purpose:**  
Compares two action selection strategies for the multi-armed bandit problem:
- **Upper Confidence Bound (UCB):** Selects actions based on estimated rewards and uncertainty.
- **Epsilon-Greedy:** Uses a fixed exploration rate (ε) to occasionally choose random actions.

**Details:**  
- The notebook sets up a 10-armed bandit environment.
- It simulates multiple runs to plot average reward curves and the percentage of optimal actions.
- Code is modular, with clearly defined functions for updating value estimates and selecting actions.

---

### bandit_algorithm_parameter_study.ipynb

**Purpose:**  
Performs a systematic parameter study for bandit algorithms.

**Details:**  
- Explores the impact of hyperparameters (e.g., learning rate, exploration constants) on performance.
- Contains multiple experiments with different parameter settings.
- Generates plots showing trends in rewards and optimal action selection across trials.

---

### cliff_walking_sarsa_qlearning.ipynb

**Purpose:**  
Implements and compares on-policy SARSA with off-policy Q-learning using the cliff-walking environment.

**Details:**  
- The notebook simulates a gridworld with a “cliff” that imposes a high penalty.
- It visualizes how each algorithm converges to a policy while avoiding the cliff.
- Detailed commentary explains the differences between SARSA and Q-learning in risky environments.

---

### epsilon_greedy_bandit.ipynb

**Purpose:**  
Focuses on the epsilon-greedy algorithm for solving the 10-armed bandit problem.

**Details:**  
- Investigates how different values of ε affect learning performance.
- Provides visual comparisons of average reward and optimal action frequency.
- The code is structured to allow easy adjustment of exploration parameters.

---

### gridworld_policy_evaluation_basic.ipynb

**Purpose:**  
Implements basic policy evaluation in a gridworld environment.

**Details:**  
- Uses iterative dynamic programming to compute state-value functions for a fixed policy.
- Contains visualizations of the gridworld with state values.
- Code includes clear docstrings explaining the evaluation process.

---

### gridworld_value_iteration_basic.ipynb

**Purpose:**  
Demonstrates the value iteration algorithm to compute the optimal value function in a gridworld.

**Details:**  
- Applies the Bellman optimality equation iteratively.
- Includes convergence plots and visualizations of the derived optimal policy.
- Modular structure allows for easy modifications of the gridworld parameters.

---

### mdp_policy_iteration_gridworld.ipynb

**Purpose:**  
Uses policy iteration to solve a gridworld Markov Decision Process (MDP).

**Details:**  
- Alternates between policy evaluation and policy improvement.
- Provides detailed explanations and plots showing policy convergence.
- Compares the performance of policy iteration with value iteration methods.

---

### n_step_td_random_walk_plot.ipynb

**Purpose:**  
Explores n-step Temporal Difference (TD) learning in a random walk scenario.

**Details:**  
- Evaluates how varying the “n” parameter in TD learning affects value estimation.
- Compares n-step TD with one-step TD and Monte Carlo methods.
- Visual plots illustrate learning curves and the impact of n on convergence.

---

### off_policy_mc_simulation.ipynb

**Purpose:**  
Implements off-policy Monte Carlo (MC) simulation using importance sampling.

**Details:**  
- Demonstrates the process of learning a target policy from data generated by a different behavior policy.
- Provides insights into variance reduction and convergence issues in off-policy learning.
- Uses clear visualizations and commentary to explain importance sampling.

---

### optimistic_vs_epsilon_greedy_bandit.ipynb

**Purpose:**  
Compares two exploration strategies in the bandit problem:
- **Optimistic Initial Values:** Begins with high initial estimates to drive early exploration.
- **Epsilon-Greedy:** Balances exploration with a fixed probability of random action.

**Details:**  
- Runs parallel simulations to compare both strategies.
- Plots show the effects on average reward and the frequency of optimal action selection.
- Code includes detailed explanations of the trade-offs involved.

---

### q_learning_vs_double_q_learning.ipynb

**Purpose:**  
Contrasts standard Q-learning with Double Q-learning to mitigate overestimation bias.

**Details:**  
- Implements both algorithms in the same experimental setup.
- Directly compares learning curves, showing improvements in double Q-learning.
- Discussion in the notebook explains the theory behind reducing bias through decoupling action selection and evaluation.

---

### td_mc_random_walk_simulation.ipynb

**Purpose:**  
Compares Temporal Difference (TD) learning and Monte Carlo (MC) methods on a random walk problem.

**Details:**  
- Provides a side-by-side analysis of value function approximations using TD and MC.
- Visualizations highlight the convergence behavior and variance differences between the two methods.
- Code is structured to facilitate easy experimentation with different parameters.

---

### state_aggregation_in_large_scale_td.ipynb

**Purpose:**  
Investigates the use of state aggregation techniques in large-scale TD learning.

**Details:**  
- Groups similar states into clusters to reduce the computational burden in environments with many states.
- Evaluates how aggregation impacts the accuracy and efficiency of value estimation.
- Contains experiments that illustrate trade-offs between state resolution and learning performance.

---

### reinforce_short_corridor_baseline_comparison.ipynb

**Purpose:**  
Compares the REINFORCE policy gradient method with baseline strategies in a “short corridor” environment.

**Details:**  
- Implements the REINFORCE algorithm and examines the effect of incorporating a baseline to reduce variance.
- Compares learning performance through reward curves and convergence plots.
- Provides commentary on how baseline methods can improve policy gradient stability.

---

## Installation & Requirements

1. **Clone the Repository**

   ```bash
   git clone https://github.com/JCohen72/Reinforcement-Learning.git
   cd Reinforcement-Learning
   ```

2. **Install Dependencies**

   Ensure you have Python 3 installed. Then install the required libraries:

   ```bash
   pip install numpy matplotlib joblib gym
   ```

   *Note:* Some notebooks might require additional packages as noted in their first cells.

---

## Usage

1. **Launch Jupyter Notebook**

   From the repository’s root directory, start Jupyter:

   ```bash
   jupyter notebook
   ```

2. **Open a Notebook**

   Select any of the 14 project notebooks (e.g., `epsilon_greedy_bandit.ipynb` or `state_aggregation_in_large_scale_td.ipynb`) to explore and run the experiments.

3. **Run the Cells**

   Execute cells sequentially to run simulations, visualize outputs, and experiment with parameters.

---

## License Details

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for full details regarding reuse, modification, and distribution.
