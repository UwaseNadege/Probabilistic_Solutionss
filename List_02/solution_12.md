# Task 12 — Mixed Counting Problem

---

## **1. Student ID Codes**

**Identifier:** 2 letters (A–E) + 3 digits (0–9)  

---

### **(a) Letters and digits may repeat**

- **Analysis:**  
  - Letters: 5 choices each → repetition allowed → 5^2  
  - Digits: 10 choices each → repetition allowed → 10^3  
  - Multiply letters × digits  

- **Model:** Sequence with Repetition  

- **Solution:**  

$$
\text{Total IDs} = 5^2 \cdot 10^3 \\
= 25 \cdot 1,000 \\
= 25,000
$$

---

### **(b) Letters may not repeat, digits may repeat**

- **Analysis:**  
  - Letters: 2-permutation of 5 → P(5,2)  
  - Digits: 10^3 → repetition allowed  

- **Model:** k-Permutation + Sequence with Repetition  

- **Solution:**  

$$
P(5,2) = \frac{5!}{(5-2)!} = \frac{120}{6} = 20
$$

$$
\text{Total IDs} = 20 \cdot 10^3 = 20,000
$$

---

### **(c) Neither letters nor digits may repeat**

- **Analysis:**  
  - Letters: 2-permutation of 5 → P(5,2) = 20  
  - Digits: 3-permutation of 10 → P(10,3)  

- **Solution:**  

$$
P(10,3) = \frac{10!}{7!} = 10 \cdot 9 \cdot 8 = 720
$$

$$
\text{Total IDs} = 20 \cdot 720 = 14,400
$$

---

## **2. Medal Assignment (12 runners, 3 medals)**

### **(a) Medals assigned freely**

- **Analysis:**  
  - 3 positions (gold, silver, bronze) → order matters  
  - 12 runners → no repetition  

- **Model:** k-Permutation  

- **Solution:**  

$$
P(12,3) = \frac{12!}{9!} = 12 \cdot 11 \cdot 10 = 1,320
$$

---

### **(b) Two particular runners must receive medals**

- **Analysis:**  
  - Casework: these 2 runners can occupy any **2 of 3 medals** → P(3,2) = 6 ways  
  - Remaining 1 medal → choose 1 of remaining 10 runners → 10 ways  

- **Solution:**  

$$
\text{Total assignments} = 6 \cdot 10 = 60
$$

---

## **3. Committee Selection (10 students, 6 men + 4 women)**

### **(a) Any 4-person committee**

- **Model:** Combination  

- **Solution:**  

$$
C(10,4) = \frac{10!}{4!6!} = 210
$$

---

### **(b) Committees with exactly 2 women**

- **Analysis:**  
  - Choose 2 women from 4 → C(4,2) = 6  
  - Choose 2 men from 6 → C(6,2) = 15  
  - Multiply → independent choices  

- **Solution:**  

$$
\text{Total committees} = 6 \cdot 15 = 90
$$

---

### **(c) Committees with at least one woman**

- **Analysis:**  
  - Complement: total committees – committees with 0 women (all men)  
  - All men: C(6,4) = 15  

- **Solution:**  

$$
\text{At least 1 woman} = 210 - 15 = 195
$$

---

## **4. Circular Seating (7 people around a round table)**

### **(a) All arrangements**

- **Model:** Circular Permutation  

- **Solution:**  

$$
(7-1)! = 6! = 720
$$

---

### **(b) Two particular people must sit next to each other**

- **Analysis:**  
  - Treat pair as 1 unit → 6 units total  
  - Arrange 6 units around table → (6-1)! = 5! = 120  
  - Pair internal arrangement → 2! = 2  

- **Solution:**  

$$
\text{Total arrangements} = 120 \cdot 2 = 240
$$

---

## **5. Passwords (5 characters, digits 0–9, letters A–Z)**

### **(a) Repetition allowed**

- **Analysis:**  
  - Total symbols: 10 digits + 26 letters = 36  
  - Length = 5 → repetition allowed  

- **Model:** Sequence with Repetition  

- **Solution:**  

$$
36^5 = 60,466,176
$$

---

### **(b) No character may repeat**

- **Analysis:**  
  - 5-permutation of 36 symbols → k-Permutation  

- **Solution:**  

$$
P(36,5) = \frac{36!}{31!} = 36 \cdot 35 \cdot 34 \cdot 33 \cdot 32 = 45,239,040
$$

---

### **(c) Models used**

| Problem | Model |
|---------|-------|
| Letters & digits repeat | Sequence with Repetition |
| Letters no repeat, digits repeat | k-Permutation + Sequence w/ repetition |
| Neither repeat | k-Permutation |
| Medal assignment | k-Permutation |
| Committees | Combination |
| Circular seating | Circular Permutation |
| Passwords | Sequence w/ repetition / k-Permutation |
