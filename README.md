# 📊 Central Limit Theorem — Simulation Study

A hands-on statistical simulation project exploring the **Central Limit Theorem (CLT)** through Python, using both normal and exponential population distributions.

---

## 📌 Overview

This project investigates how the distribution of **sample means** behaves as sample size grows, using Monte Carlo-style simulations. By drawing thousands of samples from two different population types, we empirically verify the core predictions of the CLT and compare observed results against theoretical values.

---

## 🎯 Objectives

- Generate and visualize two distinct populations: **Normal** and **Exponential**
- Simulate **1,000 samples** for each of five sample sizes: `n = 16, 25, 36, 100, 400`
- Compute and compare **observed vs. theoretical Standard Error of the Mean (SEM)**
- Overlay theoretical normal curves on sample mean histograms
- Analyze how population shape affects convergence to normality

---

## 🧪 Key Concepts

| Concept | Description |
|---|---|
| **Central Limit Theorem** | The distribution of sample means approaches a normal distribution as `n` increases, regardless of population shape |
| **Standard Error of the Mean (SEM)** | Measures how much sample means vary; calculated as `σ / √n` |
| **Normal Population** | Already bell-shaped; sample means look normal even at small `n` |
| **Exponential Population** | Right-skewed; requires larger `n` before sample means converge to normal |

---

## 🛠️ Tech Stack

- **Python 3**
- `numpy` — numerical computations
- `pandas` — tabular data & comparison tables
- `matplotlib` — histogram plots and overlaid normal curves
- `scipy.stats` — theoretical normal PDF generation
- `random` — seeded population generation and sampling

---

## 📂 Project Structure

```
trabalho_t2.ipynb       # Main Jupyter Notebook with all simulations and analyses
README.md               # Project documentation
```

---

## 📈 Results Summary

### Normal Population
- Sample means followed a normal distribution **at all values of `n`**, consistent with the population already being normally distributed
- Observed SEM closely matched the theoretical SEM (`σ / √n`) across all sample sizes
- As `n` increased, the distribution became narrower and better aligned with the theoretical curve

### Exponential Population
- For small `n` (16, 25), the distribution of sample means remained **visibly skewed**, with poor fit to the theoretical normal curve
- For large `n` (100, 400), the distribution converged clearly to normal, confirming the CLT even for heavily skewed populations
- SEM behavior was consistent with theory — the observed and theoretical values tracked very closely

---

## 📊 Sample Output

The notebook generates side-by-side histogram panels for each sample size, with **red theoretical normal curves** overlaid:

```
n = 16    n = 25    n = 36    n = 100    n = 400
[ hist ]  [ hist ]  [ hist ]  [ hist ]   [ hist ]
```

Each panel also compares observed vs. theoretical SEM in tabular format.

---

## 🔍 Conclusions

1. **Shape matters at small `n`**: Normal populations converge to a normal sampling distribution quickly; skewed populations (like exponential) need larger samples
2. **The CLT holds empirically**: Observed sample mean distributions matched theoretical predictions closely across both populations
3. **SEM decreases with `n`**: Confirmed by the `σ / √n` relationship — larger samples yield more precise estimates

---

## ▶️ How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib scipy
   ```
3. Open the notebook:
   ```bash
   jupyter notebook trabalho_t2.ipynb
   ```
4. Set your team leader's `RA` value in the appropriate cell to generate your group's custom populations
5. Run all cells in order

---

## 📚 Context

This project was developed as an academic assignment for a **Data Science & A.I** course. It demonstrates the practical application of the Central Limit Theorem through simulation, reinforcing theoretical concepts with empirical evidence.
