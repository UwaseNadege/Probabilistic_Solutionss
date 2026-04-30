# Task 1 — Discrete Distribution Given by a PMF Table
## Quick Idea: PMF, PDF, and CDF

- **PMF (Probability Mass Function)** → used for discrete variables  
  Gives probability of exact values: P(X = x)

- **PDF (Probability Density Function)** → used for continuous variables  
  Gives probability over an interval using integration:
  P(a ≤ X ≤ b) = area under the curve

- **CDF (Cumulative Distribution Function)** → works for both  
  Gives accumulated probability:
  F(x) = P(X ≤ x)

👉 Summary:
PMF = exact values  
PDF = continuous density  
CDF = accumulated probability

## Introduction
This task deals with a discrete random variable \(X\) whose probability distribution is given in tabular form.

The goal is to:
- define the probability space,
- verify the distribution,
- construct the PMF and CDF,
- compute probabilities,
- and interpret the relationship between PMF and CDF.

---

## Given Data

| x        | -2  | 0   | 1   | 3   | 5   |
|----------|-----|-----|-----|-----|-----|
| P(X = x) | 0.10| 0.25| 0.30| 0.20| 0.15|

---

## 1. Random Experiment and Random Variable

We define a probability space where each outcome corresponds to one possible value of the random variable.

Let the sample space be:

$$
\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}
$$

We define the random variable \(X\) as:

$$
X(\omega_1) = -2,\quad
X(\omega_2) = 0,\quad
X(\omega_3) = 1,\quad
X(\omega_4) = 3,\quad
X(\omega_5) = 5
$$

### Explanation:
Each outcome in the sample space represents one possible result of the experiment, and the random variable assigns a numerical value to each outcome.

---

## 2. Verification of Probability Distribution

A valid probability distribution must satisfy:

$$
\sum P(X = x) = 1
$$

Checking:

$$
0.10 + 0.25 + 0.30 + 0.20 + 0.15 = 1.00
$$

### Conclusion:
Since the sum equals 1, this is a valid probability distribution.

---

## 3. Probability Mass Function (PMF)

The PMF describes the probability of each exact value of \(X\):

$$
P(X = x) =
\begin{cases}
0.10 & x = -2 \\
0.25 & x = 0 \\
0.30 & x = 1 \\
0.20 & x = 3 \\
0.15 & x = 5 \\
0 & \text{otherwise}
\end{cases}
$$

### Explanation:
The PMF assigns a probability to each possible value of the random variable.

---

## 4. Cumulative Distribution Function (CDF)

The CDF is defined as:

$$
F(x) = P(X \le x)
$$

We compute it step by step:

$$
F(x) =
\begin{cases}
0 & x < -2 \\
0.10 & -2 \le x < 0 \\
0.35 & 0 \le x < 1 \\
0.65 & 1 \le x < 3 \\
0.85 & 3 \le x < 5 \\
1 & x \ge 5
\end{cases}
$$

### Explanation:
The CDF gives the accumulated probability up to a certain value of \(x\).

---

## 5. Relationship Between PMF and CDF

Each jump in the CDF corresponds to a probability in the PMF:

- Jump at \(x = -2\): \(0.10\)
- Jump at \(x = 0\): \(0.25\)
- Jump at \(x = 1\): \(0.30\)
- Jump at \(x = 3\): \(0.20\)
- Jump at \(x = 5\): \(0.15\)

### Explanation:
The size of each jump in the CDF is exactly equal to the PMF value at that point.

---

## 6. Probability Calculations

### (a) Exact probability

$$
P(X = 1) = 0.30
$$

---

### (b) Cumulative probability

$$
P(X \le 1) = 0.10 + 0.25 + 0.30 = 0.65
$$

---

### (c) Strict inequality

$$
P(X < 1) = 0.10 + 0.25 = 0.35
$$

---

### (d) Interval probability

$$
P(0 < X \le 3) = 0.30 + 0.20 = 0.50
$$

---

### (e) Greater or equal

$$
P(X \ge 3) = 0.20 + 0.15 = 0.35
$$

---

## 7. Compare PMF and CDF Results

We compare probabilities obtained using the PMF and the CDF to show that both methods give the same results.

---

### Key Idea

- PMF gives probabilities directly for each value of X
- CDF gives accumulated probabilities up to a value
- We can compute probabilities using either method

---

### Example 1: Exact Probability

P(X = 1)

- From PMF:
  P(X = 1) = 0.30

- From CDF:
  The jump at X = 1 is also 0.30

✔ Both methods give the same result

---

### Example 2: Cumulative Probability

P(X ≤ 1)

- From PMF:
  0.10 + 0.25 + 0.30 = 0.65

- From CDF:
  F(1) = 0.65

✔ Same result

---

### Example 3: Interval Probability

P(0 < X ≤ 3)

- From PMF:
  0.30 + 0.20 = 0.50

- From CDF:
  F(3) − F(0) = 0.85 − 0.35 = 0.50

✔ Same result

---

### Final Conclusion

- PMF and CDF are consistent representations of the same distribution
- PMF is used for direct probabilities
- CDF is used for cumulative probabilities
- Both methods always agree when computed correctly

