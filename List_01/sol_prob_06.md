# Task 6 — Events and Probabilities in Coin Tossing

We refer to **Task 1**, where the sample spaces for **one, two, and three coin tosses** were defined.

The coin is assumed to be **fair**, meaning:

- Heads ($H$) and Tails ($T$) are equally likely.
- Every **elementary outcome** in the sample space has the **same probability**.

If a sample space contains $n$ elementary outcomes, then the probability of each outcome is

$$P(\omega)=\frac{1}{n}$$

where $\omega$ denotes an elementary outcome.

---

# 1. Probabilities of Elementary Outcomes

## One Toss

The sample space is

$$\Omega_1=\{H,T\}$$

Number of outcomes:

$$|\Omega_1|=2$$

Therefore each outcome has probability

$$P(H)=\frac{1}{2}, \quad P(T)=\frac{1}{2}$$

---

## Two Tosses

The sample space is

$$\Omega_2=\{(H,H),(H,T),(T,H),(T,T)\}$$

Number of outcomes:

$$|\Omega_2|=4$$

Thus each outcome has probability

$$P(\omega)=\frac{1}{4}$$

for every $\omega \in \Omega_2$.

---

## Three Tosses

The sample space is

$$\Omega_3=\{(H,H,H),(H,H,T),(H,T,H),(H,T,T),(T,H,H),(T,H,T),(T,T,H),(T,T,T)\}$$

Number of outcomes:

$$|\Omega_3|=8$$

Each elementary outcome therefore has probability

$$P(\omega)=\frac{1}{8}$$

---

# 2. Events for One Coin Toss

Sample space:

$$\Omega_1=\{H,T\}$$

---

### Event $A_1$ — the result is heads

$$A_1=\{H\}$$

Probability:

$$P(A_1)=\frac{1}{2}$$

---

### Event $B_1$ — the result is tails

$$B_1=\{T\}$$

Probability:

$$P(B_1)=\frac{1}{2}$$

---

### Event $C_1$ — the result is not tails

This means the result must be **heads**.

$$C_1=\{H\}$$

Probability:

$$P(C_1)=\frac{1}{2}$$

---

# 3. Events for Two Coin Tosses

Sample space:

$$\Omega_2=\{(H,H),(H,T),(T,H),(T,T)\}$$

---

### Event $A_2$ — exactly one head occurs

Possible outcomes:

$$A_2=\{(H,T),(T,H)\}$$

Probability:

$$P(A_2)=\frac{2}{4}=\frac{1}{2}$$

---

### Event $B_2$ — at least one head occurs

Possible outcomes:

$$B_2=\{(H,H),(H,T),(T,H)\}$$

Probability:

$$P(B_2)=\frac{3}{4}$$

---

### Event $C_2$ — both tosses give the same result

Possible outcomes:

$$C_2=\{(H,H),(T,T)\}$$

Probability:

$$P(C_2)=\frac{2}{4}=\frac{1}{2}$$

---

# 4. Events for Three Coin Tosses

Sample space:

$$
\Omega_3=
\{(H,H,H),(H,H,T),(H,T,H),(H,T,T),
(T,H,H),(T,H,T),(T,T,H),(T,T,T)\}
$$

---

### Event $A_3$ — exactly two heads occur

Possible outcomes:

$$A_3=\{(H,H,T),(H,T,H),(T,H,H)\}$$

Probability:

$$P(A_3)=\frac{3}{8}$$

---

### Event $B_3$ — at least one tail occurs

This includes all outcomes except $(H,H,H)$.

$$B_3=\Omega_3\setminus\{(H,H,H)\}$$

Probability:

$$P(B_3)=\frac{7}{8}$$

---

### Event $C_3$ — all three tosses give the same result

Possible outcomes:

$$C_3=\{(H,H,H),(T,T,T)\}$$

Probability:

$$P(C_3)=\frac{2}{8}=\frac{1}{4}$$

---

# 5. Additional Event on $\Omega_3$

Define an additional event:

Event $D_3$ — **exactly one head occurs**.

Possible outcomes:

$$D_3=\{(H,T,T),(T,H,T),(T,T,H)\}$$

Probability:

$$P(D_3)=\frac{3}{8}$$

---

# Key Idea

When tossing a **fair coin multiple times**, all sequences are equally likely.

If the sample space contains $2^n$ outcomes for $n$ tosses, then each outcome has probability

$$P(\omega)=\frac{1}{2^n}$$

Event probabilities are then computed by counting the **number of outcomes belonging to the event** and dividing by the **total number of outcomes in the sample space**.
```
