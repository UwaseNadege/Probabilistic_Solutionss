# Task 9 — Gamma Distribution

---

## 1. Experiment Description (Continuous Waiting Time)

We consider a continuous waiting-time experiment where we measure the time until an event occurs.

Examples:
- time until a machine fails
- time until a customer arrives
- time until a system response occurs

---

### Sample Space

$$
\Omega = [0, \infty)
$$

---

### Elementary Outcome

An elementary outcome is any non-negative real number:

$$
\omega \in [0, \infty)
$$

---

### Random Variable

We define:

$$
X(\omega) = \omega
$$

So \(X\) represents the waiting time until an event occurs.

---

## 2. PDF of Gamma Distribution

The probability density function is:

$$
f(x) = \frac{\beta^\alpha}{\Gamma(\alpha)} x^{\alpha - 1} e^{-\beta x}
$$

---

### Parameters:

- \( \alpha > 0 \): shape parameter  
- \( \beta > 0 \): rate parameter  

---

## 3. Support

$$
x \in (0, \infty)
$$

---

## 4. Shape of PDF (Effect of Parameters)

### Changing α (shape):
- small α → highly skewed (right-skewed)
- larger α → more symmetric, bell-shaped

---

### Changing β (rate):
- large β → distribution compressed toward 0
- small β → distribution spreads out

---

## 5. CDF of Gamma Distribution

$$
F(x) = P(X \le x)
$$

- smooth increasing function
- starts at 0 and approaches 1
- no jumps (continuous distribution)

---

## 6. Chi-Square Distribution as Special Case

The chi-square distribution is a special case of the gamma distribution:

$$
\chi^2(k) = \text{Gamma}\left(\alpha = \frac{k}{2}, \beta = \frac{1}{2}\right)
$$

### Meaning:
- chi-square is a gamma distribution with fixed parameters
- used heavily in statistical inference

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

## 8. Why Areas Are Used

Since gamma is continuous:

- probability at a point is zero:

$$
P(X = a) = 0
$$

- probabilities are computed using area under the curve:

$$
P(a \le X \le b) = \int_a^b f(x)\,dx
$$

---

## 9. Practical Applications

### Gamma Distribution:
- waiting times in queueing systems
- reliability and failure modeling
- rainfall accumulation modeling
- insurance claim modeling

---

### Chi-Square Distribution:
- hypothesis testing
- goodness-of-fit tests
- independence tests in statistics
- confidence intervals for variance

---

## 10. Optional Application (Interactive Tool)

A small application can be built to explore Gamma and Chi-square distributions.

### Features:
- input α and β
- compare Gamma vs Chi-square
- plot PDF and CDF
- slider-based parameter control

### Idea:
- dynamic visualization of shape changes
- direct comparison of chi-square as special case
