# Task 5 — Poisson Distribution

---

## 1. Experiment Description (Events in a Fixed Interval)

We consider an experiment where random events occur in a fixed interval of time or space.

Example:
- number of error messages received in one hour
- number of calls received per minute
- number of defects in a product section

---

### Sample Space

The sample space consists of all possible counts of events:

$$
\Omega = \{0, 1, 2, 3, 4, \dots\}
$$

---

### Elementary Outcome

An elementary outcome represents a specific number of events:

$$
\omega = k
$$

where \(k\) is a non-negative integer.

---

### Random Variable

We define:

$$
X(\omega) = \text{number of events occurring in the interval}
$$

---

## 2. PMF of Poisson Distribution

The probability mass function is:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

### Parameter:
- \( \lambda \) = average number of events in the interval

---

## 3. Support of X

The support is:

$$
\{0, 1, 2, 3, \dots\}
$$

### Explanation:
The Poisson distribution is unbounded because there is no theoretical maximum number of events that can occur.

---

## 4. PMF Graphs (Effect of λ)

We plot the PMF for different values of \( \lambda \):

- small \( \lambda \): distribution is concentrated near 0
- medium \( \lambda \): bell-like shape starts forming
- large \( \lambda \): distribution shifts right and spreads out

---

## 5. CDF Graphs

The CDF is:

$$
F(x) = P(X \le x)
$$

- step function
- increases from 0 to 1
- becomes smoother as \( \lambda \) increases

---

## 6. Effect of Increasing λ

When \( \lambda \) increases:

- mean increases
- distribution shifts to the right
- spread becomes larger
- shape becomes more symmetric (approaches normal distribution)

---

## 7. Probability Calculations

### (a) Exact probability

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

### (b) Cumulative probability

$$
P(X \le k) = F(k)
$$

---

### (c) Tail probability

$$
P(X \ge k) = 1 - F(k - 1)
$$

---

### (d) Interval probability

$$
P(a \le X \le b) = F(b) - F(a - 1)
$$

---

## 8. PMF vs CDF Comparison

### Using PMF:
We sum individual probabilities:

P(X ≤ k) = P(0) + P(1) + ... + P(k)

### Using CDF:
We directly use:

F(k) = P(X ≤ k)

✔ Both methods give the same result, but CDF is faster for cumulative probabilities.

---

## 9. Practical Applications of Poisson Distribution

The Poisson model is used when events occur randomly and independently over time or space.

Examples:
- number of calls in a call center per hour
- number of emails received per minute
- number of accidents in a day
- number of defects in manufacturing
- number of website requests per second

---

## 10. Optional Application (Interactive Tool)

A small application can be created to explore the Poisson distribution.

### Features:
- input parameter λ
- display PMF graph
- display CDF graph
- compare multiple λ values on same plot

### Idea:
- slider for λ
- real-time graph update
- comparison of different rates
