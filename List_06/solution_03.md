# Problem 3 — Conditional probabilities are not symmetric

## General setup

Let:

- $W$ = the user watched the lecture  
- $Q$ = the user passed the quiz  

Total number of users:

$$
150
$$

The table:

| User behavior | Passed quiz | Did not pass quiz | Total |
|---|---|---|---|
| Watched lecture | 72 | 18 | 90 |
| Did not watch lecture | 28 | 32 | 60 |
| Total | 100 | 50 | 150 |

---

# Part A — Compute $P(Q \mid W)$

### Analysis

$P(Q \mid W)$ means:

> Probability that a user passed the quiz GIVEN that the user watched the lecture.

Formula:

$$
P(Q \mid W)=\frac{P(Q \cap W)}{P(W)}
$$

From the table:

$$
P(Q \cap W)=\frac{72}{150}
$$

$$
P(W)=\frac{90}{150}
$$

### Solution (step-by-step)

$$
P(Q \mid W)=\frac{72/150}{90/150}
$$

$$
P(Q \mid W)=\frac{72}{90}
$$

$$
P(Q \mid W)=0.80
$$

### Explanation

Among users who watched the lecture, 80% passed the quiz.

---

# Part B — Compute $P(W \mid Q)$

### Analysis

$P(W \mid Q)$ means:

> Probability that a user watched the lecture GIVEN that the user passed the quiz.

Formula:

$$
P(W \mid Q)=\frac{P(W \cap Q)}{P(Q)}
$$

From the table:

$$
P(W \cap Q)=\frac{72}{150}
$$

$$
P(Q)=\frac{100}{150}
$$

### Solution (step-by-step)

$$
P(W \mid Q)=\frac{72/150}{100/150}
$$

$$
P(W \mid Q)=\frac{72}{100}
$$

$$
P(W \mid Q)=0.72
$$

### Explanation

Among users who passed the quiz, 72% watched the lecture.

---

# Part C — Compute $P(Q \mid W^c)$

### Analysis

$W^c$ means “did not watch the lecture”.

So $P(Q \mid W^c)$ means:

> Probability that a user passed the quiz GIVEN that the user did not watch the lecture.

Formula:

$$
P(Q \mid W^c)=\frac{P(Q \cap W^c)}{P(W^c)}
$$

From the table:

$$
P(Q \cap W^c)=\frac{28}{150}
$$

$$
P(W^c)=\frac{60}{150}
$$

### Solution (step-by-step)

$$
P(Q \mid W^c)=\frac{28/150}{60/150}
$$

$$
P(Q \mid W^c)=\frac{28}{60}
$$

$$
P(Q \mid W^c)=0.4667
$$

### Explanation

Among users who did not watch the lecture, about 46.7% passed the quiz.

---

# Part D — Compute $P(W \mid Q^c)$

### Analysis

$Q^c$ means “did not pass the quiz”.

So $P(W \mid Q^c)$ means:

> Probability that a user watched the lecture GIVEN that the user did not pass the quiz.

Formula:

$$
P(W \mid Q^c)=\frac{P(W \cap Q^c)}{P(Q^c)}
$$

From the table:

$$
P(W \cap Q^c)=\frac{18}{150}
$$

$$
P(Q^c)=\frac{50}{150}
$$

### Solution (step-by-step)

$$
P(W \mid Q^c)=\frac{18/150}{50/150}
$$

$$
P(W \mid Q^c)=\frac{18}{50}
$$

$$
P(W \mid Q^c)=0.36
$$

### Explanation

Among users who did not pass the quiz, 36% watched the lecture.

---

# Part E — Why do $P(Q \mid W)$ and $P(W \mid Q)$ answer different questions?

### Analysis

Conditional probabilities depend on the condition after the vertical bar.

$$
P(Q \mid W)
$$

asks:

> “Among users who watched the lecture, how many passed the quiz?”

while

$$
P(W \mid Q)
$$

asks:

> “Among users who passed the quiz, how many watched the lecture?”

The groups being examined are different.

### Explanation

Conditional probability is not symmetric because changing the condition changes the reference group.

---

# Part F — Which probability is more useful if we want to know whether watching the lecture helps?

### Analysis

To measure whether watching helps, we should compare quiz performance among users who watched the lecture.

Therefore, the useful probability is:

$$
P(Q \mid W)
$$

and also compare it with:

$$
P(Q \mid W^c)
$$

### Explanation

These probabilities show how likely users are to pass depending on whether they watched the lecture.

Since:

$$
P(Q \mid W)=0.80
$$

and

$$
P(Q \mid W^c)=0.4667
$$

watching the lecture appears to improve quiz performance.

---

# Part G — Which probability is more useful if we want to describe users who passed the quiz?

### Analysis

If we want to describe users who passed the quiz, we focus on the group of users who passed.

Therefore, the useful probability is:

$$
P(W \mid Q)
$$

### Explanation

This probability tells us what proportion of successful users watched the lecture.
