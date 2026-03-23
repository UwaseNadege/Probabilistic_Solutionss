# Task 3 — Permutations with Repeated Elements

---

### **Problem 1: Distinct arrangements of the word MISSISSIPPI**

- **Analysis:**  
  - Total letters = 11  
  - Letter counts: M=1, I=4, S=4, P=2  
  - Some letters **repeat**, so we need **permutation with repeated elements**  

- **Model:** Permutation with repeated elements  

- **Solution:**  

$$
\text{Number of arrangements} =
\frac{11!}{1! \cdot 4! \cdot 4! \cdot 2!}
$$

$$
= \frac{39,916,800}{24 \cdot 24 \cdot 2}
$$

$$
= \frac{39,916,800}{1,152}
$$

$$
= 34,650
$$

- **Explanation:** Divide the total factorial by the factorial of each repeated letter to avoid counting identical arrangements multiple times.

---

### **Problem 2: Distinct arrangements of STATISTICS**

- **Analysis:**  
  - Total letters = 10  
  - Letter counts: S=3, T=3, A=1, I=2, C=1  
  - Letters repeat → permutation with repeated elements  

- **Model:** Permutation with repeated elements  

- **Solution:**  

$$
\text{Number of arrangements} =
\frac{10!}{3! \cdot 3! \cdot 1! \cdot 2! \cdot 1!}
$$

$$
= \frac{3,628,800}{6 \cdot 6 \cdot 1 \cdot 2 \cdot 1}
$$

$$
= \frac{3,628,800}{72}
$$

$$
= 50,400
$$

- **Explanation:** Divide the total factorial by the factorial of each repeated letter to account for identical letters.

---

### **Problem 3: Arrangements of STATISTICS starting with S**

- **Analysis:**  
  - First letter is fixed as S → remaining letters = 9 letters  
  - Remaining counts: S=2, T=3, A=1, I=2, C=1  
  - Use permutation with repeated elements for the remaining letters  

- **Model:** Permutation with repeated elements  

- **Solution:**  

$$
\text{Number of arrangements} =
\frac{9!}{2! \cdot 3! \cdot 1! \cdot 2! \cdot 1!}
$$

$$
= \frac{362,880}{2 \cdot 6 \cdot 1 \cdot 2 \cdot 1}
$$

$$
= \frac{362,880}{24}
$$

$$
= 15,120
$$

- **Explanation:** Fixing the first letter reduces the total number of letters by 1, then we use the same formula for repeated letters.
