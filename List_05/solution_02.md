# Task 2 — Discrete Distribution Given by a CDF Table

## Introduction
We are given the **cumulative distribution function (CDF)** of a discrete random variable \(X\).  
From this, we will reconstruct the **PMF**, define a probability space, and compute probabilities.

---

## Given Data

| x        | -1  | 0   | 2   | 4   | 6   |
|----------|-----|-----|-----|-----|-----|
| F(x)     | 0.15| 0.35| 0.60| 0.85| 1.00|

---

## 1. Construct a Probability Space

We construct a finite sample space:

$$
\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}
$$

Define the random variable \(X\) such that:

- X(ω₁) = -1  
- X(ω₂) = 0  
- X(ω₃) = 2  
- X(ω₄) = 4  
- X(ω₅) = 6  
---

## 2. Reconstruct the PMF from the CDF

The PMF is found by computing the **jumps of the CDF**:

- P(X = -1) = 0.15
- P(X = 0)  = 0.35 − 0.15 = 0.20
- P(X = 2)  = 0.60 − 0.35 = 0.25
- P(X = 4)  = 0.85 − 0.60 = 0.25
- P(X = 6)  = 1.00 − 0.85 = 0.15

---

## 3. PMF Table

| x        | -1  | 0   | 2   | 4   | 6   |
|----------|-----|-----|-----|-----|-----|
| P(X = x) | 0.15| 0.20| 0.25| 0.25| 0.15|

---

## 4. PMF Graph (Concept)

The PMF graph is a **bar chart** with heights:

- -1 → 0.15  
- 0 → 0.20  
- 2 → 0.25  
- 4 → 0.25  
- 6 → 0.15  

---

## 5. CDF Graph (Step Function)

The CDF is a step function:

- constant between values of x
- jumps at: -1, 0, 2, 4, 6

---

## 6. Jump Points of the CDF

The CDF jumps at:

- x = -1  
- x = 0  
- x = 2  
- x = 4  
- x = 6  

### Key Idea:
Each jump size equals:

P(X = x)

---

## 7. Why Jump Size = Probability

At each point:

$$
\text{Jump size} = F(x) - F(x^-)
$$

This represents the probability mass at that point.

So:

- larger jump → higher probability
- no jump → probability = 0

---

## 8. Probability Calculations

### (a) Cumulative probability

P(X ≤ 2)

= F(2)

= 0.60

---

### (b) Strict inequality

P(X < 2)

= F(0)

= 0.35

---

### (c) Exact probability

P(X = 4)

= 0.25

---

### (d) Interval probability

P(0 < X ≤ 4)

= F(4) − F(0)

= 0.85 − 0.35 = 0.50

---

### (e) Greater than

P(X > 2)

= 1 − F(2)

= 1 − 0.60 = 0.40

---

## 9. Comparison: PMF vs CDF (Task 1 vs Task 2)

### PMF (Task 1 style)
- probabilities are given directly
- easy to compute exact values
- harder to get cumulative probabilities

### CDF (Task 2 style)
- probabilities are accumulated
- easy to compute intervals
- PMF must be reconstructed from differences

### Key Difference:
- PMF → direct probabilities  
- CDF → built-in accumulation  

---
