# Task 10 — Normal Distribution  N(μ, σ²)

---

## 1. Experiment Description (Continuous Measurement)

We consider a continuous experiment where we measure a real-valued quantity.

Examples:
- height of students
- measurement error in instruments
- exam scores
- temperature readings

---

### Sample Space

$$
\Omega = \mathbb{R}
$$

---

### Elementary Outcome

An elementary outcome is any real number:

$$
\omega \in \mathbb{R}
$$

---

### Random Variable

We define:

$$
X(\omega) = \omega
$$

So \(X\) represents a continuous measured value.

---

## 2. PDF of Normal Distribution

The probability density function is:

$$
f(x) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)
$$

---

### Parameters:

- \( \mu \): mean (center of distribution)
- \( \sigma^2 \): variance (spread of distribution)

---

## 3. Support

$$
x \in (-\infty, \infty)
$$

---

## 4. Shape of PDF (Parameter Effects)

### (a) Changing mean μ (fixed variance)
- curve shifts left or right
- shape stays the same

---

### (b) Changing variance σ² (fixed mean)
- small σ² → narrow and tall curve
- large σ² → wide and flat curve

---

## 5. CDF of Normal Distribution

$$
F(x) = P(X \le x)
$$

- smooth S-shaped curve
- increases from 0 to 1
- symmetric around μ

---

## 6. Influence of Parameters

### Mean (μ):
- determines location (center of curve)

### Variance (σ²):
- determines spread
- larger variance → more spread out distribution

---

## 7. Probability Calculations

### (a) Cumulative probability

$$
P(X \le a) = F(a)
$$

---

### (b) Tail probability

$$
P(X \ge a) = 1 - F(a)
$$

---

### (c) Interval probability

$$
P(a \le X \le b) = F(b) - F(a)
$$

---

## 8. Standardization (Z-score method)

To compute probabilities:

$$
Z = \frac{X - \mu}{\sigma}
$$

Then:

$$
P(X \le a) = P\left(Z \le \frac{a - \mu}{\sigma}\right)
$$

---

## 9. Why P(X = a) = 0

For continuous distributions:

- probability is area under curve
- a single point has no width

So:

$$
P(X = a) = 0
$$

---

## 10. Practical Applications

The normal distribution is widely used in:

- heights and biological measurements
- measurement errors
- IQ and standardized test scores
- financial returns modeling
- natural phenomena (noise, temperature variations)

---

## 11. Optional Application (Interactive Tool)

A small application can be built to explore normal distributions.

### Features:
- input μ and σ
- plot multiple normal curves on same graph
- compare different means and variances
- display PDF and CDF

### Idea:
- slider for μ (shift curve)
- slider for σ (spread curve)
- real-time comparison of distributions
