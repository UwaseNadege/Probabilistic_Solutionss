# Task 7 — k-Permutations (Ordered Selections Without Repetition)

---

### **Problem 1: Assigning first three places among 12 runners**

- **Analysis:**  
  - Total runners = 12  
  - Assign **1st, 2nd, 3rd place** → order matters  
  - No repetition → each runner can only occupy one place  

- **Model:** k-Permutation  

- **Solution:**  

$$
P(12,3) =
\frac{12!}{(12-3)!} \\
= \frac{12!}{9!} \\
= 12 \cdot 11 \cdot 10 \\
= 1,320
$$

- **Explanation:** We pick 3 runners in order: 12 choices for 1st, 11 for 2nd, 10 for 3rd.

---

### **Problem 2: 4-digit numbers with distinct digits from 1–9**

- **Analysis:**  
  - Digits available: 1–9 → 9 digits  
  - Length = 4 digits → order matters  
  - No repetition → each digit can only appear once  

- **Model:** k-Permutation  

- **Solution:**  

$$
P(9,4) =
\frac{9!}{(9-4)!} \\
= \frac{9!}{5!} \\
= 9 \cdot 8 \cdot 7 \cdot 6 \\
= 3,024
$$

- **Explanation:** Pick digits one by one: 9 choices for first, 8 for second, 7 for third, 6 for fourth.

---

### **Problem 3: 4-digit numbers divisible by 5**

- **Analysis:**  
  - 4-digit number divisible by 5 → **last digit must be 5**  
  - Remaining 3 digits chosen from 1–9 excluding 5 → 8 digits  
  - Order matters → 3-permutation from 8 digits  

- **Model:** k-Permutation with fixed element  

- **Solution:**  

$$
P(8,3) =
\frac{8!}{(8-3)!} \\
= \frac{8!}{5!} \\
= 8 \cdot 7 \cdot 6 \\
= 336
$$

- **Explanation:** Fix the last digit as 5, then arrange the remaining 3 digits in order.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 12 runners, 1st–3rd place | k-Permutation | $P(12,3)$ | 1,320 |
| 4-digit numbers from 1–9 | k-Permutation | $P(9,4)$ | 3,024 |
| 4-digit numbers divisible by 5 | k-Permutation w/ fixed last digit | $P(8,3)$ | 336 |
