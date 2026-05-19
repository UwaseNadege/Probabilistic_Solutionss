# Problem 6 — Dependence from data

## General setup

Let:

- $I$ = the parcel is international  
- $D$ = the parcel is delayed  

Total number of parcels:

$$
600
$$

The table:

| Parcel type | Delayed | Not delayed | Total |
|---|---|---|---|
| Domestic | 24 | 376 | 400 |
| International | 36 | 164 | 200 |
| Total | 60 | 540 | 600 |

---

# Part A — Compute $P(I)$

### Analysis

Event $I$ means:

> the parcel is international.

From the table:

$$
n(I)=200
$$

### Solution (step-by-step)

$$
P(I)=\frac{200}{600}
$$

$$
P(I)=0.3333
$$

### Explanation

About 33.3% of parcels are international.

---

# Part B — Compute $P(D)$

### Analysis

Event $D$ means:

> the parcel is delayed.

From the table:

$$
n(D)=60
$$

### Solution (step-by-step)

$$
P(D)=\frac{60}{600}
$$

$$
P(D)=0.10
$$

### Explanation

10% of parcels are delayed.

---

# Part C — Compute $P(I \cap D)$

### Analysis

$I \cap D$ means:

> the parcel is international  
AND
> delayed.

From the table:

$$
n(I \cap D)=36
$$

### Solution (step-by-step)

$$
P(I \cap D)=\frac{36}{600}
$$

$$
P(I \cap D)=0.06
$$

### Explanation

6% of parcels are both international and delayed.

---

# Part D — Compute $P(D \mid I)$

### Analysis

$P(D \mid I)$ means:

> Probability that a parcel is delayed GIVEN that it is international.

Formula:

$$
P(D \mid I)=\frac{P(I \cap D)}{P(I)}
$$

### Solution (step-by-step)

$$
P(D \mid I)=\frac{0.06}{0.3333}
$$

$$
P(D \mid I)=0.18
$$

### Explanation

Among international parcels, 18% are delayed.

---

# Part E — Compute $P(D \mid I^c)$

### Analysis

$I^c$ means “the parcel is not international”, which corresponds to domestic parcels.

So $P(D \mid I^c)$ means:

> Probability that a parcel is delayed GIVEN that it is domestic.

Formula:

$$
P(D \mid I^c)=\frac{P(I^c \cap D)}{P(I^c)}
$$

From the table:

$$
P(I^c \cap D)=\frac{24}{600}
$$

$$
P(I^c)=\frac{400}{600}
$$

### Solution (step-by-step)

$$
P(D \mid I^c)=\frac{0.04}{0.6667}
$$

$$
P(D \mid I^c)=0.06
$$

### Explanation

Among domestic parcels, 6% are delayed.

---

# Part F — Are $I$ and $D$ independent?

### Analysis

Two events are independent if:

$$
P(I \cap D)=P(I)P(D)
$$

Compute:

$$
P(I)P(D)=0.3333 \times 0.10
$$

$$
P(I)P(D)=0.0333
$$

But:

$$
P(I \cap D)=0.06
$$

Since:

$$
0.06 \ne 0.0333
$$

the events are not independent.

### Conclusion

No, $I$ and $D$ are not independent.

### Explanation

The probability of delay changes depending on whether the parcel is international.

---

# Part G — Does international shipping increase the probability of delay?

### Analysis

Compare:

$$
P(D \mid I)=0.18
$$

and

$$
P(D \mid I^c)=0.06
$$

Since:

$$
0.18 > 0.06
$$

international parcels are more likely to be delayed.

### Conclusion

Yes, international shipping increases the probability of delay.

### Explanation

International parcels have an 18% delay rate, while domestic parcels have only a 6% delay rate.

---

# Part H — Compute $P(I \mid D)$

### Analysis

$P(I \mid D)$ means:

> Probability that a parcel is international GIVEN that it is delayed.

Formula:

$$
P(I \mid D)=\frac{P(I \cap D)}{P(D)}
$$

### Solution (step-by-step)

$$
P(I \mid D)=\frac{0.06}{0.10}
$$

$$
P(I \mid D)=0.60
$$

### Explanation

Among delayed parcels, 60% are international.

---

# Part I — Explain the difference between $P(D \mid I)$ and $P(I \mid D)$

### Analysis

$$
P(D \mid I)
$$

asks:

> “If a parcel is international, what is the probability that it is delayed?”

while

$$
P(I \mid D)
$$

asks:

> “If a parcel is delayed, what is the probability that it is international?”

The conditions are different, so the probabilities answer different questions.

### Explanation

Conditional probabilities are not symmetric because changing the condition changes the reference group being analyzed.
