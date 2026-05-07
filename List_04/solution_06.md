# Problem 6 — Final discussion: the axiomatic point of view

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

Say it like: *"P maps the power set of Omega into the interval zero to one"* — meaning every event gets assigned a number between 0 and 1.

---

## 1. Non-negativity

### Axiom

$$P(A) \ge 0$$

*"P of A is greater than or equal to zero"* — no event gets a negative probability.

---

### Why this already appeared in our work

From frequencies:

$$f(A) = \frac{n(A)}{1000}$$

Since $n(A) \ge 0$ — a count can never be negative — we automatically get:

$$f(A) \ge 0$$

### Interpretation

In experiments, counts are never negative, so probabilities derived from them are naturally non-negative. The axiom just locks that in forever.

---

## 2. Normalization

### Axiom

$$P(\Omega) = 1$$

*"P of Omega equals one"* — Omega is the whole sample space, so this says the probability that **something** happens is 1, i.e. 100%.

---

### Why this appeared in earlier problems

We always observed:

$$f(1) + f(2) + \cdots + f(6) = 1$$

because:

$$n(1) + \cdots + n(6) = 1000 \implies \frac{1000}{1000} = 1$$

### Interpretation

A complete experiment always lands somewhere in Omega → total probability is 1. Nothing mysterious, just saying the experiment always produces *some* outcome.

---

## 3. Finite additivity (disjoint events)

### Axiom

If:

$$A \cap B = \emptyset$$

*"A intersect B equals the empty set"* — meaning A and B share no outcomes, they can never happen at the same time.

Then:

$$P(A \cup B) = P(A) + P(B)$$

*"P of A union B equals P of A plus P of B"* — the ∪ symbol means "or", so this is the probability of A **or** B happening.

---

### Why this appeared naturally

In frequency form, if A and B do not overlap:

$$n(A \cup B) = n(A) + n(B)$$

So:

$$f(A \cup B) = f(A) + f(B)$$

### Interpretation

We can add probabilities **only** when the sets are disjoint — otherwise we'd be counting the same outcomes twice. This is exactly what we verified in every earlier problem.

---

# What goes beyond finite experiments

Now comes the key conceptual step.

---

## 4. Countable additivity (σ-additivity)

### Axiom

For infinitely many disjoint events $A_1, A_2, A_3, \ldots$ — where none of them overlap:

$$A_i \cap A_j = \emptyset \quad (i \ne j)$$

then:

$$P\!\left(\bigcup_{i=1}^{\infty} A_i\right) = \sum_{i=1}^{\infty} P(A_i)$$

The **left side** — *"P of the union of A-i from i equals 1 to infinity"*:
- the big ⋃ is just the ∪ symbol stretched out, meaning "combine all of these"
- so it's asking: what is the probability of A₁ **or** A₂ **or** A₃ **or** … happening, going on forever?

The **right side** — *"the sum of P of A-i from i equals 1 to infinity"*:
- Σ (Sigma) means "add them all up"
- so it's P(A₁) + P(A₂) + P(A₃) + … going on forever
- this is an infinite series, like in calculus

**The whole thing says:** same idea as finite additivity, just stretched to infinitely many non-overlapping events.

---

## Why this is NOT visible in experiments

In our earlier work:
- we always had a **finite number of outcomes (1–6)**
- or a **finite number of trials (1000)**

So we only ever used:

$$P(A \cup B) = P(A) + P(B)$$

for finitely many sets. No experiment can run infinitely many trials — so this axiom is **not something we observed**, it's something we *choose* to require.

---

## Why countable additivity is deeper

### 1. Infinite decomposition

We cannot physically perform infinitely many experiments or observe infinitely many disjoint events.

### 2. Limits instead of direct counting

Countable additivity is a statement about limits and infinite processes — not direct data from a table of counts.

### 3. Where we actually need it

Even though we never see infinite sums in a lab, the theory needs this for:
- continuous probability (e.g. picking a random point in an interval)
- real analysis models
- advanced stochastic processes

Without it, you simply cannot assign probabilities to things like "X lands somewhere between 0.3 and 0.7."

---

## Key distinction

| Finite world (our exercises) | Infinite theory (axioms) |
|------------------------------|--------------------------|
| finite outcomes | possibly infinite outcomes |
| finite additivity | countable additivity |
| direct counting | limit-based reasoning |

---

# Final synthesis

The axioms of probability arise naturally from our earlier work:

- **Non-negativity** → counts cannot be negative
- **Normalization** → full sample space sums to 1
- **Finite additivity** → disjoint sets can be added without overlap

However:

- **Countable additivity** is not visible in finite experiments
- it extends probability into an infinite, abstract setting
- it is a theoretical requirement, not an empirical one

---

# Final conclusion

Probability theory starts from simple counting in experiments, but becomes a full mathematical theory only when we generalize:

- from finite observations
- to infinite, structured systems

The Kolmogorov axioms formalize exactly this transition.
