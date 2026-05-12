# Frequent Itemset Mining — Apriori vs ProbBF

## Overview

This project presents a comparative analysis of **Frequent Itemset Mining (FIM)** algorithms using multiple optimization techniques and modern probabilistic approaches.

The notebook evaluates:

* Standard **Apriori Algorithm**
* Optimized **Apriori with Vertical TID Lists**
* Modern **ProbBF Algorithm** (Probabilistic Bloom Filter-Based Mining)

The experiments are performed on benchmark datasets:

* Chess Dataset
* Connect Dataset
* Mushroom Dataset

The project focuses on:

* Runtime Performance
* Memory Usage
* Number of Frequent Itemsets Generated
* Optimization Efficiency
* Scalability Analysis

---

# Project Objectives

The main goals of this project are:

* Implement classical and modern FIM algorithms
* Compare optimized and non-optimized approaches
* Analyze performance on large datasets
* Measure execution time and memory consumption
* Visualize results using graphs and tables
* Understand how optimization improves Apriori performance

---

# Algorithms Implemented

## 1. Standard Apriori Algorithm

The baseline implementation of Apriori generates candidate itemsets level by level and repeatedly scans the database to calculate support counts.

### Features

* Candidate generation
* Support counting
* Iterative pruning
* Multi-pass database scanning

### Limitation

* High runtime for large datasets
* Repeated database scans increase computational cost

---

## 2. Optimized Apriori using Vertical TID Lists

This optimized version stores transaction ID lists for each item and computes support using set intersections instead of scanning the database repeatedly.

### Optimization Benefits

* Faster support counting
* Reduced database scans
* Improved scalability
* Better runtime performance

---

## 3. ProbBF Algorithm

This implementation is based on the probabilistic frequent itemset mining approach proposed in recent research.

### Key Idea

After the second pass, the algorithm predicts support probabilistically instead of performing expensive database scans.

### Advantages

* Reduced computational overhead
* Faster mining on large datasets
* Lower scanning cost
* Modern probabilistic optimization

---

# Technologies Used

* Python
* Pandas
* Matplotlib
* itertools
* tracemalloc
* psutil
* Jupyter Notebook

---

# Project Structure

```bash
.
├── FIM_Project.ipynb
├── chess.dat
├── connect.dat
├── mushroom.dat
├── results.csv
└── README.md
```

---

# Dataset Information

The following benchmark datasets are used:

| Dataset  | Description                          |
| -------- | ------------------------------------ |
| Chess    | Chess game configurations            |
| Connect  | Connect-4 game states                |
| Mushroom | Mushroom classification transactions |

Each dataset contains transactions where items are represented as integers.

---

# Installation

## Clone Repository

```bash
git clone (https://github.com/Musmannazir/DAA_Algo)
cd frequent-itemset-mining
```

## Install Dependencies

```bash
pip install pandas matplotlib psutil
```

---

# Running the Project

## Step 1: Place Dataset Files

Put these files in the same directory as the notebook:

* `chess.dat`
* `connect.dat`
* `mushroom.dat`

## Step 2: Open Jupyter Notebook

```bash
jupyter notebook
```

## Step 3: Run the Notebook

Open:

```bash
FIM_Project.ipynb
```

Run all cells sequentially.

---

# Performance Metrics

The project compares algorithms using:

* Execution Time
* Memory Consumption
* Number of Frequent Itemsets
* Speedup over Baseline Apriori

---

# Visualizations Included

The notebook generates:

* Runtime Comparison Graphs
* Memory Usage Graphs
* Frequent Itemset Comparison Charts
* Optimization Speedup Analysis

---

# Experimental Results

The experiments demonstrate that:

* Optimized Apriori performs significantly better than the baseline approach.
* ProbBF reduces expensive database scans and improves scalability.
* Vertical TID optimization greatly improves support counting efficiency.
* Performance gains become more noticeable on larger datasets.

---

# Sample Output

The notebook exports:

```bash
results.csv
```

which contains:

* Dataset Name
* Algorithm Used
* Minimum Support
* Runtime
* Memory Usage
* Frequent Itemsets Count

---

# Complexity Analysis

| Algorithm            | Time Complexity               | Optimization             |
| -------------------- | ----------------------------- | ------------------------ |
| Standard Apriori     | High due to repeated scans    | None                     |
| Vertical TID Apriori | Reduced support counting cost | Set Intersection         |
| ProbBF               | Reduced scanning after pass 2 | Probabilistic Prediction |

---

# Future Improvements

Possible future enhancements include:

* FP-Growth implementation
* Parallel processing
* GPU acceleration
* Distributed mining with Spark
* Real-time streaming datasets
* Interactive dashboard visualization

---

# Research Reference

This project references modern probabilistic frequent itemset mining concepts inspired by:

**Sadeequllah et al. (2024)**

---

# Author

## Usman

Artificial Intelligence Student | Python Developer | AI & Data Mining Enthusiast

---

# License

This project is for educational and research purposes.

---

# GitHub Topics

```text
frequent-itemset-mining
apriori-algorithm
data-mining
machine-learning
python
probabilistic-algorithms
jupyter-notebook
algorithm-analysis
optimization
research-project
```
