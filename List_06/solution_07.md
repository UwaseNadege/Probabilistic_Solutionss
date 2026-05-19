# Problem 7 — Conditional probability with three categories

## General setup

Let:

- $H$ = the customer has high activity  
- $M$ = the customer has medium activity  
- $L$ = the customer has low activity  
- $R$ = the customer renewed the subscription  

Total number of customers:

$$
400
$$

The table:

| Activity level | Renewed | Did not renew | Total |
|---|---|---|---|
| High | 80 | 20 | 100 |
| Medium | 90 | 60 | 150 |
| Low | 30 | 120 | 150 |
| Total | 200 | 200 | 400 |

---

# Part A — Explain why $H$, $M$, and $L$ form a partition of the sample space

### Analysis

A partition of the sample space must satisfy two conditions:

1. The events are mutually exclusive.
2. The events together cover the entire sample space.

In this problem:

- every customer belongs to exactly one activity level,
- no customer can belong to more than one activity level at the same time,
- all customers are included in one of the three categories.

### Explanation

Therefore:

$$
H, M, \text{ and } L
$$

form a partition of the sample space.

---

# Part B — Compute $P(H)$

### Analysis

Event $H$ means:

> the customer has high activity.

From the table:

$$
n(H)=100
$$

### Solution (step-by-step)

$$
P(H)=\frac{100}{400}
$$

$$
P(H)=0.25
$$

### Explanation

25% of customers have high activity.

---

# Part C — Compute $P(M)$

### Analysis

Event $M$ means:

> the customer has medium activity.

From the table:

$$
n(M)=150
$$

### Solution (step-by-step)

$$
P(M)=\frac{150}{400}
$$

$$
P(M)=0.375
$$

### Explanation

37.5% of customers have medium activity.

---

# Part D — Compute $P(L)$

### Analysis

Event $L$ means:

> the customer has low activity.

From the table:

$$
n(L)=150
$$

### Solution (step-by-step)

$$
P(L)=\frac{150}{400}
$$

$$
P(L)=0.375
$$

### Explanation

37.5% of customers have low activity.

---

# Part E — Compute $P(R \mid H)$

### Analysis

$P(R \mid H)$ means:

> Probability that a customer renewed the subscription GIVEN that the customer has high activity.

Formula:

$$
P(R \mid H)=\frac{P(R \cap H)}{P(H)}
$$

From the table:

$$
P(R \cap H)=\frac{80}{400}
$$

$$
P(H)=\frac{100}{400}
$$

### Solution (step-by-step)

$$
P(R \mid H)=\frac{80/400}{100/400}
$$

$$
P(R \mid H)=\frac{80}{100}
$$

$$
P(R \mid H)=0.80
$$

### Explanation

Among high-activity customers, 80% renewed their subscription.

---

# Part F — Compute $P(R \mid M)$

### Analysis

$P(R \mid M)$ means:

> Probability that a customer renewed the subscription GIVEN that the customer has medium activity.

Formula:

$$
P(R \mid M)=\frac{P(R \cap M)}{P(M)}
$$

From the table:

$$
P(R \cap M)=\frac{90}{400}
$$

$$
P(M)=\frac{150}{400}
$$

### Solution (step-by-step)

$$
P(R \mid M)=\frac{90/400}{150/400}
$$

$$
P(R \mid M)=\frac{90}{150}
$$

$$
P(R \mid M)=0.60
$$

### Explanation

Among medium-activity customers, 60% renewed their subscription.

---

# Part G — Compute $P(R \mid L)$

### Analysis

$P(R \mid L)$ means:

> Probability that a customer renewed the subscription GIVEN that the customer has low activity.

Formula:

$$
P(R \mid L)=\frac{P(R \cap L)}{P(L)}
$$

From the table:

$$
P(R \cap L)=\frac{30}{400}
$$

$$
P(L)=\frac{150}{400}
$$

### Solution (step-by-step)

$$
P(R \mid L)=\frac{30/400}{150/400}
$$

$$
P(R \mid L)=\frac{30}{150}
$$

$$
P(R \mid L)=0.20
$$

### Explanation

Among low-activity customers, 20% renewed their subscription.

---

# Part H — Use the law of total probability to compute $P(R)$

### Analysis

Since:

$$
H, M, \text{ and } L
$$

form a partition of the sample space, we use the law of total probability:

$$
P(R)=P(R \mid H)P(H)+P(R \mid M)P(M)+P(R \mid L)P(L)
$$

### Solution (step-by-step)

$$
P(R)=(0.80)(0.25)+(0.60)(0.375)+(0.20)(0.375)
$$

$$
P(R)=0.20+0.225+0.075
$$

$$
P(R)=0.50
$$

### Explanation

50% of customers renewed their subscription.

---

# Part I — Compute $P(H \mid R)$

### Analysis

$P(H \mid R)$ means:

> Probability that a customer has high activity GIVEN that the customer renewed the subscription.

Formula:

$$
P(H \mid R)=\frac{P(H \cap R)}{P(R)}
$$

### Solution (step-by-step)

$$
P(H \mid R)=\frac{80/400}{200/400}
$$

$$
P(H \mid R)=\frac{80}{200}
$$

$$
P(H \mid R)=0.40
$$

### Explanation

Among customers who renewed, 40% have high activity.

---

# Part J — Compute $P(M \mid R)$

### Analysis

$P(M \mid R)$ means:

> Probability that a customer has medium activity GIVEN that the customer renewed the subscription.

Formula:

$$
P(M \mid R)=\frac{P(M \cap R)}{P(R)}
$$

### Solution (step-by-step)

$$
P(M \mid R)=\frac{90/400}{200/400}
$$

$$
P(M \mid R)=\frac{90}{200}
$$

$$
P(M \mid R)=0.45
$$

### Explanation

Among customers who renewed, 45% have medium activity.

---

# Part K — Compute $P(L \mid R)$

### Analysis

$P(L \mid R)$ means:

> Probability that a customer has low activity GIVEN that the customer renewed the subscription.

Formula:

$$
P(L \mid R)=\frac{P(L \cap R)}{P(R)}
$$

### Solution (step-by-step)

$$
P(L \mid R)=\frac{30/400}{200/400}
$$

$$
P(L \mid R)=\frac{30}{200}
$$

$$
P(L \mid R)=0.15
$$

### Explanation

Among customers who renewed, 15% have low activity.

---

# Part L — Interpret the difference between $P(R \mid H)$ and $P(H \mid R)$

### Analysis

$$
P(R \mid H)
$$

asks:

> “If a customer has high activity, what is the probability that they renewed?”

while

$$
P(H \mid R)
$$

asks:

> “If a customer renewed, what is the probability that they have high activity?”

The conditions are different, so the probabilities answer different questions.

### Explanation

Conditional probabilities are not symmetric because changing the condition changes the reference group being analyzed.
