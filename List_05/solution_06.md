# Task 6 — Hypergeometric Distribution

---

## 1. Experiment Description (Sampling Without Replacement)

We consider an experiment where we **draw a sample without replacement** from a finite population.

Example:
- a box contains good and defective items
- we select items randomly without putting them back

---

### Sample Space

The sample space consists of all possible ordered selections of size \(n\):

$$
\Omega = \{\text{all samples of size } n \text{ drawn without replacement}\}
$$

---

### Elementary Outcome

An elementary outcome is a specific sample:

$$
\omega = \{\text{selected items in the sample}\}
$$

---

### Random Variable

We define:

$$
X(\omega) = \text{number of distinguished (special) objects in the sample}
$$

---

## 2. PMF of Hypergeometric Distribution

The probability mass function is:

$$
P(X = k) =
\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

### Parameters:

- \(N\): total population size  
- \(K\): number of distinguished objects in population  
- \(n\): sample size  
- \(k\): number of successes in sample  

---

## 3. Support of X

The support is:

$$
\max(0, n-(N-K)) \le X \le \min(n, K)
$$

---

## 4. PMF Graphs (Parameter Effects)

We plot PMF for different cases:

- changing sample size \(n\)
- changing number of successes \(K\)

### Observation:
- distribution is discrete and bounded
- shape changes depending on sampling constraints

---

## 5. CDF Graphs

The CDF is:

$$
F(x) = P(X \le x)
$$

- step function
- increases only over valid support
- reaches 1 at maximum possible value

---

## 6. Effect of Parameters

### (a) Increasing sample size \(n\)
- distribution spreads out
- expected value increases
- more variability in outcomes

---

### (b) Increasing number of successes \(K\)
- distribution shifts to the right
- probability of larger X increases
- success becomes more likely in sample

---

## 7. Probability Calculations

### (a) Exact probability

$$
P(X = k) =
\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

### (b) Cumulative probability

$$
P(X \le k) = F(k)
$$

---

### (c) Tail probability

$$
P(X \ge k) = 1 - F(k - 1)
$$

---

### (d) Interval probability

$$
P(a \le X \le b) = F(b) - F(a - 1)
$$

---

## 8. Comparison with Binomial Model

### Hypergeometric:
- sampling **without replacement**
- probabilities change after each draw
- dependent trials

### Binomial:
- sampling **with replacement / independent trials**
- constant probability
- independent trials

✔ Hypergeometric is the exact model  
✔ Binomial is an approximation when population is large

---

## 9. Practical Applications

The hypergeometric distribution is used in:

- quality control (defective items in batch)
- card games (drawing cards from deck)
- lottery sampling
- biological sampling (genes in population)
- audit testing (defective vs non-defective items)

---

## 10. Optional Application (Comparison Tool)

A small application can be created to compare:

### Features:
- hypergeometric distribution
- binomial approximation
- input parameters:
  - N, K, n
- compare PMF and CDF side-by-side

### Idea:
- visualize difference between dependent and independent sampling
- show how binomial approximates hypergeometric for large N
