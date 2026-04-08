# Problem 2 — Die × Die (Complete Solution)

---

## Question

Consider an experiment consisting of two dice rolls.

Representation:

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .
```

---

### Part A — Marking Events

Mark all outcomes satisfying the statement:

- the sum is equal to 8  
- the first die is greater than the second  
- both dice show even numbers  
- at least one die shows 6  
- exactly one die shows 1  

---

### Part B — Interpretation

Describe the event represented by each case below:

**Case 1**

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . X X X X
4     . . X X X X
5     . . X X X X
6     . . X X X X
```

**Case 2**

```
      1 2 3 4 5 6
1     X . . . . .
2     . X . . . .
3     . . X . . .
4     . . . X . .
5     . . . . X .
6     . . . . . X
```

---

# 📌 Solution

---

## 1. Sample Space

For two dice, the sample space is:

$$
\Omega = \{(i,j) \mid i,j \in \{1,2,3,4,5,6\}\}
$$

There are:

$$
|\Omega| = 6 \times 6 = 36
$$

---

# 🔹 Part A — Marking Events

---

## 1. The Sum Is Equal to 8

We list all pairs where:

$$
i + j = 8
$$

$$
A = \{(2,6), (3,5), (4,4), (5,3), (6,2)\}
$$

---

## 2. The First Die Is Greater Than the Second

This means:

$$
i > j
$$

$$
B = \{(2,1), (3,1), (3,2), (4,1), (4,2), (4,3), (5,1), (5,2), (5,3), (5,4), (6,1), (6,2), (6,3), (6,4), (6,5)\}
$$

---

## 3. Both Dice Show Even Numbers

Even numbers: \( \{2,4,6\} \)

$$
C = \{(2,2), (2,4), (2,6), (4,2), (4,4), (4,6), (6,2), (6,4), (6,6)\}
$$

---

## 4. At Least One Die Shows 6

All outcomes where at least one coordinate is 6:

$$
D = \{(6,1),(6,2),(6,3),(6,4),(6,5),(6,6),
(1,6),(2,6),(3,6),(4,6),(5,6)\}
$$

---

## 5. Exactly One Die Shows 1

This includes two cases:

- first die is 1  
- second die is 1  

$$
E = \{(1,2),(1,3),(1,4),(1,5),(1,6),
(2,1),(3,1),(4,1),(5,1),(6,1)\}
$$

---

# 🔹 Part B — Interpretation

---

## Case 1

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . X X X X
4     . . X X X X
5     . . X X X X
6     . . X X X X
```

### Step 1 — Identify pattern

- All X’s are in rows **3, 4, 5, 6**
- Columns are **3, 4, 5, 6**

### Step 2 — Interpretation

This means:

- both dice are **at least 3**

### ✅ Event:

$$
\text{“Both dice show values greater than or equal to 3”}
$$

---

## Case 2

```
      1 2 3 4 5 6
1     X . . . . .
2     . X . . . .
3     . . X . . .
4     . . . X . .
5     . . . . X .
6     . . . . . X
```

### Step 1 — Identify pattern

- Only diagonal elements are marked

### Step 2 — Interpretation

This means:

- the two dice show **the same number**

### ✅ Event:

$$
\text{“Both dice show the same number”}
$$

---

# 🔍 Final Conceptual Understanding

- Outcomes → ordered pairs in \( \Omega \)  
- Events → subsets of \( \Omega \)  
- Geometry (table view) reveals structure:

  - diagonal → equality  
  - above diagonal → \( i < j \)  
  - below diagonal → \( i > j \)  

👉 Visualization helps understand relationships between outcomes, not just list them.
