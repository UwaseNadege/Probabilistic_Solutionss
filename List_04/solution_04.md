# Problem 4 — Building complex statements from simple ones

## General setup

Each outcome is (i, j):
- i = row (first die ↓)
- j = column (second die →)

So every cell means:
$$
(i, j)
$$

---

# Part A — Basic statements

## Event A: sum equals 7

### Analysis

$$
i + j = 7
$$

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & X & . \\
3 & . & . & . & X & . & . \\
4 & . & . & X & . & . & . \\
5 & . & X & . & . & . & . \\
6 & X & . & . & . & . & . \\
\end{array}
$$

### Explanation

I go through each cell (i, j).  
I check the sum i + j.  
If it equals 7 → I mark X, otherwise I mark .  

---
# Part B — Compound Statements

---

## 1. A ∪ C

**∪ means OR** — an outcome counts if it satisfies **either** event or both.

So **A ∪ C** means: *"The sum of the dice is 7 **OR** at least one die shows 6."*

### Analysis

```

Event A (i+j=7)          ∪        Event C (i=6 or j=6)        →        A ∪ C

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 . . . . . X                     1 . . . . . X                   1 . . . . . X

2 . . . . X .                     2 . . . . . X                   2 . . . . X X

3 . . . X . .                     3 . . . . . X                   3 . . . X . X

4 . . X . . .                     4 . . . . . X                   4 . . X . . X

5 . X . . . .                     5 . . . . . X                   5 . X . . . X

6 X . . . . .                     6 X X X X X X                   6 X X X X X X

```

### Explanation

I place Event A next to Event C.

I mark X in the result wherever **either** table has an X.

OR only needs one condition — so all sum=7 outcomes AND all 6-containing outcomes get marked.

---

## 2. A ∩ C

**∩ means AND** — an outcome only counts if it satisfies **both** events at the same time.

So **A ∩ C** means: *"The sum of the dice is 7 **AND** at least one die shows 6."*

### Analysis

```

Event A (i+j=7)          ∩        Event C (i=6 or j=6)        →        A ∩ C

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 . . . . . X                     1 . . . . . X                   1 . . . . . X

2 . . . . X .                     2 . . . . . X                   2 . . . . . .

3 . . . X . .                     3 . . . . . X                   3 . . . . . .

4 . . X . . .                     4 . . . . . X                   4 . . . . . .

5 . X . . . .                     5 . . . . . X                   5 . . . . . .

6 X . . . . .                     6 X X X X X X                   6 X . . . . .

```

### Explanation

I place Event A next to Event C.

I only mark X where **both** tables have an X at the exact same cell.

Only (1,6) and (6,1) appear in both — those are the only sum=7 outcomes that also contain a 6.

---

## 3. B ∩ C

**∩ means AND** — an outcome only counts if it satisfies **both** events at the same time.

So **B ∩ C** means: *"The first die is greater than the second **AND** at least one die shows 6."*

### Analysis

```

Event B (i>j)            ∩        Event C (i=6 or j=6)        →        B ∩ C

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 . . . . . .                     1 . . . . . X                   1 . . . . . .

2 X . . . . .                     2 . . . . . X                   2 . . . . . .

3 X X . . . .                     3 . . . . . X                   3 . . . . . .

4 X X X . . .                     4 . . . . . X                   4 . . . . . .

5 X X X X . .                     5 . . . . . X                   5 . . . . . .

6 X X X X X .                     6 X X X X X X                   6 X X X X X .

```

### Explanation

I place Event B (lower-left triangle) next to Event C (row 6 and column 6).

I only mark X where **both** tables share an X at the same cell.

Row 6 cols 1–5 appear in both. Cell (6,6) is excluded because 6 is not greater than 6.

---

## 4. A ∩ (not B)

**∩ means AND** and **not B flips Event B** — keeping only i ≤ j.

So **A ∩ (not B)** means: *"The sum is 7 **AND** the first die is not greater than the second."*

### Analysis

```

Event A (i+j=7)          ∩        not B (i≤j)                  →     A ∩ (not B)

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 . . . . . X                     1 X X X X X X                   1 . . . . . X

2 . . . . X .                     2 . X X X X X                   2 . . . . X .

3 . . . X . .                     3 . . X X X X                   3 . . . X . .

4 . . X . . .                     4 . . . X X X                   4 . . . . . .

5 . X . . . .                     5 . . . . X X                   5 . . . . . .

6 X . . . . .                     6 . . . . . X                   6 . . . . . .

```

### Explanation

I flip Event B to get not B — the upper triangle where i ≤ j.

I keep only sum=7 cells that also appear in not B.

(1,6), (2,5), (3,4) survive. (4,3), (5,2), (6,1) are removed because i > j there.

---

## 5. A ∩ (not C)

**∩ means AND** and **not C flips Event C** — keeping only outcomes with no 6.

So **A ∩ (not C)** means: *"The sum is 7 **AND** neither die shows a 6."*

### Analysis

```

Event A (i+j=7)          ∩        not C (no 6)                  →     A ∩ (not C)

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 . . . . . X                     1 X X X X X .                   1 . . . . . .

2 . . . . X .                     2 X X X X X .                   2 . . . . X .

3 . . . X . .                     3 X X X X X .                   3 . . . X . .

4 . . X . . .                     4 X X X X X .                   4 . . X . . .

5 . X . . . .                     5 X X X X X .                   5 . X . . . .

6 X . . . . .                     6 . . . . . .                   6 . . . . . .

```

