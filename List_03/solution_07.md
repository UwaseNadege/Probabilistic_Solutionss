# Task 7 — Hypergeometric Model

## Introduction
We analyze a sampling process using the **hypergeometric distribution**, where items are selected **without replacement** from a finite population.

We are given:

- Total bulbs: 15  
- Working bulbs: 12  
- Defective bulbs: 3  
- Sample size: 5  

---

## 1. Random Experiment

We randomly select **5 bulbs without replacement** from a box of 15 bulbs.

Each bulb can be:

- Defective (D)  
- Working (W)  

---

## 2. Random Variable

Let:

X = number of defective bulbs in the sample of 5  

---

## 3. Probability Formula

The hypergeometric distribution formula is:

$$
P(X = k) = \frac{\binom{3}{k} \binom{12}{5-k}}{\binom{15}{5}}
$$

---

## 4. Calculate \( P(X = 2) \)

We substitute \( k = 2 \):

$$
P(X = 2) = \frac{\binom{3}{2} \binom{12}{3}}{\binom{15}{5}}
$$

---

### Step 1 — Compute Combinations

$$
\binom{3}{2} = 3
$$

$$
\binom{12}{3} = 220
$$

$$
\binom{15}{5} = 3003
$$

---

### Step 2 — Substitute Values

$$
P(X = 2) = \frac{3 \cdot 220}{3003}
$$

$$
P(X = 2) = \frac{660}{3003}
$$

---

### Step 3 — Final Result

$$
P(X = 2) \approx 0.2198
$$

---

## 5. Final Answer

$$
P(X = 2) \approx 0.2198
$$

---

## ✅ Key Insight

- The hypergeometric model is used when sampling is done **without replacement**
- The probability depends on the composition of the remaining population after each draw
