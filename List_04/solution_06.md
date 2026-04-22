# Problem 6 — Final discussion: the axiomatic point of view

## General idea

In the previous problems, we moved through three levels:

1. **Elementary outcomes** (like 1–6 on a die)  
2. **Events as sets of outcomes**  
3. **Frequencies from experiments → probability as a model**

Now we formalize this into an abstract system: **Kolmogorov’s axioms of probability**.

---

# Kolmogorov axioms

A probability space is defined by a function:

$$
P: \mathcal{P}(\Omega) \to [0,1]
$$

satisfying three axioms.

---

## 1. Non-negativity

### Axiom

$$
P(A) \ge 0
$$

### Meaning

No event can have negative probability.

---

### Why this already appeared in our work

From frequencies:

$$
f(A) = \frac{n(A)}{1000}
$$

Since:

- \(n(A) \ge 0\)

we automatically get:

$$
f(A) \ge 0
$$

### Interpretation

In experiments:
- counts are never negative  
- so probabilities derived from them are naturally non-negative  

---

# 2. Normalization

### Axiom

$$
P(\Omega) = 1
$$

### Meaning

Something in the sample space must happen.

---

### Why this appeared in earlier problems

We always observed:

$$
f(1)+f(2)+...+f(6)=1
$$

because:

$$
n(1)+...+n(6)=1000
$$

So:

$$
\frac{1000}{1000}=1
$$

### Interpretation

A complete experiment accounts for all outcomes → total probability is 1.

---

# 3. Finite additivity (disjoint events)

### Axiom

If:

$$
A \cap B = \emptyset
$$

then:

$$
P(A \cup B)=P(A)+P(B)
$$

---

### Why this appeared naturally

In frequency form:

$$
f(A)=\frac{n(A)}{N}
$$

If A and B do not overlap:

$$
n(A \cup B)=n(A)+n(B)
$$

So:

$$
f(A \cup B)=f(A)+f(B)
$$

---

### Interpretation

We can add probabilities ONLY when:
- no outcome is counted twice
- the sets are disjoint

This was exactly what we checked in all earlier problems.

---

# What goes beyond finite experiments

Now comes the key conceptual step.

---

## 4. Countable additivity (σ-additivity)

### Axiom

For infinitely many disjoint events:

$$
A_1, A_2, A_3, ...
$$

with:

$$
A_i \cap A_j = \emptyset \quad (i \ne j)
$$

then:

$$
P\left(\bigcup_{i=1}^{\infty} A_i\right)
$$

$$
\sum_{i=1}^{\infty} P(A_i)
$$

---

## Why this is NOT visible in experiments

In our earlier work:

- we always had a **finite number of outcomes (1–6)**
- or a **finite number of trials (1000)**

So we only ever used:

$$
P(A \cup B) = P(A) + P(B)
$$

for finitely many sets.

---

## Why countable additivity is deeper

### 1. Infinite decomposition

We cannot physically perform:
- infinitely many experiments
- or observe infinitely many disjoint events

---

### 2. Limits instead of direct counting

Countable additivity is a statement about:

- limits
- infinite processes
- theoretical convergence

Not direct data.

---

### 3. Example intuition

Even though we never observe infinite sums directly, we still need it for:

- continuous probability (intervals)
- real analysis models
- advanced stochastic processes

---

## Key distinction

| Finite world (our exercises) | Infinite theory (axioms) |
|----------------------------|--------------------------|
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
