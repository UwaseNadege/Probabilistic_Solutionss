# Task 9 — Digit Restrictions

---

### **Problem 1: Total 5-digit numbers**

- **Analysis:**  
  - 5-digit numbers → first digit cannot be 0 → choices for first digit = 1–9 = 9  
  - Remaining 4 digits → each can be 0–9 → 10 choices each  
  - Repetition allowed  

- **Model:** Sequence with Repetition  

- **Solution:**  

$$
\text{Total 5-digit numbers} =
9 \cdot 10 \cdot 10 \cdot 10 \cdot 10 \\
= 9 \cdot 10^4 \\
= 90,000
$$

- **Explanation:** Multiply choices for each position; first digit cannot be 0.

---

### **Problem 2: 5-digit numbers that are even**

- **Analysis:**  
  - Last digit must be even → choices = 0,2,4,6,8 → 5 choices  
  - First digit: 1–9 → 9 choices  
  - Middle 3 digits: 0–9 → 10 choices each  

- **Solution:**  

$$
\text{Even numbers} =
9 \cdot 10 \cdot 10 \cdot 10 \cdot 5 \\
= 9 \cdot 10^3 \cdot 5 \\
= 45,000
$$

- **Explanation:** First digit cannot be 0, last digit must be even; multiply choices for middle digits.

---

### **Problem 3: 5-digit numbers with no repeated digits**

- **Analysis:**  
  - First digit: 1–9 → 9 choices  
  - Second digit: 0–9 except first digit → 9 choices  
  - Third digit: 8 choices  
  - Fourth digit: 7 choices  
  - Fifth digit: 6 choices  

- **Solution:**  

$$
\text{No repeated digits} =
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 \\
= 27,216
$$

- **Explanation:** Sequentially choose each digit without repetition.

---

### **Problem 4: 5-digit numbers with at least one repeated digit**

- **Analysis:**  
  - Use **complement principle**  
  - Total 5-digit numbers = 90,000  
  - Numbers with all digits different = 27,216  
  - Subtract to get numbers with at least one repeat  

- **Solution:**  

$$
\text{At least one repeated digit} =
90,000 - 27,216 \\
= 62,784
$$

- **Explanation:** Subtract the count of numbers with all unique digits from total numbers.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| Total 5-digit numbers | Sequence w/ restriction | $9 \cdot 10^4$ | 90,000 |
| 5-digit even numbers | Sequence w/ restriction | $9 \cdot 10^3 \cdot 5$ | 45,000 |
| No repeated digits | Sequence w/o repetition | $9 \cdot 9 \cdot 8 \cdot 7 \cdot 6$ | 27,216 |
| At least one repeated digit | Complement | $90,000 - 27,216$ | 62,784 |
