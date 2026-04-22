# Problem 2 — Die × Die

## Short description

We roll two fair dice.

Each outcome is an ordered pair:

$$
(i, j)
$$

where:
- i = result of first die (row)
- j = result of second die (column)

So the sample space is a 6×6 grid of all 36 outcomes.

- X = included in the event  
- . = not included  

---

# Part A — Marking events

---

## 1. Sum is equal to 8

### Analysis

We select all outcomes where:

$$
i + j = 8
$$

### Graph

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & . & . & . & . & . & X \\
3 & . & . & . & . & X & . \\
4 & . & . & . & X & . & . \\
5 & . & . & X & . & . & . \\
6 & . & X & . & . & . & . \\
\end{array}
$$

### Explanation

Each cell represents \((i, j)\).

I check:
- if \(i + j = 8\) → mark X
- otherwise → mark .

So the valid outcomes are:
- (2,6)
- (3,5)
- (4,4)
- (5,3)
- (6,2)

---

## 2. First die is greater than second

### Analysis

$$
i > j
$$

### Graph

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

For each cell:
- row = i
- column = j

If row number is bigger than column number → X  
Otherwise → .

So we get the lower triangle of the table.

---

## 3. Both dice show even numbers

### Analysis

Even numbers = {2, 4, 6}

So:

$$
i \in \{2,4,6\}, \quad j \in \{2,4,6\}
$$

### Graph

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & . & X & . & X & . & X \\
3 & . & . & . & . & . & . \\
4 & . & X & . & X & . & X \\
5 & . & . & . & . & . & . \\
6 & . & X & . & X & . & X \\
\end{array}
$$

### Explanation

I only allow:
- even rows (2,4,6)
- even columns (2,4,6)

Everything else is removed.

---

## 4. At least one die shows 6

### Analysis

$$
i = 6 \;\; \text{or} \;\; j = 6
$$

### Graph

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

I mark X whenever:
- row = 6 OR column = 6

So full last row and last column are included.

---

## 5. Exactly one die shows 1

### Analysis

Two cases:
- (1, j) where j ≠ 1
- (i, 1) where i ≠ 1

### Graph

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & X & X & X & X & X \\
2 & X & . & . & . & . & . \\
3 & X & . & . & . & . & . \\
4 & X & . & . & . & . & . \\
5 & X & . & . & . & . & . \\
6 & X & . & . & . & . & . \\
\end{array}
$$

### Explanation

Exactly one die is 1 means:
- one coordinate is 1
- the other is NOT 1

So we include:
- row 1 except (1,1)
- column 1 except (1,1)

---

# Part B — Interpretation

---

## Case 1

### Graph

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & . & . & . & . & . & . \\
2 & . & . & X & X & X & X \\
3 & . & X & X & X & X & . \\
4 & . & X & X & X & X & . \\
5 & . & X & X & X & X & . \\
6 & . & . & X & X & X & . \\
\end{array}
$$

### Explanation

This selects a **central block of outcomes**.

It means:
- both dice take values mostly between 2 and 5
- extreme values (1 and 6) are mostly excluded

So the event describes:
> outcomes concentrated in the middle range of the sample space

---

## Case 2

### Graph

$$
\begin{array}{c|cccccc}
 & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & X & . & . & . & . & . \\
2 & . & X & . & . & . & . \\
3 & . & . & X & . & . & . \\
4 & . & . & . & X & . & . \\
5 & . & . & . & . & X & . \\
6 & . & . & . & . & . & X \\
\end{array}
$$

### Explanation

Only diagonal entries are selected:

$$
(i, i)
$$

So both dice show the same number.

Meaning:
> the event is “doubles” (both dice equal)

---

# Final idea

- rows = first die
- columns = second die

Each rule creates a geometric pattern:
- sum → diagonal
- inequality → triangle
- even numbers → grid restriction
- 6 condition → row/column cross
- “exactly one” → two intersecting strips
