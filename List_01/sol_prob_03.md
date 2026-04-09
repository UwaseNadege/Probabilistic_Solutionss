# Task 3 — Drawing Cards

We consider an experiment consisting of drawing cards from a **standard 52-card deck**.

A standard deck contains:

- 4 suits: ♥ ♦ ♣ ♠  
- 13 ranks: A, 2, 3, ..., 10, J, Q, K  

Thus the deck contains

$$
52 = 4 \times 13
$$

distinct cards.

In this task the **order of outcomes matters**, so every outcome must record the **exact sequence of drawn cards**.

---

# 1. Sample Space for Drawing One Card

When drawing **one card**, the possible outcomes are all individual cards in the deck.

We may represent cards as pairs:

$$
(\text{rank}, \text{suit})
$$

Examples include:

- $(A, \spadesuit)$  
- $(10, \heartsuit)$  
- $(Q, \clubsuit)$  

Therefore the sample space is

$$
\Omega_1 = \{\text{all 52 cards of the deck}\}
$$

### Number of elementary outcomes

$$
|\Omega_1| = 52
$$

### Interpretation

An **elementary outcome** represents the **exact card drawn** from the deck.

---

# 2. Sample Space for Two Draws With Replacement

Now consider **two consecutive card draws with replacement**.

**With replacement** means:

- after the first card is drawn,  
- it is **returned to the deck**,  
- the deck again contains **52 cards**.

Thus both draws have **52 possible outcomes**.

### Sample Space

Each outcome is an **ordered pair of cards**:

$$
\Omega_2 =
\{(c_1, c_2) : c_1 \in D, \; c_2 \in D\}
$$

where \(D\) denotes the set of all 52 cards.

Examples:

- $(A\spadesuit, 7\heartsuit)$
- $(K\clubsuit, K\clubsuit)$
- $(3\diamondsuit, J\spadesuit)$

Note that **the same card can appear twice**, because it is replaced before the second draw.

### Number of elementary outcomes

$$
|\Omega_2| = 52 \times 52 = 52^2
$$

$$
|\Omega_2| = 2704
$$

---

# 3. Sample Space for Two Draws Without Replacement

Now consider **two consecutive draws without replacement**.

**Without replacement** means:

- after the first card is drawn,
- it is **not returned to the deck**.

Therefore:

- the first draw has **52 possibilities**
- the second draw has **51 possibilities**

### Sample Space

Each outcome is an **ordered pair of different cards**:

$$
\Omega_2' =
\{(c_1, c_2) : c_1, c_2 \in D,\; c_1 \neq c_2\}
$$

Examples:

- $(A\spadesuit, 7\heartsuit)$
- $(10\clubsuit, Q\diamondsuit)$
- $(5\heartsuit, 5\spadesuit)$

The same **rank may appear twice**, but the **exact same card cannot**, because it is not replaced.

### Number of elementary outcomes

$$
|\Omega_2'| = 52 \times 51
$$

$$
|\Omega_2'| = 2652
$$

---

# 4. Number of Elementary Outcomes

We summarize the results:

| Experiment | Sample Space | Number of Outcomes |
|-------------|-------------|--------------------|
| One draw | $\Omega_1$ | 52 |
| Two draws (with replacement) | $\Omega_2$ | $52^2 = 2704$ |
| Two draws (without replacement) | $\Omega_2'$ | $52 \times 51 = 2652$ |

---

# 5. Meaning of an Elementary Outcome

An **elementary outcome** represents the **exact ordered sequence of drawn cards**.

Examples:

- For **one draw**: the outcome might be  
  $(Q, \heartsuit)$.

- For **two draws with replacement**: the outcome might be  
  $(7\clubsuit, 7\clubsuit)$.

- For **two draws without replacement**: the outcome might be  
  $(K\spadesuit, 3\diamondsuit)$.

Thus an elementary outcome describes:

- **which cards were drawn**, and  
- **in what order they were drawn**.

---

# Key Idea

When performing repeated draws:

- **With replacement:**  

$$
| \Omega_n | = 52^n
$$

- **Without replacement:**  

the number of outcomes decreases because previously drawn cards cannot appear again.
```
