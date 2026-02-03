# 🦠 Pandemic Flu Spread Simulation

## What This Project Does
Simulates influenza spread in a 21-student classroom using **100,000 Monte Carlo iterations** and compares results against a **discrete SIR (Susceptible-Infected-Recovered) model**. Validates simulation output against theoretical Binomial distributions.

This is the real ISyE 6644 group project (Group 102: Blake French, Hande Pehlivan, Teemu Kettunen).

---

## Files

| File | What It Is |
|---|---|
| `Flu_Simulation_12-1.ipynb` | **Base case**: 21 students, p = 0.02, 100K iterations + SIR comparison |
| `Flu_Simulation_12-1_s1.ipynb` | **Scenario 1**: Higher infection rate (p = 0.08), 10K iterations |
| `Flu_Simulation_12-1_s2.ipynb` | **Scenario 2**: Larger classroom (101 students), 10K iterations |
| `Day_2_expected_infections.xlsx` | Manual Excel derivation of the theoretical Day-2 expected value |
| `README.md` | This file |

---

## Key Parameters (Base Case)

| Parameter | Value |
|---|---|
| Class size | 21 students (Tommy + 20) |
| Infection probability per interaction | p = 0.02 |
| Days contagious | 3 |
| Simulation length | 30 days |
| Replications | 100,000 |

## Scenario Changes
- **Scenario 1** → p changed to **0.08** (more infectious disease)
- **Scenario 2** → Class size changed to **101 students** (larger population)

---

## How to Run

### Prerequisites
```bash
pip install numpy pandas matplotlib seaborn scipy
```

### Open in Jupyter
```bash
jupyter notebook Flu_Simulation_12-1.ipynb
```
Run cells top-to-bottom. The base case takes a few minutes because of 100K iterations.

### Faster run for testing
Open the notebook, find this cell:
```python
num_iterations = 100000
```
Change it to `1000` to see results quickly while developing.

---

## What the Notebooks Output
- **Histogram**: Day-1 infections (matches Binomial distribution)
- **Histogram**: Day-2 infections (including Tommy)
- **Bar chart**: Mean infected per day across 30 days
- **Histogram**: Epidemic duration (with and without zero-spread runs)
- **Binomial PMF plot**: Theoretical vs simulated
- **SIR vs Simulation comparison plot**: Shows where SIR diverges

---
