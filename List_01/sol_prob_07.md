# Task 7 — Events and Probabilities in Die Rolling

We refer to **Task 2**, where the sample spaces for **one, two, and three rolls of a fair six-sided die** were defined.

A **fair die** means that each face has the same probability of appearing.

If a sample space contains $n$ elementary outcomes, then the probability of each outcome is

$$P(\omega)=\frac{1}{n}$$

where $\omega$ (omega) denotes an elementary outcome.

---

# 1. Probabilities of Elementary Outcomes

## One Roll

The sample space is

$$\Omega_1=\{1,2,3,4,5,6\}$$

Number of outcomes:

$$|\Omega_1|=6$$

Therefore each outcome has probability

$$P(i)=\frac{1}{6}, \quad i\in\{1,2,3,4,5,6\}$$

---

## Two Rolls

The sample space consists of all ordered pairs:

$$(i,j),\quad i,j\in\{1,2,3,4,5,6\}$$

Number of outcomes:

$$|\Omega_2|=6^2=36$$

Thus each elementary outcome has probability

$$P(\omega)=\frac{1}{36}$$

for every $\omega\in\Omega_2$.

---

## Three Rolls

The sample space consists of all ordered triples:

$$(i,j,k),\quad i,j,k\in\{1,2,3,4,5,6\}$$

Number of outcomes:

$$|\Omega_3|=6^3=216$$

Each elementary outcome therefore has probability

$$P(\omega)=\frac{1}{216}$$

---

# 2. Events for One Die Roll

Sample space:

$$\Omega_1=\{1,2,3,4,5,6\}$$

---

### Event $A_1$ — the result is even

Even numbers are

$$A_1=\{2,4,6\}$$

Probability:

$$P(A_1)=\frac{3}{6}=\frac{1}{2}$$

---

### Event $B_1$ — the result is greater than 4

Possible outcomes:

$$B_1=\{5,6\}$$

Probability:

$$P(B_1)=\frac{2}{6}=\frac{1}{3}$$

---

### Event $C_1$ — the result is at most 3

Possible outcomes:

$$C_1=\{1,2,3\}$$

Probability:

$$P(C_1)=\frac{3}{6}=\frac{1}{2}$$

---

# 3. Events for Two Die Rolls

Sample space size:

$$|\Omega_2|=36$$

---

### Event $A_2$ — the sum equals 7

Possible outcomes:

$$A_2=\{(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)\}$$

Number of outcomes: 6

Probability:

$$P(A_2)=\frac{6}{36}=\frac{1}{6}$$

---

### Event $B_2$ — both results are the same

Possible outcomes:

$$B_2=\{(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)\}$$

Number of outcomes: 6

Probability:

$$P(B_2)=\frac{6}{36}=\frac{1}{6}$$

---

### Event $C_2$ — the sum is at least 10

Possible outcomes:

$$C_2=\{(4,6),(5,5),(6,4),(5,6),(6,5),(6,6)\}$$

Number of outcomes: 6

Probability:

$$P(C_2)=\frac{6}{36}=\frac{1}{6}$$

---

# 4. Events for Three Die Rolls

Sample space size:

$$|\Omega_3|=216$$

---

### Event $A_3$ — the sum equals 10

Possible outcomes include all triples $(i,j,k)$ such that

$$i+j+k=10$$

Examples include:

- $(1,3,6)$
- $(2,2,6)$
- $(2,3,5)$
- $(3,3,4)$

Total number of such outcomes: 27

Probability:

$$P(A_3)=\frac{27}{216}=\frac{1}{8}$$

---

### Event $B_3$ — exactly two rolls give the same number

This means:

- two values are equal
- the third value is different.

Number of such outcomes: 90

Probability:

$$P(B_3)=\frac{90}{216}=\frac{5}{12}$$

---

### Event $C_3$ — the outcomes contain two twos and one three

Possible outcomes:

$$C_3=\{(2,2,3),(2,3,2),(3,2,2)\}$$

Number of outcomes: 3

Probability:

$$P(C_3)=\frac{3}{216}=\frac{1}{72}$$

---

# 5. Additional Event on $\Omega_3$

Define a new event:

Event $D_3$ — **all three rolls are even**.

Even numbers are

$$\{2,4,6\}$$

Thus the possible outcomes are triples consisting only of these numbers.

Number of possibilities:

$$3^3=27$$

Probability:

$$P(D_3)=\frac{27}{216}=\frac{1}{8}$$

---

# Key Idea

For repeated rolls of a **fair die**, all ordered outcomes are equally likely.

If the experiment consists of $n$ rolls, then the number of elementary outcomes is

$$6^n$$

and each elementary outcome has probability

$$P(\omega)=\frac{1}{6^n}$$

Event probabilities are obtained by **counting how many outcomes satisfy the event** and dividing by the **total number of outcomes in the sample space**.
```
