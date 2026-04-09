# Task 2 — Permutations

---

### **Problem 1: Arranging 8 different books on a shelf**

- **Analysis:**  
  - Using **all objects** (8 books)  
  - Order matters  
  - No repetitions  

- **Model:** Permutation  

- **Solution:**  

$$
P_8 =
8! \\
= 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 \\
= 40,320
$$

- **Explanation:** Each position on the shelf can be filled by any remaining book. Multiply the choices for each position to get the total number of arrangements.

---

### **Problem 2: 8 people in a row if two particular people must sit next to each other**

- **Analysis:**  
  - Treat the two people who must sit together as **one block**  
  - Now we have 7 objects (6 people + 1 block)  
  - Order matters  
  - Inside the block, the two people can switch positions  

- **Model:** Permutation with a block  

- **Solution:**  

$$
\text{Ways to arrange 7 objects} =
7! \\
= 5040
$$

$$
\text{Ways to arrange 2 people inside the block} =
2! \\
= 2
$$

$$
\text{Total arrangements} =
7! \cdot 2! \\
= 5040 \cdot 2 \\
= 10,080
$$

- **Explanation:** We treat the two people as one object first, then account for the two possible orders within that block.

---

### **Problem 3: 8 people in a row if the two particular people must NOT sit next to each other**

- **Analysis:**  
  - First, calculate **total arrangements without restriction** → 8!  
  - Subtract arrangements where the two are together (from Problem 2 → 10,080)  

- **Solution:**  

$$
\text{Total arrangements without restriction} =
8! \\
= 40,320
$$

$$
\text{Arrangements where 2 people sit together} =
10,080
$$

$$
\text{Arrangements where 2 people do NOT sit together} =
8! - (7! \cdot 2!) \\
= 40,320 - 10,080 \\
= 30,240
$$

- **Explanation:** Subtract the restricted cases from the total to find the allowed arrangements.

---

### **Problem 4: Ordering 10 questions in a test if the first question is fixed**

- **Analysis:**  
  - First question is fixed → only 9 questions left  
  - Order matters  
  - No repetition  

- **Model:** Permutation of remaining objects  

- **Solution:**  

$$
\text{Ways to order remaining 9 questions} =
9! \\
= 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 \\
= 362,880
$$

- **Explanation:** With the first question fixed, we only need to arrange the remaining 9 questions.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 8 books on a shelf | Permutation | $P_8 = 8!$ | 40,320 |
| 8 people together (2 must sit together) | Permutation with block | $7! \cdot 2!$ | 10,080 |
| 8 people apart (2 must NOT sit together) | Subtraction | $8! - 7! \cdot 2!$ | 30,240 |
| 10 questions, first fixed | Permutation of remaining | $9!$ | 362,880 |
