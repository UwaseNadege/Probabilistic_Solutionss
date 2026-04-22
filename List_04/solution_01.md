# Problem 1 — Coin × Coin

## Short description

We perform **two coin tosses**.

Each outcome is an ordered pair:

$$
(i, j)
$$

where:
- i = first toss (row)
- j = second toss (column)

Each cell represents one outcome:
- X = included in event  
- . = not included  

So the sample space is:

$$
\{(H,H), (H,T), (T,H), (T,T)\}
$$

---

# General representation

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & . & . \\
T & . & . \\
\end{array}
$$

---

# Part A — Marking events

---

## 1. Exactly one head

### Analysis

We want outcomes where exactly one toss is H:

$$
(H,T), (T,H)
$$

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & . & X \\
T & X & . \\
\end{array}
$$

### Explanation

I check each ordered pair:
- (H,H) → 2 heads → reject
- (H,T) → 1 head → accept
- (T,H) → 1 head → accept
- (T,T) → 0 heads → reject

So I mark only cases with exactly one head.

---

## 2. Both tosses are the same

### Analysis

We want:

$$
(H,H), (T,T)
$$

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & X & . \\
T & . & X \\
\end{array}
$$

### Explanation

I check equality of results:
- same outcome → X
- different outcome → .

So I select diagonal entries only.

---

## 3. At least one head

### Analysis

All outcomes except (T,T)

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & X & X \\
T & X & . \\
\end{array}
$$

### Explanation

I mark all outcomes where:
- first is H OR second is H

Only (T,T) is excluded.

---

## 4. First toss is tails

### Analysis

All outcomes where first result = T:

$$
(T,H), (T,T)
$$

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & . & . \\
T & X & X \\
\end{array}
$$

### Explanation

I fix row = T and include all columns.

---

## 5. Second toss is heads

### Analysis

All outcomes where second result = H:

$$
(H,H), (T,H)
$$

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & X & . \\
T & X & . \\
\end{array}
$$

### Explanation

I fix column = H and include both rows.

---

# Part B — Interpretation

---

## Case 1

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & X & X \\
T & . & . \\
\end{array}
$$

### Step-by-step interpretation

This means:
- first toss must be H (only top row is active)
- second toss can be H or T

So the event is:

$$
(H,H), (H,T)
$$

### Meaning

👉 The first toss is **heads**

---

## Case 2

### Graph

$$
\begin{array}{c|cc}
 & H & T \\
\hline
H & . & X \\
T & X & . \\
\end{array}
$$

### Step-by-step interpretation

This selects:
- (H,T)
- (T,H)

So both outcomes are different.

### Meaning

👉 The two tosses are **different results** (exactly one head)

---

# Final idea

- Rows = first toss
- Columns = second toss

Patterns:
- same results → diagonal
- exactly one head → anti-diagonal
- first fixed → row selection
- second fixed → column selection
