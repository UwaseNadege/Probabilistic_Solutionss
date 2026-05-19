# Problem 2 — Four regions of a sample space

## General setup

Let:

- $T$ = the ticket is technical  
- $S$ = the ticket was solved during the first contact  

Total number of tickets:

$$
350
$$

The table:

| Ticket type | Solved during first contact | Not solved during first contact | Total |
|---|---|---|---|
| Technical | 90 | 60 | 150 |
| Non-technical | 160 | 40 | 200 |
| Total | 250 | 100 | 350 |

---

# Part A — The four disjoint regions

---

## Region 1 — $T \cap S$

### Analysis

$T \cap S$ means:

- the ticket is technical  
AND
- the ticket was solved during the first contact

From the table:

$$
n(T \cap S)=90
$$

### Solution (step-by-step)

$$
P(T \cap S)=\frac{90}{350}
$$

$$
P(T \cap S)=0.2571
$$

### Explanation

90 tickets were both technical and solved during the first contact.

---

## Region 2 — $T \cap S^c$

### Analysis

$S^c$ means “not solved during the first contact”.

So $T \cap S^c$ means:

- the ticket is technical  
AND
- the ticket was not solved during the first contact

From the table:

$$
n(T \cap S^c)=60
$$

### Solution (step-by-step)

$$
P(T \cap S^c)=\frac{60}{350}
$$

$$
P(T \cap S^c)=0.1714
$$

### Explanation

60 tickets were technical but not solved during the first contact.

---

## Region 3 — $T^c \cap S$

### Analysis

$T^c$ means “non-technical”.

So $T^c \cap S$ means:

- the ticket is non-technical  
AND
- the ticket was solved during the first contact

From the table:

$$
n(T^c \cap S)=160
$$

### Solution (step-by-step)

$$
P(T^c \cap S)=\frac{160}{350}
$$

$$
P(T^c \cap S)=0.4571
$$

### Explanation

160 tickets were non-technical and solved during the first contact.

---

## Region 4 — $T^c \cap S^c$

### Analysis

This means:

- the ticket is non-technical  
AND
- the ticket was not solved during the first contact

From the table:

$$
n(T^c \cap S^c)=40
$$

### Solution (step-by-step)

$$
P(T^c \cap S^c)=\frac{40}{350}
$$

$$
P(T^c \cap S^c)=0.1143
$$

### Explanation

40 tickets were non-technical and not solved during the first contact.

---

# Part B — Verify that the four probabilities add up to 1

### Solution (step-by-step)

$$
0.2571+0.1714+0.4571+0.1143
$$

$$
=0.4285+0.4571+0.1143
$$

$$
=0.8856+0.1143
$$

$$
\approx 1.000
$$

### Explanation

The four disjoint regions cover the entire sample space, so their probabilities must add up to 1.

---

# Part C — Compute $P(T \cup S)$

### Analysis

$T \cup S$ means:

- the ticket is technical  
OR
- the ticket was solved during the first contact
- or both

The only excluded region is:

$$
T^c \cap S^c
$$

### Solution (step-by-step)

$$
P(T \cup S)=1-P(T^c \cap S^c)
$$

$$
P(T \cup S)=1-0.1143
$$

$$
P(T \cup S)=0.8857
$$

### Explanation

About 88.6% of tickets are either technical, solved during first contact, or both.

---

# Part D — Compute $P(T^c \cup S)$

### Analysis

$T^c \cup S$ means:

- the ticket is non-technical  
OR
- the ticket was solved during the first contact
- or both

The only excluded region is:

$$
T \cap S^c
$$

### Solution (step-by-step)

$$
P(T^c \cup S)=1-P(T \cap S^c)
$$

$$
P(T^c \cup S)=1-0.1714
$$

$$
P(T^c \cup S)=0.8286
$$

### Explanation

About 82.9% of tickets are either non-technical, solved during first contact, or both.

---

# Part E — Conditional probabilities

---

## Compute $P(S \mid T)$

### Analysis

$P(S \mid T)$ means:

“Probability that a ticket was solved during the first contact GIVEN that the ticket is technical.”

Formula:

$$
P(S \mid T)=\frac{P(T \cap S)}{P(T)}
$$

First compute:

$$
P(T)=\frac{150}{350}
$$

$$
P(T)=0.4286
$$

### Solution (step-by-step)

$$
P(S \mid T)=\frac{0.2571}{0.4286}
$$

$$
P(S \mid T)=0.60
$$

### Explanation

Among technical tickets, 60% were solved during the first contact.

---

## Compute $P(S \mid T^c)$

### Analysis

$P(S \mid T^c)$ means:

“Probability that a ticket was solved during the first contact GIVEN that the ticket is non-technical.”

Formula:

$$
P(S \mid T^c)=\frac{P(T^c \cap S)}{P(T^c)}
$$

First compute:

$$
P(T^c)=\frac{200}{350}
$$

$$
P(T^c)=0.5714
$$

### Solution (step-by-step)

$$
P(S \mid T^c)=\frac{0.4571}{0.5714}
$$

$$
P(S \mid T^c)=0.80
$$

### Explanation

Among non-technical tickets, 80% were solved during the first contact.

---

# Part F — Does being a technical ticket change the probability of being solved during the first contact?

### Analysis

Compare:

$$
P(S \mid T)=0.60
$$

and

$$
P(S \mid T^c)=0.80
$$

Since these probabilities are different, the type of ticket affects the probability of being solved during the first contact.

### Conclusion

Yes, being a technical ticket changes the probability of being solved during the first contact.

### Explanation

Technical tickets are less likely to be solved during the first contact than non-technical tickets.v
