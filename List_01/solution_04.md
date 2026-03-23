# Task 4 — Circular Permutations

---

### **Problem 1: 7 people sitting around a round table**

- **Analysis:**  
  - 7 people arranged in a **circle**  
  - Rotations are considered the **same arrangement**, so we use **circular permutation**  
  - Formula: $(n-1)!$  

- **Model:** Circular Permutation  

- **Solution:**  

$$
P_\text{circle} =
(7-1)! \\
= 6! \\
= 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 \\
= 720
$$

- **Explanation:** In a circle, fixing one position removes rotational duplicates, so we arrange the remaining 6 people normally.

---

### **Problem 2: 7 people sitting with 2 particular people next to each other**

- **Analysis:**  
  - Treat the 2 people who must sit together as **one block** → 6 objects (5 individuals + 1 block)  
  - Order matters within the block → 2! ways  

- **Model:** Circular permutation with a block  

- **Solution:**  

$$
\text{Ways to arrange 6 objects in a circle} =
(6-1)! \\
= 5! \\
= 120
$$

$$
\text{Ways to arrange 2 people inside the block} =
2! \\
= 2
$$

$$
\text{Total arrangements} =
5! \cdot 2! \\
= 120 \cdot 2 \\
= 240
$$

- **Explanation:** The block reduces the circle to 6 objects, then we multiply by the internal arrangements of the block.

---

### **Problem 3: 7 people sitting with 2 particular people opposite each other**

- **Analysis:**  
  - Fix one of the two particular people at any seat (rotation irrelevant)  
  - The other person must sit directly opposite → 1 choice  
  - Remaining 5 people can sit in the remaining 5 seats → $(5-1)! = 4!$ circular arrangements  

- **Model:** Circular permutation with fixed positions  

- **Solution:**  

$$
\text{Ways to arrange remaining 5 people in circle} =
(5-1)! \\
= 4! \\
= 24
$$

$$
\text{Total arrangements including 2 opposite people} =
24 \cdot 1 \\
= 24
$$

- **Explanation:** By fixing one person and placing the other opposite, the rest are arranged normally in the remaining seats.

---

## ✅ Quick Summary Table

| Problem | Model | Formula | Result |
|---------|-------|---------|--------|
| 7 people around a table | Circular Permutation | $(7-1)!$ | 720 |
| 2 people must sit together | Circular Perm. with block | $(6-1)! \cdot 2!$ | 240 |
| 2 people opposite each other | Circular Perm. with fixed positions | $4! \cdot 1$ | 24 |
