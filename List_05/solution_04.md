# Task 4 — Geometric Distribution

---

## 1. Experiment Description (Repeated Trials Until First Success)

We consider a process where we repeat independent Bernoulli trials until the **first success occurs**.

Each trial has:
- Success probability: \( p \)
- Failure probability: \( 1 - p \)

---

### Sample Space

The sample space consists of all possible sequences that end with the first success:

$$
\Omega = \{ S,\; FS,\; FFS,\; FFFS,\; \dots \}
$$

---

### Elementary Outcome

An elementary outcome is:

$$
\omega = (F, F, F, \dots, S)
$$

---

### Random Variable

We define:

$$
X(\omega) = \text{trial number on which the first success occurs}
$$

So:
- X = 1 → success on first trial  
- X = 2 → first success after 1 failure  
- X = 3 → first success after 2 failures  
- etc.

---

## 2. PMF of Geometric Distribution

The probability mass function is:

$$
P(X = k) = (1 - p)^{k-1} p
$$

---

## 3. CDF of Geometric Distribution

The cumulative distribution function is:

$$
F(k) = P(X \le k) = 1 - (1 - p)^k
$$

---

## 4. Support of X

The support is:

$$
\{1, 2, 3, 4, \dots\}
$$

### Why infinite?
Because in theory, we may keep failing forever before the first success occurs.

---

## 5. PMF Graphs (Effect of p)

We plot PMF for different values of p:

- small p → slow decay (long waiting time)
- large p → steep drop (quick success)

### Behavior:
- p small → distribution spreads out
- p large → values concentrate near 1

---

## 6. CDF Graphs (Effect of p)

The CDF:

$$
F(k) = 1 - (1 - p)^k
$$

### Behavior:
- p large → CDF rises quickly to 1
- p small → CDF rises slowly

---

## 7. Effect of Parameter p

### When p increases:
- success becomes more likely
- X tends to be smaller
- PMF shifts left
- CDF rises faster

---

### When p decreases:
- success becomes less likely
- X tends to be larger
- PMF spreads out
- CDF rises slowly

---

## 8. Probability Calculations

### (a) Exact probability

$$
P(X = k) = (1 - p)^{k-1} p
$$

---

### (b) Cumulative probability

$$
P(X \le k) = 1 - (1 - p)^k
$$

---

### (c) Tail probability

$$
P(X > k) = (1 - p)^k
$$

---

### (d) Interval probability

$$
P(a \le X \le b) = F(b) - F(a-1)
$$

---

## 9. Interpretation of Tail Probabilities

The tail probability:

$$
P(X > k)
$$

represents:

👉 the probability that we still have NOT obtained a success after k trials  
👉 i.e., the waiting time is longer than k

So it measures **how long we might have to wait**.

---

## 10. Practical Applications

The geometric distribution is used when modeling:

- number of attempts until first success
- number of coin flips until first head
- number of quality checks until first defective item
- number of calls until first answer
- machine failure detection timing

---

## 11. Optional Application Extension

This distribution can be added to the previous interactive tool.

### Features:
- input parameter p
- display PMF graph
- display CDF graph
- compare different values of p
- compare geometric vs binomial distributions

### Idea:
- slider for p
- dynamic update of curves
