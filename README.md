# PACSOY-502008-Multi-armed-Bandit-Algorithms
## basic dataset
- [Movie Lens Dataset](https://grouplens.org/datasets/movielens/1m/)
- [Goodreads Dataset](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home)(only use dataset "goodreads_books.json")

# Multi-Armed Bandit Algorithms

This repository contains implementations of various Multi-Armed Bandit (MAB) algorithms, including ε-Greedy, Thompson Sampling, and Upper Confidence Bound (UCB). The algorithms are applied to a movie recommendation dataset to compare their performance in terms of cumulative regret.

## Prerequisites

Before running the code, ensure you have Python installed on your system. You can download Python from [python.org](https://www.python.org/).

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/multi-armed-bandit.git
   cd multi-armed-bandit
   ```

2. **Install the required dependencies:**
   ```bash
   pip -r requirement.txt
   ```

3. **Download the MovieLens Dataset:**
   - The MovieLens dataset can be downloaded from [GroupLens](https://grouplens.org/datasets/movielens/1m/).
   - Extract the dataset and place the `ratings.dat` and `movies.dat` files in the `data/Movie Lens` directory.

4. **Run the preprocessing script:**
   ```bash
   python preprocess.py
   ```
   This script will generate `arms.json` and `rewards.json` files in the `save` directory.

## Running the Algorithms

### ε-Greedy Algorithm


### Thompson Sampling Algorithm

### Upper Confidence Bound (UCB) Algorithm

## Visualization

Each algorithm script will generate a plot showing the cumulative regret over time. The plots will help you compare the performance of different algorithms.

## Directory Structure

```
C:.
│  README.md
│  preprocess.py
│  epsilongreedy.py
│  TS.py
│  UCB.py
│
├─data
│  ├─Goodreads
│  ├─Movie Lens
│  │      movies.dat
│  │      ratings.dat
│  │      users.dat
│  │
│  └─Open Bandits
│
└─save
        arms.json
        rewards.json
```

