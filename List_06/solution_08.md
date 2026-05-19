# Problem 8 — Bayes’ formula from a table

## General setup

Let:

- $F$ = the transaction is fraudulent  
- $S$ = the transaction is marked suspicious  

Total number of transactions:

$$
10000
$$

The table:

| Transaction type | Marked suspicious | Not marked suspicious | Total |
|---|---|---|---|
| Fraudulent | 98 | 2 | 100 |
| Legitimate | 297 | 9603 | 9900 |
| Total | 395 | 9605 | 10000 |

---

# Part A — Compute $P(F)$

### Analysis

Event $F$ means:

> the transaction is fraudulent.

From the table:

$$
n(F)=100
$$

### Solution (step-by-step)

$$
P(F)=\frac{100}{10000}
$$

$$
P(F)=0.01
$$

### Explanation

Only 1% of all transactions are fraudulent.

---

# Part B — Compute $P(S \mid F)$

### Analysis

$P(S \mid F)$ means:

> Probability that a transaction is marked suspicious GIVEN that it is fraudulent.

Formula:

$$
P(S \mid F)=\frac{P(S \cap F)}{P(F)}
$$

From the table:

$$
P(S \cap F)=\frac{98}{10000}
$$

$$
P(F)=\frac{100}{10000}
$$

### Solution (step-by-step)

$$
P(S \mid F)=\frac{98/10000}{100/10000}
$$

$$
P(S \mid F)=\frac{98}{100}
$$

$$
P(S \mid F)=0.98
$$

### Explanation

The system correctly marks 98% of fraudulent transactions as suspicious.

---

# Part C — Compute $P(S \mid F^c)$

### Analysis

$F^c$ means “the transaction is legitimate”.

So $P(S \mid F^c)$ means:

> Probability that a legitimate transaction is marked suspicious.

Formula:

$$
P(S \mid F^c)=\frac{P(S \cap F^c)}{P(F^c)}
$$

From the table:

$$
P(S \cap F^c)=\frac{297}{10000}
$$

$$
P(F^c)=\frac{9900}{10000}
$$

### Solution (step-by-step)

$$
P(S \mid F^c)=\frac{297/10000}{9900/10000}
$$

$$
P(S \mid F^c)=\frac{297}{9900}
$$

$$
P(S \mid F^c)=0.03
$$

### Explanation

3% of legitimate transactions are incorrectly marked suspicious.

---

# Part D — Use the law of total probability to compute $P(S)$

### Analysis

Use the law of total probability:

$$
P(S)=P(S \mid F)P(F)+P(S \mid F^c)P(F^c)
$$

### Solution (step-by-step)

$$
P(S)=(0.98)(0.01)+(0.03)(0.99)
$$

$$
P(S)=0.0098+0.0297
$$

$$
P(S)=0.0395
$$

### Explanation

About 3.95% of all transactions are marked suspicious.

---

# Part E — Use Bayes’ formula to compute $P(F \mid S)$

### Analysis

$P(F \mid S)$ means:

> Probability that a transaction is fraudulent GIVEN that it was marked suspicious.

Bayes’ formula:

$$
P(F \mid S)=\frac{P(S \mid F)P(F)}{P(S)}
$$

### Solution (step-by-step)

$$
P(F \mid S)=\frac{(0.98)(0.01)}{0.0395}
$$

$$
P(F \mid S)=\frac{0.0098}{0.0395}
$$

$$
P(F \mid S)=0.2481
$$

### Explanation

Among suspicious transactions, about 24.8% are actually fraudulent.

---

# Part F — Among suspicious transactions, are most transactions fraudulent or legitimate?

### Analysis

We computed:

$$
P(F \mid S)=0.2481
$$

This means:

- about 24.8% are fraudulent,
- about 75.2% are legitimate.

### Conclusion

Most suspicious transactions are actually legitimate.

### Explanation

Even though the system detects fraud very well, legitimate transactions still make up the majority of suspicious alerts.

---

# Part G — Why can this happen even if the system detects fraudulent transactions very well?

### Analysis

The system has a very high detection rate:

$$
P(S \mid F)=0.98
$$

However, fraudulent transactions are very rare:

$$
P(F)=0.01
$$

Even a small false positive rate applied to many legitimate transactions produces many suspicious legitimate transactions.

For legitimate transactions:

$$
P(S \mid F^c)=0.03
$$

and there are:

$$
9900
$$

legitimate transactions.

### Explanation

Because legitimate transactions are much more common than fraudulent ones, false alarms from legitimate transactions can outnumber correctly detected fraud cases.

---

# Part H — Explain the role of the base rate $P(F)$

### Analysis

The base rate:

$$
P(F)
$$

represents how common fraudulent transactions are in the overall population.

Here:

$$
P(F)=0.01
$$

which means fraud is very rare.

### Explanation

A very small base rate means that even highly accurate systems can produce many false positives relative to the number of true fraud cases.

This strongly affects:

$$
P(F \mid S)
$$

the probability that a suspicious transaction is actually fraudulent.
