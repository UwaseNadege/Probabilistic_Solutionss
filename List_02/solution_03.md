# 📘 Task 3 — Geometric Model (Waiting for the First Event)

## Introduction
We analyze a process using the **geometric distribution**, where we observe repeated independent trials until the **first success** occurs.

We are given:

- Each page may contain an error with probability **p**
- Each page is independent
- The probability of error is the same for every page

---

## 1. Random Experiment

We observe consecutive printed pages until the **first printing error appears**.

Each page can be:

- Error (E)  
- No error (N)

We continue the process until the first occurrence of an error.

---

## 2. Sample Space

The sample space consists of all sequences where the **first error appears at some position**.

Examples:

- E  
- N E  
- N N E  
- N N N E  
- and so on...

---

### General Form of Sample Space

$$
\Omega = \{ E,\ NE,\ NNE,\ NNNE,\ \dots \}
$$

---

## 3. Random Variable

Let:

X = number of pages printed until the first error appears

---

## 4. Probability Distribution

The geometric distribution formula is:

$$
P(X = k) = (1 - p)^{k - 1} \cdot p
$$

---

### Explanation

- The first \( k - 1 \) pages have no error → probability \( (1 - p)^{k-1} \)  
- The \( k \)-th page contains the first error → probability \( p \)

---

## 5. Probability of Specific Values

### **P(X = 1)**

$$
P(X = 1) = p
$$

---

### **P(X = 2)**

$$
P(X = 2) = (1 - p)p
$$

---

### **P(X = 3)**

$$
P(X = 3) = (1 - p)^2 p
$$

---

### **P(X = k)**

$$
P(X = k) = (1 - p)^{k-1} p
$$

---

## 6. Definition of Success

In this model:

**Success = occurrence of a printing error**

Thus:

- Probability of success:
  
$$
P(\text{success}) = p
$$

- Probability of failure:
  
$$
P(\text{failure}) = 1 - p
$$

---

## 7. Final Summary

- Model: **Geometric distribution**  
- Random variable:  

$$
X = \text{number of trials until first success}
$$

- Probability distribution:

$$
P(X = k) = (1 - p)^{k - 1} p
$$

---

## ✅ Key Insight

- The process continues until the **first success occurs**
- Each trial is **independent**
- The probability of success remains **constant**
