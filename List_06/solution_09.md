# Problem 9 — Law of total probability without a full table

## General setup

Let:

- $W$ = the order came through the website  
- $A$ = the order came through the mobile app  
- $H$ = the order came by phone  
- $C$ = the order is cancelled  

Given:

$$
P(W)=0.50
$$

$$
P(A)=0.35
$$

$$
P(H)=0.15
$$

Cancellation probabilities:

$$
P(C \mid W)=0.04
$$

$$
P(C \mid A)=0.06
$$

$$
P(C \mid H)=0.10
$$

---

# Part A — Explain why $W$, $A$, and $H$ form a partition of the sample space

### Analysis

A partition of the sample space must satisfy two conditions:

1. The events are mutually exclusive.
2. The events together cover the entire sample space.

In this problem:

- every order comes from exactly one channel,
- an order cannot come from more than one channel at the same time,
- all orders come from either the website, mobile app, or phone.

Also:

$$
P(W)+P(A)+P(H)=0.50+0.35+0.15
$$

$$
=1
$$

### Explanation

Therefore:

$$
W, A, \text{ and } H
$$

form a partition of the sample space.

---

# Part B — Use the law of total probability to compute $P(C)$

### Analysis

Since:

$$
W, A, \text{ and } H
$$

form a partition of the sample space, we use the law of total probability:

$$
P(C)=P(C \mid W)P(W)+P(C \mid A)P(A)+P(C \mid H)P(H)
$$

### Solution (step-by-step)

$$
P(C)=(0.04)(0.50)+(0.06)(0.35)+(0.10)(0.15)
$$

$$
P(C)=0.020+0.021+0.015
$$

$$
P(C)=0.056
$$

### Explanation

The probability that an order is cancelled is:

$$
P(C)=0.056
$$

or 5.6%.

---

# Part C — Compute $P(W \mid C)$

### Analysis

$P(W \mid C)$ means:

> Probability that a cancelled order came from the website.

Use Bayes’ formula:

$$
P(W \mid C)=\frac{P(C \mid W)P(W)}{P(C)}
$$

### Solution (step-by-step)

$$
P(W \mid C)=\frac{(0.04)(0.50)}{0.056}
$$

$$
P(W \mid C)=\frac{0.020}{0.056}
$$

$$
P(W \mid C)=0.3571
$$

### Explanation

About 35.7% of cancelled orders came from the website.

---

# Part D — Compute $P(A \mid C)$

### Analysis

$P(A \mid C)$ means:

> Probability that a cancelled order came from the mobile app.

Use Bayes’ formula:

$$
P(A \mid C)=\frac{P(C \mid A)P(A)}{P(C)}
$$

### Solution (step-by-step)

$$
P(A \mid C)=\frac{(0.06)(0.35)}{0.056}
$$

$$
P(A \mid C)=\frac{0.021}{0.056}
$$

$$
P(A \mid C)=0.375
$$

### Explanation

37.5% of cancelled orders came from the mobile app.

---

# Part E — Compute $P(H \mid C)$

### Analysis

$P(H \mid C)$ means:

> Probability that a cancelled order came by phone.

Use Bayes’ formula:

$$
P(H \mid C)=\frac{P(C \mid H)P(H)}{P(C)}
$$

### Solution (step-by-step)

$$
P(H \mid C)=\frac{(0.10)(0.15)}{0.056}
$$

$$
P(H \mid C)=\frac{0.015}{0.056}
$$

$$
P(H \mid C)=0.2679
$$

### Explanation

About 26.8% of cancelled orders came by phone.

---

# Part F — Which channel is most likely among cancelled orders?

### Analysis

Compare:

$$
P(W \mid C)=0.3571
$$

$$
P(A \mid C)=0.375
$$

$$
P(H \mid C)=0.2679
$$

The largest probability is:

$$
P(A \mid C)=0.375
$$

### Conclusion

The mobile app channel is most likely among cancelled orders.

### Explanation

Among cancelled orders, the largest proportion came from the mobile app.

---

# Part G — Is this necessarily the channel with the highest cancellation rate?

### Analysis

The highest cancellation rate is:

$$
P(C \mid H)=0.10
$$

which belongs to phone orders.

However, phone orders make up only:

$$
P(H)=0.15
$$

of all orders.

The mobile app has a lower cancellation rate:

$$
P(C \mid A)=0.06
$$

but a much larger share of total orders:

$$
P(A)=0.35
$$

### Explanation

No, the channel most common among cancelled orders is not necessarily the channel with the highest cancellation rate.

Both the cancellation rate and the size of the group affect the final probability.
