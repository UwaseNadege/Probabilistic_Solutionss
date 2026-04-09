# Task 8 — Geometric Model

## Introduction
We analyze a process using the **geometric distribution**, where we repeat independent trials until the **first success** occurs.

We are given:

- Probability of error:

$$
p = 0.1
$$

- Probability of no error:

$$
1 - p = 0.9
$$

- Each compilation is independent

---

## 1. Random Variable

Let:

X = number of compilations until the first error occurs  

Then:

$$
X \sim \text{Geometric}(p = 0.1)
$$

---

## 2. Probability Formula

$$
P(X = k) = (1 - p)^{k - 1} p
$$

---

## 3. First Error Appears on the 4th Compilation

We compute:

$$
P(X = 4) = (0.9)^3 \cdot 0.1
$$

---

### Step-by-Step Calculation

$$
(0.9)^3 = 0.729
$$

$$
P(X = 4) = 0.729 \cdot 0.1
$$

$$
P(X = 4) = 0.0729
$$

---

## 4. First Error Appears No Later Than the 3rd Compilation

We compute:

$$
P(X \leq 3) = P(X = 1) + P(X = 2) + P(X = 3)
$$

---

### Step 1 — Compute Each Term

#### **P(X = 1)**

$$
P(X = 1) = 0.1
$$

---

#### **P(X = 2)**

$$
P(X = 2) = (0.9)(0.1) = 0.09
$$

---

#### **P(X = 3)**

$$
P(X = 3) = (0.9)^2 (0.1) = 0.081
$$

---

### Step 2 — Add Probabilities

$$
P(X \leq 3) = 0.1 + 0.09 + 0.081
$$

$$
P(X \leq 3) = 0.271
$$

---

## 5. Final Answers

$$
P(X = 4) = 0.0729
$$

$$
P(X \leq 3) = 0.271
$$

---

## ✅ Key Insight

- The geometric distribution models **waiting time until the first success**
- The probability decreases exponentially as the number of trials increases
- The complement can also be used for efficiency in calculations
