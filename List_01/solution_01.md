# Task List 02 — Combinatorics for Probability (Step-by-Step Solutions)

## Introduction

Many probability problems start by counting outcomes: the size of a sample space, the number of favorable outcomes, or the number of possible codes or arrangements.  
The main difficulty is usually **not the formula, but recognizing which counting model applies**.

**Key Questions to Identify the Model:**

1. Does order matter?  
2. Are we using all objects or only some of them?  
3. Are repetitions allowed?  
4. Are objects distinguishable or indistinguishable?  
5. What kind of outcome are we describing? (set, sequence, linear arrangement, circular arrangement)

---

## Useful Formulas and Models

1. **Permutation (all objects, order matters, no repetition):**  

$$
P_n = n!
$$

2. **Circular Permutation (objects arranged in a circle):**  

$$
P_\text{circle} = (n-1)!
$$

3. **Combination (unordered selection of some objects, no repetition):**  

$$
C(n,k) =
\frac{n!}{k!(n-k)!}
$$

4. **k-Permutation (ordered selection of some objects, no repetition):**  

$$
P(n,k) =
\frac{n!}{(n-k)!}
$$

5. **Sequence with Repetition (ordered selection with repetition allowed):**  

$$
n^k
$$

6. **Permutation with Repeated Elements (some objects identical):**  

$$
\text{Number of arrangements} =
\frac{n!}{n_1! \, n_2! \, \dots \, n_r!}
$$

---

## Task 1 — Recognizing Counting Models

For each situation, determine which combinatorial model is most appropriate and calculate if needed.

---

### **Problem 1: Arranging 7 students in a line**

- **Analysis:**  
  - Using **all objects** (7 students)  
  - Order matters  
  - No repetitions  

- **Model:** Permutation  

- **Solution:**  

$$
P_7 =
7! \\
= 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 \\
= 5040
$$

---

### **Problem 2: Choosing 4 members of a committee from 12 people**

- **Analysis:**  
  - Using **only some objects** (4 out of 12)  
  - Order does **not** matter  
  - No repetition  

- **Model:** Combination  

- **Solution:**  

$$
C(12,4) =
\frac{12!}{4!(12-4)!} \\
= \frac{12!}{4! \cdot 8!} \\
= 495
$$

---

### **Problem 3: Assigning gold, silver, and bronze medals among 15 athletes**

- **Analysis:**  
  - Using **only some objects** (3 out of 15)  
  - Order matters (gold ≠ silver ≠ bronze)  
  - No repetition  

- **Model:** k-Permutation  

- **Solution:**  

$$
P(15,3) =
\frac{15!}{(15-3)!} \\
= \frac{15!}{12!} \\
= 2730
$$

---

### **Problem 4: Forming a 6-digit PIN code**

- **Analysis:**  
  - Using **only some objects** (digits 0–9, total 10)  
  - Order matters  
  - Repetition allowed  

- **Model:** Sequence with Repetition  

- **Solution:**  

$$
\text{Number of PIN codes} =
10^6 \\
= 1,000,000
$$

---

### **Problem 5: Arranging the letters of the word BANANA**

- **Analysis:**  
  - Using **all objects** (letters of BANANA)  
  - Order matters  
  - Some objects identical (A×3, N×2, B×1)  

- **Model:** Permutation with Repeated Elements  

- **Solution:**  

$$
\text{Number of arrangements} =
\frac{6!}{3! \cdot 2! \cdot 1!} \\
= \frac{720}{6 \cdot 2} \\
= 60
$$

---

### **Problem 6: Seating 6 people around a round table**

- **Analysis:**  
  - Using **all objects** (6 people)  
  - Arranged in a circle  
  - Order matters relative to others  

- **Model:** Circular Permutation  

- **Solution:**  

$$
P_\text{circle} =
(6-1)! \\
= 5! \\
= 120
$$

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 7 students in a line | Permutation | $P_7 = 7!$ | 5040 |
| 4-member committee | Combination | $C(12,4) = \frac{12!}{4! \cdot 8!}$ | 495 |
| Medals among 15 athletes | k-Permutation | $P(15,3) = \frac{15!}{12!}$ | 2730 |
| 6-digit PIN | Sequence w/ repetition | $10^6$ | 1,000,000 |
| Letters of BANANA | Perm. w/ repeated | $\frac{6!}{3! \cdot 2! \cdot 1!}$ | 60 |
| 6 people at round table | Circular Permutation | $(6-1)!$ | 120 |
