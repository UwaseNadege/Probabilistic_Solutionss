# Task 6 — Combinations in Card Problems

---

### **Problem 1: 5 cards with exactly 2 hearts**

- **Analysis:**  
  - Standard deck: 52 cards → 13 hearts, 39 non-hearts
  - A 5-card hand with exactly 2 hearts must have: 2 hearts
the remaining 3 cards must NOT be hearts
  - Choose **2 hearts from 13** → C(13,2)  
  - Choose **3 non-hearts from 39** → C(39,3)  
  - Multiply the two numbers → independent selections  

- **Model:** Combination  

- **Solution:**  

$$
C(13,2) =
\frac{13!}{2! (13-2)!} \\
= \frac{13!}{2! \cdot 11!} \\
= 78
$$

$$
C(39,3) =
\frac{39!}{3! (39-3)!} \\
= \frac{39!}{3! \cdot 36!} \\
= 9,139
$$

$$
\text{Total hands} =
C(13,2) \cdot C(39,3) \\
= 78 \cdot 9,139 \\
= 713,982
$$

- **Explanation:** Select hearts and non-hearts independently, then multiply to get total hands.

---

### **Problem 2: 5 cards with at least one heart**

- **Analysis:**  
  - Easier to use **complement principle**
  - We want the number of 5-card hands that contain **at least one heart**.

Instead of counting all possible cases (1 heart, 2 hearts, 3 hearts, etc.), it is much easier to use the **complement principle**.
First, count all possible 5-card hands from a standard 52-card deck:
  - Total 5-card hands: C(52,5)
  - Next, count the number of hands that contain **no hearts**.  
This means all 5 cards are chosen from the 39 non-heart cards:
  - Hands with **no hearts** → choose 5 from 39 non-hearts → C(39,5)
  - Subtract to get hands with at least one heart  

- **Solution:**  

$$
C(52,5) =
\frac{52!}{5! (52-5)!} \\
= 2,598,960
$$

$$
C(39,5) =
\frac{39!}{5! (39-5)!} \\
= 575,757
$$

$$
\text{Hands with at least 1 heart} =
C(52,5) - C(39,5) \\
= 2,598,960 - 575,757 \\
= 2,023,203
$$

- **Explanation:** Subtract the “no hearts” cases from the total to get “at least one heart.”

---

### **Problem 3: 5 cards with no face cards (J, Q, K)**

- **Analysis:**  
  - There are **12 face cards** in the deck → 52-12=40 non-face cards  
  - Choose 5 cards from these 40  

- **Model:** Combination  

- **Solution:**  

$$
C(40,5) =
\frac{40!}{5! (40-5)!} \\
= \frac{40!}{5! \cdot 35!} \\
= 658,008
$$

- **Explanation:** Only choose from non-face cards; order does not matter.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| Exactly 2 hearts | Combination | $C(13,2) \cdot C(39,3)$ | 713,982 |
| At least 1 heart | Combination (complement) | $C(52,5) - C(39,5)$ | 2,023,203 |
| No face cards | Combination | $C(40,5)$ | 658,008 |
