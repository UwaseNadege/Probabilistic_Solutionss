# Task 6 — Binomial Model

## Introduction
We analyze a process using the **binomial distribution**, where:

- Each part is either defective or not defective  
- The probability of a defective part is constant  
- Each inspection is independent  

We are given:

- Probability of defect:

$$
p = 0.04
$$

- Number of inspections:

$$
n = 10
$$

---

## 1. Random Variable

Let:

X = number of defective parts among 10 inspected parts  

Then:

$$
X \sim \text{Binomial}(n = 10,\ p = 0.04)
$$

---

## 2. Probability Formula

$$
P(X = k) = \binom{10}{k} (0.04)^k (0.96)^{10-k}
$$

---

## 3. Probability That Exactly 2 Parts Are Defective

We compute:

$$
P(X = 2) = \binom{10}{2} (0.04)^2 (0.96)^8
$$

---

### Step-by-Step Calculation

$$
\binom{10}{2} = 45
$$

$$
(0.04)^2 = 0.0016
$$

$$
(0.96)^8 \approx 0.7208
$$

---

### Final Result

$$
P(X = 2) = 45 \cdot 0.0016 \cdot 0.7208
$$

$$
P(X = 2) \approx 0.0519
$$

---

## 4. Probability That At Least One Part Is Defective

We use the complement rule:

$$
P(X \geq 1) = 1 - P(X = 0)
$$

---

### Step 1 — Compute \( P(X = 0) \)

$$
P(X = 0) = \binom{10}{0} (0.04)^0 (0.96)^{10}
$$

$$
P(X = 0) = (0.96)^{10}
$$

$$
P(X = 0) \approx 0.6650
$$

---

### Step 2 — Final Result

$$
P(X \geq 1) = 1 - 0.6650
$$

$$
P(X \geq 1) \approx 0.3350
$$

---

## 5. Final Answers

$$
P(X = 2) \approx 0.0519
$$

$$
P(X \geq 1) \approx 0.3350
$$

---

## ✅ Key Insight

- The binomial model is used for **fixed number of independent trials**
- The complement rule simplifies calculations:

$$
P(\text{at least one}) = 1 - P(0)
$$
