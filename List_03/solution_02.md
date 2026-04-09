# Task 2 — Hypergeometric Model (Sampling from a Batch)

## Introduction
We analyze a sampling process using the **hypergeometric distribution**, where elements are drawn **without replacement** from a finite population.

We are given:

- Total components: 20  
- Defective components: 5  
- Functional components: 15  
- Sample size: 4  

---

## 1. Random Experiment

We randomly select 4 components without replacement from a batch of 20.

Each selected component can be:

- Defective (D)  
- Functional (F)  

---

## 2. Random Variable

Let:

X = number of defective components in the sample of 4  

---

## 3. Possible Values of X

X ∈ {0, 1, 2, 3, 4}

---

## 4. Probability Distribution

The hypergeometric probability formula is:

$$
P(X = k) = \frac{\binom{5}{k} \binom{15}{4-k}}{\binom{20}{4}}
$$

---

### Step 1 — Total Number of Samples

$$
\binom{20}{4} = 4845
$$

---

### Step 2 — Compute Each Probability

#### **P(X = 0)**

$$
P(X = 0) = \frac{\binom{5}{0} \binom{15}{4}}{\binom{20}{4}}
$$

$$
= \frac{1 \cdot 1365}{4845}
$$

$$
= \frac{1365}{4845} \approx 0.2817
$$

---

#### **P(X = 1)**

$$
P(X = 1) = \frac{\binom{5}{1} \binom{15}{3}}{\binom{20}{4}}
$$

$$
= \frac{5 \cdot 455}{4845}
$$

$$
= \frac{2275}{4845} \approx 0.4696
$$

---

#### **P(X = 2)**

$$
P(X = 2) = \frac{\binom{5}{2} \binom{15}{2}}{\binom{20}{4}}
$$

$$
= \frac{10 \cdot 105}{4845}
$$

$$
= \frac{1050}{4845} \approx 0.2167
$$

---

#### **P(X = 3)**

$$
P(X = 3) = \frac{\binom{5}{3} \binom{15}{1}}{\binom{20}{4}}
$$

$$
= \frac{10 \cdot 15}{4845}
$$

$$
= \frac{150}{4845} \approx 0.0310
$$

---

#### **P(X = 4)**

$$
P(X = 4) = \frac{\binom{5}{4} \binom{15}{0}}{\binom{20}{4}}
$$

$$
= \frac{5 \cdot 1}{4845}
$$

$$
= \frac{5}{4845} \approx 0.0010
$$

---

## 5. Definition of Success

Success = selecting a defective component

---

## 6. Final Summary

- Model: Hypergeometric distribution  
- Population size: 20  
- Defective elements: 5  
- Sample size: 4  

---

### Final Probability Distribution

$$
P(X = 0) \approx 0.2817
$$

$$
P(X = 1) \approx 0.4696
$$

$$
P(X = 2) \approx 0.2167
$$

$$
P(X = 3) \approx 0.0310
$$

$$
P(X = 4) \approx 0.0010
$$

---

## ✅ Key Insight

Unlike the binomial model:

- The probability changes after each draw  
- Because sampling is done **without replacement**
