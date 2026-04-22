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

## Event B: first die > second die

### Analysis

$$
i > j
$$

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & X & . & . & . & . & . \\
3 & X & X & . & . & . & . \\
4 & X & X & X & . & . & . \\
5 & X & X & X & X & . & . \\
6 & X & X & X & X & X & . \\
\end{array}
$$

### Explanation

I compare row (i) with column (j).  
If i is bigger than j → I put X.  
This is why X’s form a triangle below the diagonal.

---

## Event C: at least one die shows 6

### Analysis

$$
i = 6 \text{ or } j = 6
$$

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & . & X \\
3 & . & . & . & . & . & X \\
4 & . & . & . & . & . & X \\
5 & . & . & . & . & . & X \\
6 & X & X & X & X & X & X \\
\end{array}
$$

### Explanation

I check each cell.  
If either i = 6 or j = 6 → I mark X.  
So I fill the last row and last column.

# Part B — Compound statements

## 1. A ∪ C

### Analysis

We combine:
- A: i + j = 7
- C: i = 6 or j = 6

So X appears if it is in A OR in C.

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & X & X \\
3 & . & . & . & X & . & X \\
4 & . & . & X & . & . & X \\
5 & . & X & . & . & . & X \\
6 & X & X & X & X & X & X \\
\end{array}
$$

### Explanation

I mark all outcomes that are in A or in C.  
So I first identify both patterns and then merge them into one table.

---

## 2. A ∩ C

### Analysis

We keep only outcomes that satisfy BOTH:
- i + j = 7
- and (i = 6 or j = 6)

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & . & . \\
3 & . & . & . & . & . & . \\
4 & . & . & . & . & . & . \\
5 & . & . & . & . & . & . \\
6 & X & . & . & . & . & . \\
\end{array}
$$

### Explanation

I first locate all sum = 7 outcomes.  
Then I keep only those that also contain a 6 in row or column.

---

## 3. B ∩ C

### Analysis

We keep outcomes where:
- i > j
- and (i = 6 or j = 6)

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & . & . & . & . & . & . \\
3 & . & . & . & . & . & . \\
4 & . & . & . & . & . & . \\
5 & . & . & . & . & . & . \\
6 & X & X & X & X & X & . \\
\end{array}
$$

### Explanation

I first take all outcomes where the first die is greater.  
Then I keep only those that also lie in row 6 or column 6.

---

## 4. A ∩ (not B)

### Analysis

We keep:
- A: i + j = 7
- not B: i ≤ j

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & X & . \\
3 & . & . & . & X & . & . \\
4 & . & . & . & . & . & . \\
5 & . & . & . & . & . & . \\
6 & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

I take the sum = 7 diagonal.  
Then I remove all cases where i > j, leaving only i ≤ j.

---

## 5. A ∩ (not C)

### Analysis

We keep:
- A: i + j = 7
- not C: no 6 in row or column

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & . & . & . & . & X & . \\
3 & . & . & . & X & . & . \\
4 & . & . & X & . & . & . \\
5 & . & X & . & . & . & . \\
6 & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

I start from sum = 7 cases.  
Then I remove every outcome that involves a 6.

---

## 6. C ∩ (not A)

### Analysis

We keep:
- C: i = 6 or j = 6
- not A: i + j ≠ 7

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & . & X \\
3 & . & . & . & . & . & X \\
4 & . & . & . & . & . & X \\
5 & . & . & . & . & . & X \\
6 & . & X & X & X & X & X \\
\end{array}
$$

### Explanation

I take all cases with a 6.  
Then I remove the two outcomes that sum to 7.

---

## 7. (not A) ∩ B

### Analysis

We keep:
- B: i > j
- not A: i + j ≠ 7

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & X & . & . & . & . & . \\
3 & X & X & . & . & . & . \\
4 & X & X & X & . & . & . \\
5 & X & X & X & X & . & . \\
6 & . & X & X & X & X & . \\
\end{array}
$$

### Explanation

I start with all i > j outcomes.  
Then I remove the diagonal sum = 7 cases.

---

## 8. (not B) ∩ C

### Analysis

We keep:
- not B: i ≤ j
- C: i = 6 or j = 6

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & X \\
2 & . & . & . & . & . & X \\
3 & . & . & . & . & . & X \\
4 & . & . & . & . & . & X \\
5 & . & . & . & . & . & X \\
6 & . & . & . & . & . & X \\
\end{array}
$$

### Explanation

I only allow i ≤ j.  
Then I keep only outcomes with a 6.

---

## 9. not (A ∪ C)

### Analysis

We invert everything in A ∪ C.

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & X & X & X & X & X & . \\
2 & X & X & X & X & . & . \\
3 & X & X & X & . & X & . \\
4 & X & X & . & X & X & . \\
5 & X & . & X & X & X & . \\
6 & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

I take everything in A or C and flip it.  
All X become dots and all dots become X.

---

## 10. not (A ∩ C)

### Analysis

We remove only the intersection of A and C.

### Solution

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & X & X & X & X & X & . \\
2 & X & X & X & X & X & X \\
3 & X & X & X & X & X & X \\
4 & X & X & X & X & X & X \\
5 & X & X & X & X & X & X \\
6 & X & X & X & X & X & X \\
\end{array}
$$

### Explanation

I remove only the overlap of A and C (the shared outcomes).  
Everything else stays unchanged.
