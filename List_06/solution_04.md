# Problem 4 — Inclusion–exclusion and double counting

## General setup

A company surveyed 200 employees about two software tools.

Given:

- 130 employees use Tool A
- 90 employees use Tool B
- 60 employees use both tools

Let:

- $A$ = the employee uses Tool A  
- $B$ = the employee uses Tool B  

Total number of employees:

$$
200
$$

---

# Part A — Compute $P(A)$, $P(B)$, and $P(A \cap B)$

---

## Compute $P(A)$

### Analysis

Event $A$ means:

> the employee uses Tool A.

From the information given:

$$
n(A)=130
$$

### Solution (step-by-step)

$$
P(A)=\frac{130}{200}
$$

$$
P(A)=0.65
$$

### Explanation

65% of employees use Tool A.

---

## Compute $P(B)$

### Analysis

Event $B$ means:

> the employee uses Tool B.

From the information given:

$$
n(B)=90
$$

### Solution (step-by-step)

$$
P(B)=\frac{90}{200}
$$

$$
P(B)=0.45
$$

### Explanation

45% of employees use Tool B.

---

## Compute $P(A \cap B)$

### Analysis

$A \cap B$ means:

> the employee uses both Tool A and Tool B.

From the information given:

$$
n(A \cap B)=60
$$

### Solution (step-by-step)

$$
P(A \cap B)=\frac{60}{200}
$$

$$
P(A \cap B)=0.30
$$

### Explanation

30% of employees use both software tools.

---

# Part B — Use inclusion–exclusion to compute $P(A \cup B)$

### Analysis

$A \cup B$ means:

> the employee uses Tool A or Tool B or both.

Use the inclusion–exclusion formula:

$$
P(A \cup B)=P(A)+P(B)-P(A \cap B)
$$

### Solution (step-by-step)

$$
P(A \cup B)=0.65+0.45-0.30
$$

$$
P(A \cup B)=1.10-0.30
$$

$$
P(A \cup B)=0.80
$$

### Explanation

80% of employees use at least one of the two tools.

---

# Part C — Compute the probabilities of the remaining regions

---

## Region 1 — $A \setminus B$

### Analysis

$A \setminus B$ means:

> employees who use Tool A but not Tool B.

Formula:

$$
P(A \setminus B)=P(A)-P(A \cap B)
$$

### Solution (step-by-step)

$$
P(A \setminus B)=0.65-0.30
$$

$$
P(A \setminus B)=0.35
$$

### Explanation

35% of employees use only Tool A.

---

## Region 2 — $B \setminus A$

### Analysis

$B \setminus A$ means:

> employees who use Tool B but not Tool A.

Formula:

$$
P(B \setminus A)=P(B)-P(A \cap B)
$$

### Solution (step-by-step)

$$
P(B \setminus A)=0.45-0.30
$$

$$
P(B \setminus A)=0.15
$$

### Explanation

15% of employees use only Tool B.

---

## Region 3 — $A^c \cap B^c$

### Analysis

$A^c \cap B^c$ means:

> employees who use neither Tool A nor Tool B.

Formula:

$$
P(A^c \cap B^c)=1-P(A \cup B)
$$

### Solution (step-by-step)

$$
P(A^c \cap B^c)=1-0.80
$$

$$
P(A^c \cap B^c)=0.20
$$

### Explanation

20% of employees use neither tool.

---

# Part D — Compute $P(A \mid B)$

### Analysis

$P(A \mid B)$ means:

> Probability that an employee uses Tool A GIVEN that the employee uses Tool B.

Formula:

$$
P(A \mid B)=\frac{P(A \cap B)}{P(B)}
$$

### Solution (step-by-step)

$$
P(A \mid B)=\frac{0.30}{0.45}
$$

$$
P(A \mid B)=0.6667
$$

### Explanation

Among employees who use Tool B, about 66.7% also use Tool A.

---

# Part E — Compute $P(B \mid A)$

### Analysis

$P(B \mid A)$ means:

> Probability that an employee uses Tool B GIVEN that the employee uses Tool A.

Formula:

$$
P(B \mid A)=\frac{P(A \cap B)}{P(A)}
$$

### Solution (step-by-step)

$$
P(B \mid A)=\frac{0.30}{0.65}
$$

$$
P(B \mid A)=0.4615
$$

### Explanation

Among employees who use Tool A, about 46.2% also use Tool B.

---

# Part F — Explain why

$$
P(A \cup B)\ne P(A)+P(B)
$$

### Analysis

If we simply add:

$$
P(A)+P(B)
$$

then employees who use both tools are counted twice.

This happens because the overlap:

$$
A \cap B
$$

belongs to both events.

### Explanation

To avoid double counting, we subtract:

$$
P(A \cap B)
$$

once in the inclusion–exclusion formula.

---

# Part G — Which group is counted twice in $P(A)+P(B)$?

### Analysis

The employees counted twice are those in:

$$
A \cap B
$$

### Explanation

These are employees who use both Tool A and Tool B.

They are included once in $P(A)$ and again in $P(B)$, so they must be subtracted once to get the correct probability.
