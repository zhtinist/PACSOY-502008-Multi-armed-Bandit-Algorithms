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
   ```
   git clone https://github.com/your-username/multi-armed-bandit.git
   cd multi-armed-bandit
   ```

2. **Install the required dependencies:**
   ```
   pip install -r requirements.txt
   ```
The project relies on the following Python libraries: numpy, matplotlib, joblib, and scipy:

numpy for numerical operations,

matplotlib for visualization,

joblib for parallel execution,

scipy for statistical modeling (used in Bayes-UCB).
   
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
│  epsilongreedy(optimised).ipynb
│  TS(optimised).ipynb
│  UCB(optimised).ipynb
│  Bootstrap Thompson Sampling（BTS）.ipynb
│  Bayes-UCB.ipynb
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


## OPtimized
```
In this project, we systematically implemented and optimized three classic Multi-Armed Bandit (MAB) algorithms: ε-Greedy, Upper Confidence Bound (UCB), and Thompson Sampling (TS). To enhance computational efficiency and scalability, several optimization strategies were applied:

Parallel Execution: We employed the joblib library to run each algorithm 10 times in parallel (n_jobs=-1), maximizing CPU utilization and significantly reducing runtime.

Numerical Stability Enhancements: For example, a small constant (1e-5) was added in UCB calculations to prevent division by zero, improving robustness.

Vectorized Implementation: We used NumPy arrays for initializing and updating all metrics, resulting in faster computations and cleaner code.

Standardized Experimentation: All algorithms were run for the same number of steps and trials. We recorded cumulative regrets and visualized the average performance with standard error bands for fair comparison.

```

## New Algorithms
```
Bayesian UCB (Bayes-UCB): This method integrates Bayesian inference into the UCB framework by estimating posterior distributions and computing confidence bounds using scipy.stats.norm.ppf. It is especially useful when prior knowledge or distributional assumptions are available.

Bootstrap Thompson Sampling (BTS): To overcome the dependency on predefined priors in standard TS, we implemented a non-parametric version that performs bootstrap resampling of observed rewards. This approach allows greater flexibility and adaptability to unknown or non-Gaussian reward distributions, making it highly applicable to real-world data.
```

## Summary

```
Together, these optimizations and algorithmic extensions resulted in a robust, extensible, and efficient experimental framework for comparing MAB algorithms. This framework is well-suited for practical applications such as recommendation systems, online decision-making, and adaptive experimentation, providing both empirical strength and theoretical justification.
```
