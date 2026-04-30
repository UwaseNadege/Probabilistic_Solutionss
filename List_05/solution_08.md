# Task 8 — Beta Distribution

---

## 1. Experiment Description (Continuous on [0,1])

We consider a continuous experiment where outcomes are values between 0 and 1.

---

### Sample Space

$$
\Omega = [0,1]
$$

---

### Elementary Outcome

An elementary outcome is any real number in the interval:

$$
\omega \in [0,1]
$$

---

### Random Variable

We define:

$$
X(\omega) = \omega
$$

So the random variable is simply the identity function on \([0,1]\).

---

## 2. PDF of Beta Distribution

The probability density function is:

$$
f(x) = \frac{x^{\alpha - 1}(1-x)^{\beta - 1}}{B(\alpha,\beta)}
$$

---

### Parameters:

- \( \alpha > 0 \)
- \( \beta > 0 \)

where \(B(\alpha,\beta)\) is the Beta function (normalization constant).

---

## 3. Support

The support is:

$$
x \in (0,1)
$$

---

## 4. Shape of PDF (Parameter Effects)

We consider different cases:

### (a) Symmetric distribution
- \( \alpha = \beta \)
- bell-shaped around 0.5

---

### (b) Skewed to the right
- \( \alpha < \beta \)
- more mass near 0

---

### (c) Skewed to the left
- \( \alpha > \beta \)
- more mass near 1

---

### (d) Concentrated at endpoints
- small parameters (\(\alpha < 1\), \(\beta < 1\))
- U-shaped distribution

---

## 5. CDF of Beta Distribution

The cumulative distribution function is:

$$
F(x) = P(X \le x)
$$

- increases smoothly from 0 to 1
- no jumps (continuous distribution)
- shape depends on \(\alpha, \beta\)

---

## 6. Effect of Parameters

### Increasing α:
- shifts density toward 1
- CDF rises faster near 1

### Increasing β:
- shifts density toward 0
- CDF rises faster near 0

### Small α and β:
- more weight near edges (U-shape)

---

## 7. Probability Calculations

### (a) Cumulative probability

$$
P(X \le a) = F(a)
$$

---

### (b) Greater than probability

$$
P(X \ge a) = 1 - F(a)
$$

---

### (c) Interval probability

$$
P(a \le X \le b) = F(b) - F(a)
$$

---

## 8. Why We Use Areas (Continuous Case)

For continuous distributions:

- probability at a single point is zero:

$$
P(X = a) = 0
$$

- probabilities are computed using **areas under the PDF**

So:

$$
P(a \le X \le b) = \int_a^b f(x)\,dx
$$

---

## 9. Practical Applications of Beta Distribution

The beta distribution is used for modeling probabilities and proportions:

- Bayesian statistics (prior distributions)
- machine learning (probability modeling)
- success rates (click-through rates, conversion rates)
- quality control (fraction defective items)
- project completion probabilities

---

## 10. Optional Application (Interactive Tool)

A small interactive tool can be built for exploration.

### Features:
- input parameters α and β
- display PDF curve
- display CDF curve
- compare multiple shapes
- real-time updates using sliders

### Idea:
- slider for α
- slider for β
- dynamic curve visualization
