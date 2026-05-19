# Problem 10 — Comprehensive problem: event algebra, conditioning, independence, and Bayes

## General setup

Let:

- $T$ = the user received the tutorial  
- $C$ = the user completed onboarding  

Total number of users:

$$
500
$$

The table:
| Group | Completed onboarding | Did not complete onboarding | Total |
|---|---|---|---|
| Received tutorial | 180 | 70 | 250 |
| No tutorial | 120 | 130 | 250 |
| Total | 300 | 200 | 500 |

---

# Part A — Four disjoint regions

---

## Region 1 — $T \cap C$

### Analysis

$T \cap C$ means:

> received tutorial AND completed onboarding

From the table:

$$
n(T \cap C)=180
$$

### Solution

$$
P(T \cap C)=\frac{180}{500}=0.36
$$

---

## Region 2 — $T \cap C^c$

### Analysis

> received tutorial AND did not complete onboarding

$$
n(T \cap C^c)=70
$$

### Solution

$$
P(T \cap C^c)=\frac{70}{500}=0.14

## Region 3 — $T^c \cap C$

### Analysis

> no tutorial AND completed onboarding

$$
n(T^c \cap C)=120
$$

### Solution

$$
P(T^c \cap C)=\frac{120}{500}=0.24
$$

---

## Region 4 — $T^c \cap C^c$

### Analysis

> no tutorial AND did not complete onboarding

$$
n(T^c \cap C^c)=130
$$

### Solution

$$
P(T^c \cap C^c)=\frac{130}{500}=0.26
$$

---

# Part B — Compute $P(T)$, $P(C)$, $P(T \cup C)$

---

## Compute $P(T)$

$$
P(T)=\frac{250}{500}=0.50
$$

---

## Compute $P(C)$

$$
P(C)=\frac{300}{500}=0.60
$$

---

## Compute $P(T \cup C)$

### Analysis

Use:

$$
P(T \cup C)=1-P(T^c \cap C^c)
$$

### Solution

$$
P(T \cup C)=1-0.26=0.74
$$

---

# Part C — Compute conditional probabilities

---

## $P(C \mid T)$

$$
P(C \mid T)=\frac{180}{250}=0.72
$$

---

## $P(C \mid T^c)$

$$
P(C \mid T^c)=\frac{120}{250}=0.48
$$

---

# Part D — Compute reverse conditionals

---

## $P(T \mid C)$

$$
P(T \mid C)=\frac{180}{300}=0.60
$$

---

## $P(T \mid C^c)$

$$
P(T \mid C^c)=\frac{70}{200}=0.35
$$

---

# Part E — Are $T$ and $C$ independent?

### Check independence condition:

$$
P(C \mid T)=0.72
$$

$$
P(C)=0.60
$$

Since:

$$
0.72 \ne 0.60
$$

### Conclusion

No, $T$ and $C$ are not independent.

---

# Part F — Does receiving the tutorial change completion probability?

### Compare:

$$
P(C \mid T)=0.72
$$

$$
P(C \mid T^c)=0.48
$$

### Conclusion

Yes, receiving the tutorial increases the probability of completing onboarding.

---

# Part G — Difference between $P(C \mid T)$ and $P(T \mid C)$

### $P(C \mid T)$ means:

> Among users who received the tutorial, how many completed onboarding?

### $P(T \mid C)$ means:

> Among users who completed onboarding, how many received the tutorial?
$$

---

# Part H — Interpretation in words
Receiving the tutorial is strongly associated with higher onboarding completion rates. Users who 
receive the tutorial are more likely to complete onboarding, and among those who complete onboarding, a majority had received the tutorial. However, these are different conditional perspectives: 
one measures success given exposure to the tutorial, while the other describes the composition of successful users.
