# Task 1 — Binomial Model (Quality Control)

## Introduction
We analyze a quality control process using the **binomial distribution**, where each trial has only two possible outcomes:

- Good screw (G)
- Defective screw (D)

We assume:

- Each inspection is **independent**
- The probability of a defective screw is **p**
- The probability of a good screw is **1 - p**

---

## 1. Random Experiment

We inspect **3 consecutive screws**.

Each screw can be:

- Defective (D)
- Good (G)

Thus, the experiment consists of observing the sequence of outcomes for 3 screws.

---

## 2. Sample Space

For one screw:

Ω₁ = {D, G}

For three screws:

Ω₃ = { (x₁, x₂, x₃) : xᵢ ∈ {D, G} }

---

### All Possible Outcomes

Ω₃ = {  
DDD, DDG, DGD, DGG,  
GDD, GDG, GGD, GGG  
}

---

### Number of Elementary Outcomes

|Ω₃| = 2³ = 8

---

## 3. Probabilities of Elementary Outcomes

Each sequence probability depends on:

- Number of defective screws → probability p  
- Number of good screws → probability (1 - p)

---

### General Formula

For a sequence with:

- k defective screws  
- (3 - k) good screws  

P(ω) = pᵏ (1 - p)^(3 - k)

---

### Explicit Probabilities

- **DDD**  
P(DDD) = p³  

- **DDG, DGD, GDD** (2 defective, 1 good)  
P = p² (1 - p)  

- **DGG, GDG, GGD** (1 defective, 2 good)  
P = p (1 - p)²  

- **GGG**  
P(GGG) = (1 - p)³  

---

## 4. Definition of Success

In this model:

**Success = selecting a defective screw**

Thus:

- P(success) = p  
- P(failure) = 1 - p  

---

## 5. Random Variable (Binomial Model)

Let:

X = number of defective screws in 3 trials  

Then:

X ~ Binomial(n = 3, p)

---

## 6. Probability Distribution (Final Answers)

The probability of exactly k defective screws:

P(X = k) = (3 choose k) pᵏ (1 - p)^(3 - k)

---

### Final Calculated Values

- **P(X = 0)**  
P(X = 0) = (1 - p)³  

- **P(X = 1)**  
P(X = 1) = 3p(1 - p)²  

- **P(X = 2)**  
P(X = 2) = 3p²(1 - p)  

- **P(X = 3)**  
P(X = 3) = p³  

---

## ✅ Summary

- Total outcomes: **8**  
- Model: **Binomial distribution**  
- Success: **defective screw**  
- Random variable:  

X ~ Binomial(3, p)
