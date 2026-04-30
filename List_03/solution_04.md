# Task 4 — Poisson Model (Arrival of Events)

## Introduction
We analyze a process using the Poisson distribution, which models the number of events occurring in a fixed interval of time or space.

We are given:

- Average number of error reports per hour:

$$
\lambda = 3
$$

- Events occur independently  
- The rate is constant over time  

---

## 1. Random Variable

Let:

$$
X = \text{number of error reports in one hour}
$$

Then:

$$
X \sim \text{Poisson}(\lambda = 3)
$$

---

## 2. Probability Formula

We model this using a Poisson distribution with:

$$
\lambda = 3
$$

The general formula is:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

## Example Calculations

### P(X = 0)

$$
P(X = 0) = \frac{3^0 e^{-3}}{0!}
$$

$$
= \frac{1 \cdot e^{-3}}{1}
= e^{-3}
$$

$$
\approx 0.0498
$$

---

### P(X = 1)

$$
P(X = 1) = \frac{3^1 e^{-3}}{1!}
$$

$$
= \frac{3 \cdot e^{-3}}{1}
= 3e^{-3}
$$

$$
\approx 0.1494
$$

---

### P(X = 2)

$$
P(X = 2) = \frac{3^2 e^{-3}}{2!}
$$

Step-by-step:

$$
3^2 = 9
$$

$$
2! = 2
$$

$$
P(X = 2) = \frac{9}{2} e^{-3}
$$

$$
\approx 4.5 \cdot 0.0498
$$

$$
\approx 0.2240
$$

---

## 3. Probability That Exactly 3 Error Reports Occur

We compute:

$$
P(X = 3) = \frac{3^3 e^{-3}}{3!}
$$

### Step-by-Step Calculation

$$
3^3 = 27
$$

$$
3! = 6
$$

$$
\frac{27}{6} = 4.5
$$

$$
P(X = 3) = 4.5 \cdot e^{-3}
$$

$$
\approx 4.5 \cdot 0.0498
$$

$$
\approx 0.2240
$$

---

## Final Answer

$$
P(X = 3) \approx 0.2240
$$