### Explanation

I flip Event C to get not C — removing all row 6 and column 6 outcomes.

I keep only sum=7 cells that survive the flip.

(1,6) and (6,1) are removed. The four middle pairs (2,5)(3,4)(4,3)(5,2) remain.

---

## 6. C ∩ (not A)

**∩ means AND** and **not A flips Event A** — keeping only outcomes where sum ≠ 7.

So **C ∩ (not A)** means: *"At least one die shows 6 **AND** the sum is not 7."*

### Analysis

```

Event C (i=6 or j=6)     ∩        not A (sum≠7)                →     C ∩ (not A)

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 . . . . . X                     1 X X X X X .                   1 . . . . . X

2 . . . . . X                     2 X X X X X X                   2 . . . . . X

3 . . . . . X                     3 X X X X X X                   3 . . . . . X

4 . . . . . X                     4 X X X X X X                   4 . . . . . X

5 . . . . . X                     5 X X X X X X                   5 . . . . . X

6 X X X X X X                     6 X . . . . X                   6 . X X X X X

```

### Explanation

I flip Event A to get not A — everything except the sum=7 diagonal.

I keep only cells from Event C that also appear in not A.

(1,6) and (6,1) are removed because they sum to 7. All other 6-containing outcomes stay.

---

## 7. (not A) ∩ B

**∩ means AND** and **not A flips Event A** — keeping only outcomes where sum ≠ 7.

So **(not A) ∩ B** means: *"The sum is not 7 **AND** the first die is greater than the second."*

### Analysis

```

not A (sum≠7)            ∩        Event B (i>j)                →    (not A) ∩ B

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 X X X X X .                     1 . . . . . .                   1 . . . . . .

2 X X X X X X                     2 X . . . . .                   2 X . . . . .

3 X X X X X X                     3 X X . . . .                   3 X X . . . .

4 X X X X X X                     4 X X X . . .                   4 X X X . . .

5 X X X X X X                     5 X X X X . .                   5 X X X X . .

6 X . . . . X                     6 X X X X X .                   6 . X X X X .

```

### Explanation

I flip Event A to get not A — removing the sum=7 diagonal.

I keep only cells from not A that also appear in Event B (lower-left triangle).

Only (6,1) gets removed from B since it was the one sum=7 outcome inside the triangle.

---

## 8. (not B) ∩ C

**∩ means AND** and **not B flips Event B** — keeping only i ≤ j.

So **(not B) ∩ C** means: *"The first die is not greater than the second **AND** at least one die shows 6."*

### Analysis

```

not B (i≤j)              ∩        Event C (i=6 or j=6)        →    (not B) ∩ C

  1 2 3 4 5 6                       1 2 3 4 5 6                      1 2 3 4 5 6

1 X X X X X X                     1 . . . . . X                   1 . . . . . X

2 . X X X X X                     2 . . . . . X                   2 . . . . . X

3 . . X X X X                     3 . . . . . X                   3 . . . . . X

4 . . . X X X                     4 . . . . . X                   4 . . . . . X

5 . . . . X X                     5 . . . . . X                   5 . . . . . X

6 . . . . . X                     6 X X X X X X                   6 . . . . . X

```

### Explanation

I flip Event B to get not B — the upper triangle where i ≤ j.

I keep only cells that appear in both not B and Event C.

Only column 6 survives — j=6 always satisfies i ≤ j for every row.

---

## 9. not (A ∪ C)

**not means complement** — we flip the entire result of A ∪ C.

So **not (A ∪ C)** means: *"The sum is not 7 AND neither die shows a 6."*

### Analysis

```

A ∪ C (built from Q1)              →         not (A ∪ C)  [flip every cell]

  1 2 3 4 5 6                                  1 2 3 4 5 6

1 . . . . . X                               1 X X X X X .

2 . . . . X X                               2 X X X X . .

3 . . . X . X                               3 X X X . X .

4 . . X . . X                               4 X X . X X .

5 . X . . . X                               5 X . X X X .

6 X X X X X X                               6 . . . . . .

```

### Explanation

I take the full A ∪ C result from Question 1.

I flip every cell — X becomes dot and dot becomes X.

What remains is every outcome that had no 6 and did not sum to 7.

---

## 10. not (A ∩ C)

**not means complement** — we flip the entire result of A ∩ C.

So **not (A ∩ C)** means: *"It is not the case that the sum is 7 AND a 6 is showing."*

### Analysis

```

A ∩ C (built from Q2)              →         not (A ∩ C)  [flip every cell]

  1 2 3 4 5 6                                  1 2 3 4 5 6

1 . . . . . X                               1 X X X X X .

2 . . . . . .                               2 X X X X X X

3 . . . . . .                               3 X X X X X X

4 . . . . . .                               4 X X X X X X

5 . . . . . .                               5 X X X X X X

6 X . . . . .                               6 . X X X X X

```

### Explanation

A ∩ C only had two outcomes marked: (1,6) and (6,1).

I flip the entire grid — those two become dots and all 34 other outcomes become X.

This is the largest possible result since we are only removing 2 cells out of 36.
 
