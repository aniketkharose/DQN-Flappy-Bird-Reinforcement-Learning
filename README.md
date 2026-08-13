# 🐦 DQN-Based Flappy Bird Reinforcement Learning Agent

A Deep Reinforcement Learning project that uses a **Deep Q-Network (DQN)** to train an agent to play the Flappy Bird game through trial and error.

> 🎓 **Course Project:** This project was implemented as part of my AI/ML learning journey to understand Reinforcement Learning and Deep Q-Learning.

---

## 📌 Project Overview

In this project, a Reinforcement Learning agent learns to play Flappy Bird by interacting with the game environment and receiving rewards based on its actions.

The agent gradually improves its gameplay by learning which actions are more valuable in different game states.

The project demonstrates how **Reinforcement Learning concepts can be combined with Deep Learning** to handle a more complex environment.

---

## 🧠 Concepts Covered

- Reinforcement Learning
- Q-Learning
- Deep Reinforcement Learning
- Deep Q-Network (DQN)
- Q-Value Estimation
- Experience Replay
- Replay Buffer
- ε-Greedy Exploration
- Exploration vs Exploitation
- ε-Decay
- Target Network
- Temporal Difference Learning
- Neural Network Training

---

## ⚙️ How DQN Works

The basic learning process is:

```text
Current State
     ↓
DQN Neural Network
     ↓
Q-Values
     ↓
Select Action
     ↓
Flappy Bird Game
     ↓
Reward + Next State
     ↓
Replay Buffer
     ↓
Random Mini-Batch
     ↓
Train DQN
     ↓
Repeat
```

The agent learns to select actions that maximize its cumulative reward.

---

## 🎮 Actions

The agent can perform actions such as:

- Flap
- Do Nothing

The DQN predicts a Q-value for each possible action.

The action with the highest Q-value can be selected during exploitation.

---

## 💾 Experience Replay

The agent stores experiences in a replay buffer.

Each experience contains:

```text
(State, Action, Reward, Next State, Done)
```

Random mini-batches are sampled from the replay buffer to train the neural network.

This helps reduce correlation between consecutive experiences and improves training stability.

---

## 🔍 Exploration vs Exploitation

The project uses an **ε-greedy strategy**.

- **Exploration:** Select a random action to discover new possibilities.
- **Exploitation:** Select the action with the highest predicted Q-value.

The value of ε gradually decreases during training using **ε-decay**, allowing the agent to move from exploration toward exploitation.

---

## 🎯 Target Network

DQN uses two networks:

### Online / Policy Network
Learns continuously and predicts current Q-values.

### Target Network
Provides more stable target Q-values during training.

The target network is periodically updated using the weights of the online network.

---

## 🛠️ Technologies Used

- **Python**
- **PyTorch**
- **Gymnasium**
- **Flappy Bird Gymnasium**
- **Pygame**
- **NumPy**
- **PyYAML**

---

## 📁 Project Structure

```text
RL_DQN-main/
│
├── agent.py
├── dqn.py
├── experience_replay.py
├── game_flappy_bird.py
├── parameters.yaml
│
├── runs/
│   └── Trained model and training logs
│
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/DQN-Flappy-Bird-Reinforcement-Learning.git
```

### 2. Navigate to the project

```bash
cd DQN-Flappy-Bird-Reinforcement-Learning
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the environment

**Windows:**

```bash
venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install torch gymnasium flappy-bird-gymnasium pygame pyyaml numpy
```

### 6. Run the project

Follow the training/inference command configured in `agent.py` and `parameters.yaml`.

---

## 📊 Training

During training, the agent interacts with the environment repeatedly.

The general process is:

```text
Observe State
     ↓
Choose Action
     ↓
Receive Reward
     ↓
Store Experience
     ↓
Sample Experience
     ↓
Train DQN
     ↓
Update Network
     ↓
Repeat
```

Over multiple episodes, the agent attempts to improve its performance.

---

## 🎯 Learning Objective

The main objective of this project is to understand how a **Deep Q-Network** can be used to solve a Reinforcement Learning problem.

The project helped me understand:

- How an RL agent interacts with an environment
- How Q-values are estimated using a neural network
- How experience replay works
- How exploration and exploitation are balanced
- Why target networks are used in DQN
- How Deep Learning can be applied to Reinforcement Learning

---

## 📚 Learning Reference

This project was implemented as part of my **AI/ML course learning journey**.

The project is intended for **educational and learning purposes**.

---

## 👨‍💻 Author

**Aniket Kharose**

BE Electronics & Telecommunication Engineering  
Aspiring Embedded, Communication & AI/ML Engineer

---

⭐ If you find this project useful for learning Reinforcement Learning, feel free to explore the repository.
