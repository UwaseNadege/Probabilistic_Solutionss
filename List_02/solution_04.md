# Task 4 — Poisson Model (Arrival of Events)

## Introduction
We analyze a process using the **Poisson distribution**, which models the number of events occurring in a fixed interval of time or space.

We are given:

- Average number of error reports per hour: **3**
- Events occur independently
- The rate is constant over time

---

## 1. Random Experiment

We observe the number of error reports received by a web service during a **one-hour interval**.

Each outcome represents a count of how many error reports occur in that hour.

---

## 2. Sample Space

The sample space consists of all possible non-negative integer values:

$$
\Omega = \{0, 1, 2, 3, 4, 5, \dots\}
$$

---

## 3. Probability Distribution

The Poisson probability mass function is:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

### Parameter

- \( \lambda \) = average number of events in the given interval
  
λ : (lambda)
---

## 4. Interpretation of \( \lambda \)

In this problem:

$$
\lambda = 3 
$$

This means:

- On average, **3 error reports occur per hour**
- \( \lambda \) represents the **expected number of events in one hour**

---

### Examples of Probabilities

#### **P(X = 0)**

$$
P(X = 0) = \frac{3^0 e^{-3}}{0!} = e^{-3}
$$

$$
P(X = 0) \approx 0.0498
$$

---

#### **P(X = 1)**

$$
P(X = 1) = \frac{3^1 e^{-3}}{1!} = 3e^{-3}
$$

$$
P(X = 1) \approx 0.1494
$$

---

#### **P(X = 2)**

$$
P(X = 2) = \frac{3^2 e^{-3}}{2!} = \frac{9}{2} e^{-3}
$$

$$
P(X = 2) \approx 0.2240
$$

---

## 5. Final Summary

- Model: **Poisson distribution**  
- Random variable:

$$
X = \text{number of error reports in one hour}
$$

- Probability distribution:

$$
P(X = k) = \frac{3^k e^{-3}}{k!}
$$

- Parameter:

$$
\lambda = 3
$$

---

## ✅ Key Insight

- The Poisson model is used for **counting events over time**
- Events occur:
  - independently  
  - at a constant average rate  
- The parameter \( \lambda \) is the **average rate of occurrence**
