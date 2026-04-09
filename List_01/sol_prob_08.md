# Task 8 — Events and Probabilities in Card Drawing

We refer to **Task 3**, where the sample spaces for drawing cards from a **standard 52-card deck** were defined.

A standard deck contains:

- 52 cards  
- 4 suits: Hearts, Diamonds, Clubs, Spades  
- 13 ranks: A,2,3,4,5,6,7,8,9,10,J,Q,K

If a sample space contains $n$ **equally likely elementary outcomes**, then

$$
P(\omega)=\frac{1}{n}
$$

where $\omega$ is an elementary outcome.

---

# 1. Probabilities of Elementary Outcomes

## One Card Drawn

The sample space contains all 52 cards:

$$
\Omega_1 = \{\text{all 52 cards}\}
$$

Number of outcomes:

$$
|\Omega_1| = 52
$$

Each card therefore has probability

$$
P(\omega)=\frac{1}{52}
$$

---

## Two Cards Drawn (with replacement)

Two ordered draws are performed, and the first card is returned to the deck before the second draw.

The sample space consists of ordered pairs:

$$
(c_1,c_2)
$$

where each $c_i$ can be any of the 52 cards.

Number of outcomes:

$$
|\Omega_2| = 52 \times 52 = 2704
$$

Each outcome therefore has probability

$$
P(\omega)=\frac{1}{2704}
$$

---

## Two Cards Drawn (without replacement)

Two ordered draws are performed, but the first card is **not returned**.

Thus the second draw has only **51 possible cards**.

Number of outcomes:

$$
|\Omega_2'| = 52 \times 51 = 2652
$$

Each elementary outcome therefore has probability

$$
P(\omega)=\frac{1}{2652}
$$

---

# 2. Events for One Card Drawn

Sample space:

$$
\Omega_1
$$

---

### Event $A_1$ — the card is a heart

There are 13 hearts in the deck.

$$
A_1 = \{\text{all heart cards}\}
$$

Probability:

$$
P(A_1)=\frac{13}{52}=\frac{1}{4}
$$

---

### Event $B_1$ — the card is a king

There are 4 kings.

$$
B_1=\{\text{four kings}\}
$$

Probability:

$$
P(B_1)=\frac{4}{52}=\frac{1}{13}
$$

---

### Event $C_1$ — the card is not a face card

Face cards are:

- Jack
- Queen
- King

There are:

$$
3 \times 4 = 12
$$

face cards.

Thus the number of non-face cards is

$$
52-12=40
$$

Probability:

$$
P(C_1)=\frac{40}{52}=\frac{10}{13}
$$

---

# 3. Events for Two Cards Drawn (With Replacement)

Sample space size:

$$
|\Omega_2|=2704
$$

---

### Event $A_2$ — both cards are hearts

Probability for one heart:

$$
\frac{13}{52}=\frac{1}{4}
$$

Since draws are independent:

$$
P(A_2)=\frac{1}{4}\cdot\frac{1}{4}=\frac{1}{16}
$$

---

### Event $B_2$ — both cards have the same rank

Choose any rank first.  
For the second card there are **4 cards with that rank**.

Probability:

$$
P(B_2)=\frac{4}{52}=\frac{1}{13}
$$

---

### Event $C_2$ — at least one card is an ace

Use the complement event: **no ace appears**.

Probability of not drawing an ace:

$$
\frac{48}{52}
$$

Thus

$$
P(\text{no ace})=
\left(\frac{48}{52}\right)^2
$$

Therefore

$$
P(C_2)=1-\left(\frac{48}{52}\right)^2
\approx 0.148
$$

---

# 4. Events for Two Cards Drawn (Without Replacement)

Sample space size:

$$
|\Omega_2'|=2652
$$

---

### Event $A_3$ — both cards are hearts

First heart:

$$
\frac{13}{52}
$$

Second heart:

$$
\frac{12}{51}
$$

Therefore

$$
P(A_3)=\frac{13}{52}\cdot\frac{12}{51}
=\frac{1}{17}
$$

---

### Event $B_3$ — both cards have the same rank

After drawing the first card, there are **3 remaining cards with the same rank**.

Probability:

$$
P(B_3)=\frac{3}{51}
=\frac{1}{17}
$$

---

### Event $C_3$ — one king and one queen (any order)

There are:

- 4 kings
- 4 queens

Two possible orders:

1. King then Queen
2. Queen then King

Probability:

$$
P(K,Q)=\frac{4}{52}\cdot\frac{4}{51}
$$

$$
P(Q,K)=\frac{4}{52}\cdot\frac{4}{51}
$$

Total probability:

$$
P(C_3)=2\cdot\frac{4}{52}\cdot\frac{4}{51}
=\frac{32}{2652}
=\frac{8}{663}
$$

---

# 5. Additional Event on $\Omega_2'$

Define a new event:

Event $D_3$ — **both cards are aces**.

First draw:

$$
\frac{4}{52}
$$

Second draw:

$$
\frac{3}{51}
$$

Probability:

$$
P(D_3)=\frac{4}{52}\cdot\frac{3}{51}
=\frac{12}{2652}
=\frac{1}{221}
$$

---

# Key Idea

When drawing cards:

- **With replacement** → draws are **independent**.
- **Without replacement** → probabilities change after each draw.

The number of elementary outcomes depends on whether the **deck is restored between draws or not**, which directly affects the probability calculations.
```
