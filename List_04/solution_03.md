# Problem 3 — Weather (7 days × 3 states)

## Short description

We model a full week of weather as a table.

- Columns = days of the week (Mon → Sun)
- Rows = weather states:
  - S = sunny
  - C = cloudy
  - R = rainy

Each cell describes whether a weather state is **allowed or included** for that day in a given event.

Important idea:
We are NOT listing full weekly sequences.  
We are describing **constraints on possible weeks**.

---

# General representation

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & . & . & . & . & . & . & . \\
C & . & . & . & . & . & . & . \\
R & . & . & . & . & . & . & . \\
\end{array}
$$

- X = allowed / included
- . = not included

---

# Part A — Marking events

---

## 1. Monday is sunny

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & X & . & . & . & . & . & . \\
C & . & . & . & . & . & . & . \\
R & . & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

I only restrict Monday:
- Monday must be S → I mark X in (S, Mon)
- All other days are free → dots

So I fix ONE condition and leave everything else open.

---

## 2. Weekend is rainy

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & . & . & . & . & . & . & . \\
C & . & . & . & . & . & . & . \\
R & . & . & . & . & . & X & X \\
\end{array}
$$

### Explanation

Weekend = Saturday + Sunday.

Both must be rainy:
- Sat → R
- Sun → R

So I mark R in both weekend columns.

---

## 3. Rain on Wednesday OR Friday

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & . & . & . & . & . & . & . \\
C & . & . & . & . & . & . & . \\
R & . & . & X & . & X & . & . \\
\end{array}
$$

### Explanation

This is an OR condition:
- Wednesday is rainy OR Friday is rainy

So I mark both possibilities in the R row.

We are not requiring both, only at least one.

---

## 4. No rainy day during the week

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & X & X & X & X & X & X & X \\
C & X & X & X & X & X & X & X \\
R & . & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

Condition: no R allowed.

So:
- I remove all R cells completely
- Only S and C remain possible for every day

---

## 5. Thursday is not sunny

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & X & X & X & . & X & X & X \\
C & X & X & X & X & X & X & X \\
R & X & X & X & X & X & X & X \\
\end{array}
$$

### Explanation

Only restriction:
- Thursday cannot be S

So:
- I remove S in Thu column
- Keep C and R allowed

---

# Part B — Interpretation

---

## Case 1

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & . & . & . & . & . & X & X \\
C & . & . & . & . & . & . & . \\
R & . & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

Only Saturday and Sunday are restricted:
- Both must be sunny

All other days are free:
- can be S, C, or R

### Meaning

👉 Weekend is sunny, weekdays are unrestricted.

---

## Case 2

### Graph

$$
\begin{array}{c|ccccccc}
 & Mon & Tue & Wed & Thu & Fri & Sat & Sun \\
\hline
S & X & X & X & X & X & X & X \\
C & X & X & X & X & X & X & X \\
R & . & . & . & . & . & . & . \\
\end{array}
$$

### Explanation

- R is completely removed everywhere
- Only S and C are allowed for all days

### Meaning

👉 There is no rainy day in the entire week.

---

# Final idea

- Columns = time (days)
- Rows = weather states
- X = allowed condition
- . = excluded condition

We translate sentences into restrictions:

- AND → multiple constraints
- OR → multiple allowed positions
- NOT → remove states
- “no X” → remove entire row

---

# Final takeaway

We are not just filling tables — we are converting language into structured mathematical constraints on a sample space.
