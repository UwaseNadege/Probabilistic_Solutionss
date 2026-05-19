# Problem 5 — Independence from data

## General setup

Let:

- $A$ = the user has a premium account  
- $M$ = the user watched a movie during the weekend  

Total number of users:

$$
200
$$

The table:

| Account type | Watched a movie | Did not watch a movie | Total |
|---|---|---|---|
| Premium | 84 | 36 | 120 |
| Free | 56 | 24 | 80 |
| Total | 140 | 60 | 200 |

---

# Part A — Compute $P(A)$

### Analysis

Event $A$ means:

> the user has a premium account.

From the table:

$$
n(A)=120
$$

### Solution (step-by-step)

$$
P(A)=\frac{120}{200}
$$

$$
P(A)=0.60
$$

### Explanation

60% of users have a premium account.

---

# Part B — Compute $P(M)$

### Analysis

Event $M$ means:

> the user watched a movie during the weekend.

From the table:

$$
n(M)=140
$$

### Solution (step-by-step)

$$
P(M)=\frac{140}{200}
$$

$$
P(M)=0.70
$$

### Explanation

70% of users watched a movie during the weekend.

---

# Part C — Compute $P(A \cap M)$

### Analysis

$A \cap M$ means:

> the user has a premium account  
AND
> watched a movie during the weekend.

From the table:

$$
n(A \cap M)=84
$$

### Solution (step-by-step)

$$
P(A \cap M)=\frac{84}{200}
$$

$$
P(A \cap M)=0.42
$$

### Explanation

42% of users both have a premium account and watched a movie during the weekend.

---

# Part D — Compute $P(M \mid A)$

### Analysis

$P(M \mid A)$ means:

> Probability that a user watched a movie GIVEN that the user has a premium account.

Formula:

$$
P(M \mid A)=\frac{P(A \cap M)}{P(A)}
$$

### Solution (step-by-step)

$$
P(M \mid A)=\frac{0.42}{0.60}
$$

$$
P(M \mid A)=0.70
$$

### Explanation

Among premium users, 70% watched a movie during the weekend.

---

# Part E — Compute $P(M \mid A^c)$

### Analysis

$A^c$ means “the user does not have a premium account”, which corresponds to free users.

So $P(M \mid A^c)$ means:

> Probability that a user watched a movie GIVEN that the user has a free account.

Formula:

$$
P(M \mid A^c)=\frac{P(A^c \cap M)}{P(A^c)}
$$

From the table:

$$
P(A^c \cap M)=\frac{56}{200}
$$

$$
P(A^c)=\frac{80}{200}
$$

### Solution (step-by-step)

$$
P(M \mid A^c)=\frac{0.28}{0.40}
$$

$$
P(M \mid A^c)=0.70
$$

### Explanation

Among free users, 70% watched a movie during the weekend.

---

# Part F — Decide whether $A$ and $M$ are independent

### Analysis

Two events are independent if:

$$
P(A \cap M)=P(A)P(M)
$$

Compute:

$$
P(A)P(M)=0.60 \times 0.70
$$

$$
P(A)P(M)=0.42
$$

Now compare with:

$$
P(A \cap M)=0.42
$$

Since:

$$
P(A \cap M)=P(A)P(M)
$$

the events are independent.

### Conclusion

Yes, $A$ and $M$ are independent.

---

# Part G — Explain in words what independence means in this situation

### Analysis

Independence means that knowing whether a user has a premium account does not change the probability that the user watched a movie during the weekend.

We can see this because:

$$
P(M \mid A)=0.70
$$

and

$$
P(M \mid A^c)=0.70
$$

Both probabilities are the same.

### Explanation

Having a premium account does not affect whether users watched a movie during the weekend.
