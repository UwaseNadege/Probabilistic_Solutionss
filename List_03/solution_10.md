# Task 10 — Multinomial Model

## Introduction
We analyze a process using the **multinomial distribution**, which generalizes the binomial model to more than two possible outcomes.

We are given:

- Strawberry probability:

$$
p_1 = 0.4
$$

- Lemon probability:

$$
p_2 = 0.35
$$

- Mint probability:

$$
p_3 = 0.25
$$

- Number of selections:

$$
n = 6
$$

---

## 1. Random Experiment

We perform **6 independent selections with replacement**, where each selection results in one of three outcomes:

- Strawberry  
- Lemon  
- Mint  

---

## 2. Random Variable

Let:

- \( X_1 \) = number of strawberry candies  
- \( X_2 \) = number of lemon candies  
- \( X_3 \) = number of mint candies  

with the constraint:

$$
X_1 + X_2 + X_3 = 6
$$

---

## 3. Multinomial Probability Formula

$$
P(X_1 = x_1,\ X_2 = x_2,\ X_3 = x_3)
= \frac{6!}{x_1! \, x_2! \, x_3!}
\cdot (0.4)^{x_1}
\cdot (0.35)^{x_2}
\cdot (0.25)^{x_3}
$$

---

## 4. Required Probability

We are asked to compute:

- 3 strawberry  
- 2 lemon  
- 1 mint  

So:

$$
x_1 = 3,\quad x_2 = 2,\quad x_3 = 1
$$

---

## 5. Step-by-Step Calculation

### Step 1 — Multinomial Coefficient

$$
\frac{6!}{3! \, 2! \, 1!}
$$

$$
6! = 720,\quad 3! = 6,\quad 2! = 2,\quad 1! = 1
$$

$$
\frac{720}{6 \cdot 2 \cdot 1} = \frac{720}{12} = 60
$$

---

### Step 2 — Probability Terms

$$
(0.4)^3 = 0.064
$$

$$
(0.35)^2 = 0.1225
$$

$$
(0.25)^1 = 0.25
$$

---

### Step 3 — Multiply All Terms

$$
P = 60 \cdot 0.064 \cdot 0.1225 \cdot 0.25
$$

$$
P = 60 \cdot 0.00196
$$

$$
P \approx 0.1176
$$

---

## 6. Final Answer

$$
P(3\ \text{strawberry},\ 2\ \text{lemon},\ 1\ \text{mint}) \approx 0.1176
$$

---

## ✅ Key Insight

- The multinomial model extends the binomial model to **multiple categories**
- The sum of probabilities must always equal 1:

$$
0.4 + 0.35 + 0.25 = 1
$$

- The multinomial coefficient counts how many ways the arrangement can occur
