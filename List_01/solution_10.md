# Task 10 — Urn Models

---

### **Problem 1: Three balls drawn without replacement, order ignored**

- **Analysis:**  
  - Total balls = 5 red + 4 blue + 3 green = 12  
  - Draw 3 balls **without replacement**  
  - Order **does not matter** → combination  

- **Model:** Combination  

- **Solution:**  

$$
C(12,3) =
\frac{12!}{3! (12-3)!} \\
= \frac{12!}{3! \cdot 9!} \\
= 220
$$

- **Explanation:** Choose any 3 balls from 12 regardless of order.

---

### **Problem 2: Samples containing exactly two red balls**

- **Analysis:**  
  - Choose 2 red balls from 5 → C(5,2)  
  - Choose 1 ball from remaining non-red balls (4 blue + 3 green = 7) → C(7,1)  
  - Multiply → independent choices  

- **Solution:**  

$$
C(5,2) =
\frac{5!}{2! (5-2)!} = 10
$$

$$
C(7,1) =
\frac{7!}{1! (7-1)!} = 7
$$

$$
\text{Total samples} = C(5,2) \cdot C(7,1) = 10 \cdot 7 = 70
$$

- **Explanation:** Pick red balls first, then choose one non-red ball; multiply to get total combinations.

---

### **Problem 3: Three balls drawn, order recorded**

- **Analysis:**  
  - Order **matters** → sequence  
  - Total balls = 12 → 3 positions  
  - No replacement → 12 choices for first, 11 for second, 10 for third  

- **Model:** k-Permutation  

- **Solution:**  

$$
P(12,3) =
\frac{12!}{(12-3)!} \\
= \frac{12!}{9!} \\
= 12 \cdot 11 \cdot 10 \\
= 1,320
$$

- **Explanation:** Each draw has fewer options as balls are removed; multiply sequentially.

---

### **Problem 4: Outcomes with exactly two red balls, order recorded**

- **Analysis:**  
  - First, choose **2 red balls** from 5 → C(5,2)  
  - Choose **1 non-red ball** from 7 → C(7,1)  
  - Then **arrange the 3 balls in order** → 3! permutations  

- **Solution:**  

$$
C(5,2) = 10
$$

$$
C(7,1) = 7
$$

$$
\text{Arrange 3 balls} = 3! = 6
$$

$$
\text{Total outcomes} = 10 \cdot 7 \cdot 6 = 420
$$

- **Explanation:** Count all ways to select balls, then account for order of selection.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 3 balls, order ignored | Combination | $C(12,3)$ | 220 |
| Exactly 2 red balls | Combination | $C(5,2) \cdot C(7,1)$ | 70 |
| 3 balls, order recorded | k-Permutation | $P(12,3)$ | 1,320 |
| Exactly 2 red balls, order recorded | k-Permutation w/ selection | $C(5,2) \cdot C(7,1) \cdot 3!$ | 420 |
