# Task 11 — Modeling Outcomes

---

### **1. Distinguishable vs Indistinguishable Objects**

**Box:** 4 red, 4 blue, 3 green → total 11 balls  

#### **(a) Balls of the same color indistinguishable**

- **Analysis:**  
  - Linear arrangements of 11 balls  
  - Some balls **identical** → use **permutation with repeated elements**  

- **Model:** Permutation with repeated elements  

- **Solution:**  

$$
\text{Arrangements} =
\frac{11!}{4! \cdot 4! \cdot 3!} \\
= \frac{39,916,800}{24 \cdot 24 \cdot 6} \\
= 11,650
$$

- **Explanation:** Divide by factorials of identical objects to avoid overcounting.

---

#### **(b) Every ball labeled individually**

- **Analysis:**  
  - All balls **distinguishable** → standard **permutation** of 11 objects  

- **Model:** Permutation  

- **Solution:**  

$$
11! = 39,916,800
$$

- **Explanation:** Each ball is unique → all arrangements counted separately.

---

#### **(c) Why the answers differ**

- Indistinguishable balls → multiple arrangements that are physically identical are counted as **one**  
- Distinguishable balls → each labeled ball counts as a unique outcome  

---

### **2. Recording Order vs Ignoring Order**

**Experiment:** Draw 3 balls without replacement from the same box  

#### **(a) Only set of colors recorded (order ignored)**

- **Analysis:**  
  - Outcomes depend only on **colors**, not sequence  
  - Use **combinations** of colors  

- **Model:** Combination  

- **Solution (example with 3 colors R, B, G):**  

- Possible color sets:  
  - 3 red, 0 blue, 0 green → C(4,3) = 4  
  - 2 red + 1 blue → C(4,2)*C(4,1) = 6*4 = 24  
  - 1 red + 1 blue + 1 green → C(4,1)*C(4,1)*C(3,1) = 4*4*3 = 48  
  - ...sum all possibilities  

- **Explanation:** Only the combination of colors matters → order ignored  

#### **(b) Sequence of colors recorded**

- **Analysis:**  
  - Outcomes distinguish sequences → **permutation of selected balls**  
  - Multiply by 3! for ordering of 3 selected balls  

- **Model:** k-Permutation  

- **Explanation:** Recording order increases total outcomes because different orders are now distinct.

---

### **3. PIN Code vs 4-digit Number**

#### **(a) 4-digit PIN code (digits 0–9, repetition allowed)**

- **Analysis:**  
  - Each position independent, digits may repeat → **sequence with repetition**  

- **Model:** Sequence with Repetition  

- **Solution:**  

$$
10^4 = 10,000
$$

- **Explanation:** 10 choices for each of 4 positions → multiply.

---

#### **(b) 4-digit numbers (first digit ≠ 0, repetition allowed)**

- **Analysis:**  
  - First digit: 1–9 → 9 choices  
  - Other 3 digits: 0–9 → 10 choices each  

- **Model:** Sequence with restrictions  

- **Solution:**  

$$
9 \cdot 10^3 = 9,000
$$

- **Explanation:** First digit cannot be 0 → reduces total outcomes.

---

#### **(c) Why counting rules differ**

- PIN code: all positions equally allowed, repetition OK → total = 10^4  
- 4-digit number: first digit restricted → total = 9·10^3  

#### **(d) Why 1234 ≠ 4321**

- Order matters → sequences with same digits in different order are **distinct outcomes**  

---

## ✅ Quick Summary Table

| Concept | Model | Formula / Reasoning | Result |
|---------|-------|-------------------|--------|
| Indistinguishable balls | Perm. w/ repeated | $11!/(4!4!3!)$ | 11,650 |
| Distinguishable balls | Permutation | $11!$ | 39,916,800 |
| 3 balls, colors only | Combination | sum of C(counts) | depends on color choice |
| 3 balls, order recorded | k-Permutation | multiply by ordering | larger than combination |
| 4-digit PIN | Sequence w/ repetition | $10^4$ | 10,000 |
| 4-digit number, 1st ≠ 0 | Sequence w/ restriction | $9 \cdot 10^3$ | 9,000 |
