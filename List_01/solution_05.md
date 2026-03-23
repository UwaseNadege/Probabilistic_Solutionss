# Task 5 — Combinations

---

### **Problem 1: Choosing 4 people from 12 students**

- **Analysis:**  
  - Selecting **some objects** (4 out of 12)  
  - Order does **not matter**  
  - No repetition  

- **Model:** Combination  

- **Solution:**  

$$
C(12,4) =
\frac{12!}{4! (12-4)!} \\
= \frac{12!}{4! \cdot 8!} \\
= \frac{479,001,600}{24 \cdot 40,320} \\
= 495
$$

- **Explanation:** We divide by 4! to remove ordering within the chosen group, leaving only the combinations.

---

### **Problem 2: Committees containing a particular student**

- **Analysis:**  
  - Fix the **particular student** in the committee → 1 choice  
  - Choose the remaining 3 members from the other 11 students → C(11,3)  

- **Solution:**  

$$
C(11,3) =
\frac{11!}{3! (11-3)!} \\
= \frac{11!}{3! \cdot 8!} \\
= \frac{39,916,800}{6 \cdot 40,320} \\
= 165
$$

- **Explanation:** By fixing the student, we reduce the problem to choosing 3 more from the remaining students.

---

### **Problem 3: Committees containing at least one of two particular students**

- **Analysis:**  
  - Total combinations without restriction → C(12,4) = 495  
  - Subtract committees with **neither student** → choose 4 from remaining 10 → C(10,4)  

- **Solution:**  

$$
C(10,4) =
\frac{10!}{4! (10-4)!} \\
= \frac{10!}{4! \cdot 6!} \\
= 210
$$

$$
\text{Committees with at least one of the two students} =
C(12,4) - C(10,4) \\
= 495 - 210 \\
= 285
$$

- **Explanation:** Using **complement principle** makes it easier to count “at least one” cases.

---

### **Problem 4: Committees containing exactly two women (7 men, 5 women)**

- **Analysis:**  
  - Choose **2 women from 5** → C(5,2)  
  - Choose **2 men from 7** → C(7,2)  
  - Multiply the choices → combination of women × combination of men  

- **Solution:**  

$$
C(5,2) =
\frac{5!}{2! (5-2)!} \\
= \frac{5!}{2! \cdot 3!} \\
= 10
$$

$$
C(7,2) =
\frac{7!}{2! (7-2)!} \\
= \frac{7!}{2! \cdot 5!} \\
= 21
$$

$$
\text{Total committees} =
C(5,2) \cdot C(7,2) \\
= 10 \cdot 21 \\
= 210
$$

- **Explanation:** Choose the women and men independently, then multiply to get total combinations.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 4 people from 12 | Combination | $C(12,4)$ | 495 |
| Containing 1 particular student | Combination | $C(11,3)$ | 165 |
| Containing at least one of 2 students | Combination (complement) | $C(12,4)-C(10,4)$ | 285 |
| Exactly 2 women (7 men, 5 women) | Combination | $C(5,2) \cdot C(7,2)$ | 210 |
