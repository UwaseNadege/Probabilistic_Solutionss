#  Problem 1 — Coin × Coin (Complete Solution)

---

##  Question

Consider an experiment consisting of two coin tosses.

Representation:

```
      H   T
H     .   .
T     .   .
```

Each cell corresponds to one possible outcome.

---

### Part A — Marking Events

For each statement, mark all outcomes for which the statement is true:

- exactly one head  
- both tosses are the same  
- at least one head  
- the first toss is tails  
- the second toss is heads  

---

### Part B — Interpretation

Describe the event represented by each case below:

**Case 1**

```
      H   T
H     X   X
T     .   .
```

**Case 2**

```
      H   T
H     .   X
T     X   .
```

---

# 📌 Solution

---

## 1. Sample Space

For two coin tosses:

$$
\Omega = \{(H,H), (H,T), (T,H), (T,T)\}
$$

---

# 🔹 Part A — Marking Events

---

## 1. Exactly One Head

$$
A = \{(H,T), (T,H)\}
$$

---

## 2. Both Tosses Are the Same

$$
B = \{(H,H), (T,T)\}
$$

---

## 3. At Least One Head

$$
C = \{(H,H), (H,T), (T,H)\}
$$

---

## 4. The First Toss Is Tails

$$
D = \{(T,H), (T,T)\}
$$

---

## 5. The Second Toss Is Heads

$$
E = \{(H,H), (T,H)\}
$$

---

# 🔹 Part B — Interpretation

---

## Case 1

```
      H   T
H     X   X
T     .   .
```

### Marked outcomes:

$$
\{(H,H), (H,T)\}
$$

### Interpretation:

- The **first toss is heads**

### ✅ Event:

$$
\text{“The first toss is heads”}
$$

---

## Case 2

```
      H   T
H     .   X
T     X   .
```

### Marked outcomes:

$$
\{(H,T), (T,H)\}
$$

### Interpretation:

- The two tosses are **different**

### Event:

$$
\text{“Exactly one head”}
$$

---

#  Final Conceptual Understanding

- Outcomes → elements of \( \Omega \)  
- Events → subsets of \( \Omega \)  

Logical translation:

- AND → intersection  
- OR → union  
- NOT → complement  

👉 This problem shows how to translate **real situations into mathematical formalism**
