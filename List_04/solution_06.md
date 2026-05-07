## General idea

In the previous problems, we moved through three levels:

1. **Elementary outcomes** (like 1–6 on a die)
2. **Events as sets of outcomes**
3. **Frequencies from experiments → probability as a model**

Now we formalize this into an abstract system: **Kolmogorov's axioms of probability**.

---

# Kolmogorov axioms

A probability space is defined by a function:

$$P: \mathcal{P}(\Omega) \to [0,1]$$

satisfying three axioms.

---

## 1. Non-negativity

### Axiom

$$P(A) \ge 0$$

### Meaning

No event can have negative probability.

### Why this already appeared in our work

From frequencies:

$$f(A) = \frac{n(A)}{1000}$$

Since $n(A) \ge 0$, we automatically get $f(A) \ge 0$.

### Interpretation

Counts are never negative → so probabilities derived from them are naturally non-negative.

---

## 2. Normalization

### Axiom

$$P(\Omega) = 1$$

**Read as:** *"P of Omega equals 1"* — the probability that something in the sample space happens is 100%.

### Why this appeared in earlier problems

We always observed:

$$f(1) + f(2) + \cdots + f(6) = 1$$

because $n(1) + \cdots + n(6) = N$, so $\frac{N}{N} = 1$.

### Interpretation

A complete experiment accounts for all outcomes → total probability is 1.

---

## 3. Finite additivity (disjoint events)

### Axiom

If $A \cap B = \emptyset$ (A and B share no outcomes), then:

$$P(A \cup B) = P(A) + P(B)$$

**Read as:** *"P of A union B equals P of A plus P of B"*

### Why this appeared naturally

If A and B do not overlap: $n(A \cup B) = n(A) + n(B)$, so:

$$f(A \cup B) = f(A) + f(B)$$

### Interpretation

We can add probabilities **only** when the sets are disjoint — no outcome is counted twice.

---

## 4. Countable additivity (σ-additivity) — beyond finite experiments

### Axiom

For infinitely many disjoint events $A_1, A_2, A_3, \ldots$ where $A_i \cap A_j = \emptyset$ for $i \ne j$:

$$P\!\left(\bigcup_{i=1}^{\infty} A_i\right) = \sum_{i=1}^{\infty} P(A_i)$$

**Read as:** *"The probability of the union of A-i from i=1 to infinity, equals the sum of P(A-i) from i=1 to infinity"*

- The **left side** $\bigcup_{i=1}^{\infty} A_i$ means: combine A₁, A₂, A₃, … forever (infinitely many events joined with "or")
- The **right side** $\sum_{i=1}^{\infty} P(A_i)$ means: P(A₁) + P(A₂) + P(A₃) + … (an infinite series)

### Why this is NOT visible in experiments

In our earlier work we always had a **finite number of outcomes** and a **finite number of trials**. You cannot run infinitely many experiments. This axiom is a **theoretical requirement** — needed for:

- continuous probability (e.g. picking a random number in [0,1])
- real analysis models
- advanced stochastic processes

---

## Key distinction

| Finite world (our exercises) | Infinite theory (axioms) |
|------------------------------|--------------------------|
| Finite outcomes | Possibly infinite outcomes |
| Finite additivity | Countable (σ-) additivity |
| Direct counting | Limit-based reasoning |
| Empirical, observable | Theoretical, axiomatic |

---

## Final conclusion

The first three axioms feel natural — we saw them in every experiment:

- **Non-negativity** → counts cannot be negative
- **Normalization** → full sample space sums to 1
- **Finite additivity** → disjoint sets add cleanly

**Countable additivity** is the one step that goes beyond. It cannot be derived from any finite experiment — it is a deliberate mathematical extension that turns probability into a full theory.
