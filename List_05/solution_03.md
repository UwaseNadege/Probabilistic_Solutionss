# Task 3 — Binomial Distribution Bin(n, p)

---

## 1. Bernoulli Trials Model (Experiment Description)

We model the experiment as **n independent Bernoulli trials**.

Each trial has only two outcomes:
- Success (S)
- Failure (F)

Each trial has:
- Probability of success: p  
- Probability of failure: 1 − p  

---

### Sample Space

A sample space consists of all sequences of length n made of S and F:

$$
\Omega = \{(S,F,S,S,F,\dots)\}
$$

Each element ω represents one possible sequence of outcomes.

---

### Elementary Outcome

An elementary outcome is:

$$
\omega = (x_1, x_2, \dots, x_n)
$$

where each \(x_i \in \{S, F\}\)

---

### Random Variable

We define:

$$
X(\omega) = \text{number of successes in the n trials}
$$

So X counts how many successes occur in the experiment.

---

## 2. PMF of Binomial Distribution

The probability mass function is:

$$
P(X = k) = \binom{n}{k} p^k (1 - p)^{n-k}
$$

---

## 3. Support of X

The support is all possible values of X:

$$
\{0, 1, 2, \dots, n\}
$$

---

## 4. PMF Graphs (Parameter Changes)

We study two cases:

### (a) Fixed n, different p
- When p increases:
  - distribution shifts to the right
  - higher probability of large k

---

### (b) Fixed p, different n
- When n increases:
  - distribution becomes wider
  - shape becomes more smooth and symmetric (if p ≈ 0.5)

---

## 5. CDF Graphs

The CDF is defined as:

$$
F(x) = P(X \le x)
$$

- It is a step function
- Increases from 0 to 1
- Jumps at integer values of X

---

## 6. Shape Changes

### When p increases:
- mean increases: np increases
- graph shifts to the right
- more probability of success outcomes

---

### When n increases:
- distribution becomes more spread out
- shape becomes smoother
- tends toward normal distribution (for large n)

---

## 7. Probability Calculations

### (a) Exact probability

$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

---

### (b) Cumulative probability

$$
P(X \le k) = F(k)
$$

---

### (c) Greater than

$$
P(X \ge k) = 1 - F(k-1)
$$

---

### (d) Interval probability

$$
P(a \le X \le b) = F(b) - F(a-1)
$$

---

## 8. PMF vs CDF Computation

- PMF is used when calculating exact values P(X = k)
- CDF is used for ranges and inequalities

Example:

- PMF: P(X = k)
- CDF: P(X ≤ k)

Both methods give the same results when applied correctly.

---

## 9. Practical Applications of Binomial Distribution

The binomial model is used when:
- fixed number of trials
- each trial has two outcomes
- constant probability

### Examples:
- defective items in manufacturing
- pass/fail exams
- coin flips
- success in marketing campaigns
- medical test results (positive/negative)

---

## 10. Optional Application (Interactive Tool)

A small application can be built to compare binomial distributions.

### Features:
- input n and p
- plot PMF graph
- plot CDF graph
- compare two distributions on same graph

---

### Example Python Idea

- Use matplotlib for plotting
- Allow user to change:
  - n
  - p
- Display:
  - PMF bar chart
  - CDF step chart
  - comparison overlay
