# Task 7 — Negative Binomial Distribution

---

## 1. Experiment Description (Until the r-th Success)

We consider an experiment where independent Bernoulli trials are repeated until the **r-th success** occurs.

Each trial has:
- success probability: \( p \)
- failure probability: \( 1 - p \)

---

### Sample Space

The sample space consists of all sequences that end when the r-th success occurs:

$$
\Omega = \{ \text{all sequences of F and S ending at r-th S} \}
$$

Example:
- S S F S F ... (ends at r-th success)

---

### Elementary Outcome

An elementary outcome is:

$$
\omega = (F, S, F, F, S, \dots, S)
$$

---

### Random Variable

We define:

$$
X(\omega) = \text{trial number on which the r-th success occurs}
$$

So:
- X = k means the r-th success happens at trial k

---

## 2. PMF of Negative Binomial Distribution

The probability mass function is:

$$
P(X = k) =
\binom{k-1}{r-1} p^r (1 - p)^{k-r}
$$

---

### Parameters:

- \(r\): number of successes required  
- \(p\): probability of success in each trial  
- \(k\): trial number where r-th success occurs  

---

## 3. Support of X

The support is:

$$
k = r, r+1, r+2, \dots
$$

---

## 4. PMF Graphs (Parameter Effects)

We analyze different parameter choices:

### Changing r:
- larger r → distribution shifts right
- more trials needed on average
- distribution becomes wider

### Changing p:
- larger p → distribution shifts left
- r-th success happens faster
- distribution becomes more concentrated

---

## 5. CDF Graphs

The CDF is:

$$
F(k) = P(X \le k)
$$

- step function
- increases slowly when p is small
- increases quickly when p is large

---

## 6. Effect of Parameters

### (a) Increasing p:
- success becomes more likely
- fewer trials needed
- distribution shifts left

---

### (b) Increasing r:
- more successes required
- more trials needed
- distribution spreads out

---

## 7. Probability Calculations

### (a) Exact probability

$$
P(X = k) =
\binom{k-1}{r-1} p^r (1 - p)^{k-r}
$$

---

### (b) Cumulative probability

$$
P(X \le k) = F(k)
$$

---

### (c) Tail probability

$$
P(X > k) = 1 - F(k)
$$

---

### (d) Interval probability

$$
P(a \le X \le b) = F(b) - F(a - 1)
$$

---

## 8. Relation to Geometric Distribution

The geometric distribution is a special case of the negative binomial distribution:

$$
r = 1
$$

So:
- geometric = time until first success
- negative binomial = time until r-th success

✔ Therefore, geometric is a special case of this model.

---

## 9. Practical Applications

The negative binomial distribution is used in:

- number of attempts until multiple successes
- quality control (multiple defect detections)
- biology (number of trials until r successes)
- sports (number of games until r wins)
- reliability testing (failures before success threshold)

---

## 10. Optional Application (Comparison Tool)

A small application can be built to compare distributions.

### Features:
- input parameters r and p
- plot PMF and CDF
- compare:
  - negative binomial vs geometric
- visualize effect of changing r

### Idea:
- slider for r
- slider for p
- real-time curve updates
