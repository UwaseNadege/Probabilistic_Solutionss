# Task 5 — Multinomial Model (Categories of Outcomes)

## Introduction
We analyze a random experiment using the **multinomial distribution**, which generalizes the binomial model to more than two possible outcomes.

We are given:

- A die is rolled **5 times**
- Outcomes are grouped into 3 categories:
  - Small: (1–2)
  - Medium: (3–4)
  - Large: (5–6)

Each category has probability:

$$
P(\text{small}) = P(\text{medium}) = P(\text{large}) = \frac{1}{3}
$$

---

## 1. Random Experiment

We roll a die **5 times** and record how many times each category appears:

- Small numbers (1–2)  
- Medium numbers (3–4)  
- Large numbers (5–6)

Each roll is independent.

---

## 2. Sample Space

The sample space consists of all possible sequences of 5 outcomes, where each outcome belongs to one of the three categories.

Instead of listing all sequences, we describe outcomes by counts:

$$
\Omega = \{(x_1, x_2, x_3) \in \mathbb{N}_0^3 : x_1 + x_2 + x_3 = 5\}
$$

Where:

- \( x_1 \) = number of small outcomes  
- \( x_2 \) = number of medium outcomes  
- \( x_3 \) = number of large outcomes  

---

## 3. Multinomial Distribution

Let:

- \( X_1 \) = number of small outcomes  
- \( X_2 \) = number of medium outcomes  
- \( X_3 \) = number of large outcomes  

Then:

$$
(X_1, X_2, X_3) \sim \text{Multinomial}(n = 5; p_1, p_2, p_3)
$$

where:

$$
p_1 = \frac{1}{3}, \quad p_2 = \frac{1}{3}, \quad p_3 = \frac{1}{3}
$$

---

### Probability Formula

$$
P(X_1 = x_1, X_2 = x_2, X_3 = x_3)
= \frac{5!}{x_1! \, x_2! \, x_3!}
\left(\frac{1}{3}\right)^{x_1}
\left(\frac{1}{3}\right)^{x_2}
\left(\frac{1}{3}\right)^{x_3}
$$

---

### Simplified Form

Since all probabilities are equal:

$$
P(X_1, X_2, X_3)
= \frac{5!}{x_1! \, x_2! \, x_3!}
\left(\frac{1}{3}\right)^5
$$

---

## 4. Interpretation of Parameters

### \( n = 5 \)

- Number of trials (die rolls)

---

### \( p_1, p_2, p_3 \)

- Probabilities of each category:
  
$$
Small: \( \frac{1}{3} \)
Medium: \( \frac{1}{3} \)
Large: \( \frac{1}{3} \)
$$
  
---

### \( x_1, x_2, x_3 \)

- Counts of how many times each category occurs in 5 rolls

---

## 5. Example

Example outcome:

- 2 small numbers  
- 2 medium numbers  
- 1 large number  

So:

$$
(x_1, x_2, x_3) = (2, 2, 1)
$$

---

### Probability of this outcome:

$$
P(2,2,1) = \frac{5!}{2! \, 2! \, 1!} \left(\frac{1}{3}\right)^5
$$

$$
= \frac{120}{2 \cdot 2 \cdot 1} \cdot \frac{1}{243}
$$

$$
= 30 \cdot \frac{1}{243}
$$

$$
\approx 0.1235
$$

---

## 6. Final Summary

- Model: **Multinomial distribution**  
- Number of trials:

$$
n = 5
$$

- Categories:

$$
( \text{small}, \text{medium}, \text{large} )
$$

- Probabilities:

$$
\left(\frac{1}{3}, \frac{1}{3}, \frac{1}{3}\right)
$$

---

## ✅ Key Insight

- The multinomial distribution is a **generalization of the binomial distribution**
- It is used when each trial has **more than two possible outcomes**
- It counts how many times each category occurs
