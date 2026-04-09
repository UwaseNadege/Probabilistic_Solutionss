# Task 9 — Poisson Model

## Introduction
We analyze a process using the **Poisson distribution**, which models the number of events occurring in a fixed time interval.

We are given:

- Average number of requests per hour:

$$
\lambda = 5
$$

- Requests occur independently at a constant rate

---

## 1. Random Variable

Let:

X = number of requests received in one hour  

Then:

$$
X \sim \text{Poisson}(\lambda = 5)
$$

---

## 2. Probability Formula

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

## 3. Probability of Exactly 3 Requests

We compute:

$$
P(X = 3) = \frac{5^3 e^{-5}}{3!}
$$

---

### Step-by-Step Calculation

$$
5^3 = 125
$$

$$
3! = 6
$$

$$
P(X = 3) = \frac{125 e^{-5}}{6}
$$

$$
e^{-5} \approx 0.0067379
$$

---

### Final Result

$$
P(X = 3) = \frac{125 \cdot 0.0067379}{6}
$$

$$
P(X = 3) \approx 0.1404
$$

---

## 4. Probability of At Least One Request

We use the complement rule:

$$
P(X \geq 1) = 1 - P(X = 0)
$$

---

### Step 1 — Compute \( P(X = 0) \)

$$
P(X = 0) = \frac{5^0 e^{-5}}{0!} = e^{-5}
$$

$$
P(X = 0) \approx 0.0067379
$$

---

### Step 2 — Final Result

$$
P(X \geq 1) = 1 - 0.0067379
$$

$$
P(X \geq 1) \approx 0.9933
$$

---

## 5. Final Answers

$$
P(X = 3) \approx 0.1404
$$

$$
P(X \geq 1) \approx 0.9933
$$

---

## ✅ Key Insight

- The Poisson model is used for **counting events over time**
- The parameter:

$$
\lambda = 5
$$

represents the **average number of requests per hour**
- The complement rule is very useful:

$$
P(X \geq 1) = 1 - P(X = 0)
$$
