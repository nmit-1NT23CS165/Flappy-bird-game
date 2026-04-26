# 🐦 Flappy Bird AI — NEAT Algorithm

An AI-powered Flappy Bird game built with Python and Pygame, where a neural network learns to play the game on its own using the NEAT (NeuroEvolution of Augmenting Topologies) algorithm.

---

## 🎮 Demo

The AI starts off knowing nothing about the game. Through evolution across generations, it learns to navigate through pipes without any hardcoded rules — just raw trial and error.

---

## 🧠 How the AI Works (NEAT)

NEAT stands for **NeuroEvolution of Augmenting Topologies**. It's a genetic algorithm that evolves neural networks over generations — similar to how biological evolution works.

### Each bird in the simulation has:
- Its own **neural network** (brain)
- Its own **genome** (the DNA of the network)

### The neural network takes 3 inputs:
1. The bird's current **Y position**
2. The distance to the **top pipe**
3. The distance to the **bottom pipe**

And outputs a single decision: **jump or don't jump**.

### How evolution works:
1. A population of birds all play simultaneously
2. Birds that survive longer get a **higher fitness score**
3. Birds that die early are eliminated
4. The best-performing genomes are **selected and mutated** to create the next generation
5. Over many generations, the birds get progressively better

This means the AI **teaches itself** to play — no training data, no hardcoded rules.

---

## 🛠️ Tech Stack

- **Python 3.11**
- **Pygame** — game engine and rendering
- **NEAT-Python** — neuroevolution library
- **Matplotlib + Graphviz** — visualizing neural networks and stats

---

## 🚀 How to Run

### 1. Clone the repo
```bash
git clone https://github.com/nmit-1NT23CS165/Flappy-bird-game.git
cd Flappy-bird-game
```

### 2. Install dependencies
```bash
pip install pygame neat-python matplotlib graphviz numpy
```

### 3. Run the game
```bash
python flappy_bird.py
```

The AI will start training immediately. Watch it improve across generations in real time!

---

## 📁 Project Structure

```
Flappy-bird-game/
│
├── flappy_bird.py          # Main game + NEAT integration
├── visualize.py            # Neural network & stats visualizer
├── config-feedforward.txt  # NEAT configuration
├── requirements.txt        # Dependencies
└── imgs/                   # Game assets (bird, pipe, background)
```

---

## ⚙️ NEAT Configuration Highlights

| Parameter | Value | Description |
|-----------|-------|-------------|
| `pop_size` | 50 | Number of birds per generation |
| `fitness_threshold` | 100 | Score at which training stops |
| `num_inputs` | 3 | Bird Y, top pipe dist, bottom pipe dist |
| `num_outputs` | 1 | Jump or not |

---

## 📊 Results

The AI typically learns to pass pipes consistently within **5–10 generations**, and can achieve very high scores by generation 20+.

---

## 👩‍💻 Author

Made by **Pracheta-1NT23CS165** as part of an AI/ML project.
