# Problem 1 — Event algebra from a two-way table

## General setup

Let:

- $A$ = the student attends lectures regularly  
- $B$ = the student submits homework on time  

Total number of students:

$$
100
$$

The table:

| Student type | Submits on time | Does not submit on time | Total |
|---|---|---|---|
| Attends lectures regularly | 48 | 12 | 60 |
| Does not attend regularly | 22 | 18 | 40 |
| Total | 70 | 30 | 100 |

---

# Part A — The four disjoint regions

---

## Region 1 — $A \cap B$

### Analysis

$A \cap B$ means:

- attends lectures regularly  
AND
- submits homework on time

From the table:

$$
n(A \cap B)=48
$$

### Solution (step-by-step)

$$
P(A \cap B)=\frac{48}{100}
$$

$$
P(A \cap B)=0.48
$$

### Explanation

48 students both attend lectures regularly and submit homework on time.

---

## Region 2 — $A \cap B^c$

### Analysis

$B^c$ means “does not submit homework on time”.

So $A \cap B^c$ means:

- attends lectures regularly  
AND
- does not submit homework on time

From the table:

$$
n(A \cap B^c)=12
$$

### Solution (step-by-step)

$$
P(A \cap B^c)=\frac{12}{100}
$$

$$
P(A \cap B^c)=0.12
$$

### Explanation

12 students attend lectures regularly but do not submit homework on time.

---

## Region 3 — $A^c \cap B$

### Analysis

$A^c$ means “does not attend lectures regularly”.

So $A^c \cap B$ means:

- does not attend regularly  
AND
- submits homework on time

From the table:

$$
n(A^c \cap B)=22
$$

### Solution (step-by-step)

$$
P(A^c \cap B)=\frac{22}{100}
$$

$$
P(A^c \cap B)=0.22
$$

### Explanation

22 students do not attend lectures regularly but still submit homework on time.

---

## Region 4 — $A^c \cap B^c$

### Analysis

This means:

- does not attend lectures regularly  
AND
- does not submit homework on time

From the table:

$$
n(A^c \cap B^c)=18
$$

### Solution (step-by-step)

$$
P(A^c \cap B^c)=\frac{18}{100}
$$

$$
P(A^c \cap B^c)=0.18
$$

### Explanation

18 students neither attend lectures regularly nor submit homework on time.

---

# Part B — Compute $P(A)$, $P(B)$, and $P(A \cup B)$

---

## Probability of $A$

### Analysis

Event $A$ includes:

- $A \cap B$
- $A \cap B^c$

### Solution (step-by-step)

$$
P(A)=0.48+0.12
$$

$$
P(A)=0.60
$$

### Explanation

60% of students attend lectures regularly.

---

## Probability of $B$

### Analysis

Event $B$ includes:

- $A \cap B$
- $A^c \cap B$

### Solution (step-by-step)

$$
P(B)=0.48+0.22
$$

$$
P(B)=0.70
$$

### Explanation

70% of students submit homework on time.

---

## Probability of $A \cup B$

### Analysis

$A \cup B$ means:

- attends regularly OR
- submits homework on time
- or both

The only excluded region is:

$$
A^c \cap B^c
$$

### Solution (step-by-step)

$$
P(A \cup B)=1-P(A^c \cap B^c)
$$

$$
P(A \cup B)=1-0.18
$$

$$
P(A \cup B)=0.82
$$

### Explanation

82% of students either attend regularly, submit homework on time, or do both.

---

# Part C — Conditional probabilities

---

## Compute $P(A \mid B)$

### Analysis

$P(A \mid B)$ means:

“Probability that a student attends lectures regularly GIVEN that the student submits homework on time.”

Formula:

$$
P(A \mid B)=\frac{P(A \cap B)}{P(B)}
$$

### Solution (step-by-step)

$$
P(A \mid B)=\frac{0.48}{0.70}
$$

$$
P(A \mid B)=0.6857
$$

$$
P(A \mid B)\approx0.686
$$

### Explanation

Among students who submit homework on time, about 68.6% attend lectures regularly.

---

## Compute $P(B \mid A)$

### Analysis

$P(B \mid A)$ means:

“Probability that a student submits homework on time GIVEN that the student attends lectures regularly.”

Formula:

$$
P(B \mid A)=\frac{P(A \cap B)}{P(A)}
$$

### Solution (step-by-step)

$$
P(B \mid A)=\frac{0.48}{0.60}
$$

$$
P(B \mid A)=0.80
$$

### Explanation

Among students who attend lectures regularly, 80% submit homework on time.

---

# Part D — Are $A$ and $B$ mutually exclusive?

### Analysis

Two events are mutually exclusive if they cannot happen together.

But:

$$
P(A \cap B)=0.48
$$

which is not zero.

### Conclusion

No, $A$ and $B$ are not mutually exclusive.

### Explanation

Some students both attend lectures regularly and submit homework on time.

---

# Part E — Are $A$ and $B$ independent?

### Analysis

Events are independent if:

$$
P(A \cap B)=P(A)P(B)
$$

Compute:

$$
P(A)P(B)=0.60 \times 0.70
$$

$$
P(A)P(B)=0.42
$$

But:

$$
P(A \cap B)=0.48
$$

Since:

$$
0.48 \ne 0.42
$$

the events are not independent.

### Conclusion

No, $A$ and $B$ are not independent.

### Explanation

Submitting homework on time is related to lecture attendance.

---

# Part F — Interpretation in words

---

## Interpretation of $P(A \mid B)$

$$
P(A \mid B)
$$

means:

> The probability that a student attends lectures regularly, given that the student submits homework on time.

---

## Interpretation of $P(B \mid A)$

$$
P(B \mid A)
$$

means:

> The probability that a student submits homework on time, given that the student attends lectures regularly.
