# Task 8 — Sequences with Repetition

---

### **Problem 1: 5-digit PIN codes with digits that may repeat**

- **Analysis:**  
  - Digits available: 0–9 → 10 digits  
  - Length of sequence = 5  
  - Repetition allowed → each position can independently take any digit  

- **Model:** Sequence with Repetition  

- **Solution:**  

$$
\text{Total PIN codes} =
10^5 \\
= 10 \cdot 10 \cdot 10 \cdot 10 \cdot 10 \\
= 100,000
$$

- **Explanation:** Each of the 5 positions has 10 choices; multiply them together.

---

### **Problem 2: PIN codes containing at least one repeated digit**

- **Analysis:**  
  - Easier to use **complement principle**  
  - Total PIN codes without restriction → 10^5 = 100,000  
  - PIN codes with **all digits different** → 10P5  

- **Model:** Sequence with Repetition (complement principle)  

- **Solution:**  

$$
10P5 =
\frac{10!}{(10-5)!} \\
= \frac{10!}{5!} \\
= 10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \\
= 30,240
$$

$$
\text{PIN codes with at least one repeated digit} =
10^5 - 10P5 \\
= 100,000 - 30,240 \\
= 69,760
$$

- **Explanation:** Subtract the sequences with all unique digits from total sequences to find those with repeats.

---

### **Problem 3: PIN codes with all digits different**

- **Analysis:**  
  - Digits 0–9 → choose 5 distinct digits  
  - Order matters → 5-permutation of 10 digits  

- **Model:** k-Permutation  

- **Solution:**  

$$
10P5 =
\frac{10!}{(10-5)!} \\
= \frac{10!}{5!} \\
= 30,240
$$

- **Explanation:** Each position gets a unique digit; multiply the number of choices sequentially.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 5-digit PIN codes, repetition allowed | Sequence with Repetition | $10^5$ | 100,000 |
| At least one repeated digit | Sequence w/ repetition (complement) | $10^5 - 10P5$ | 69,760 |
| All digits different | k-Permutation | $10P5$ | 30,240 |
