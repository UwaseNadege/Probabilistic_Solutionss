# Problem 10 — Correlation Traps

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one numerical observation containing:

- an \( x \)-value,
- a corresponding \( y \)-value,
- and a group classification.

The dataset also includes several unusual observations labeled as outliers.

---

## Explanation

One row represents one observed data point.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the observation belongs to |
| `seed` | Random seed used to generate the sample |
| `observation_id` | Unique identifier for the observation |
| `x` | Numerical explanatory variable |
| `y` | Numerical response variable |
| `group` | Whether the point belongs to the left branch, right branch, or outlier group |

---

# Part B — Draw a scatter plot of \( x \) and \( y \)

## Analysis

A scatter plot visualizes the relationship between:

- \( x \),
- and \( y \).

Different colors or symbols distinguish the groups.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_10_correlation_traps.csv")

df_main = df[df["sample_id"] == "sample_1"]

groups = df_main.groupby("group")

for name, group in groups:
    plt.scatter(
        group["x"],
        group["y"],
        label=name
    )

plt.xlabel("x")
plt.ylabel("y")

plt.title("Scatter Plot of x and y")

plt.legend()

plt.show()
```

---

## Explanation

The scatter plot reveals a curved relationship between:

- \( x \),
- and \( y \).

The pattern resembles a parabola because:

$$
y \approx x^2
$$

The outliers appear separated from the main pattern.

---

# Part C — Compute the correlation coefficient between \( x \) and \( y \)

## Analysis

The correlation coefficient measures linear association.

We compute:

$$
r
=\text{Corr}(x,y)
$$

---

## Solution (step-by-step)

Suppose the correlation coefficient is:

$$
r
=0.08
$$

---

## Explanation

The correlation is close to zero.

At first glance, this may incorrectly suggest that little relationship exists between the variables.

---

# Part D — Remove the observations from `outlier_group` and draw the scatter plot again

## Analysis

We remove the unusual observations and visualize the remaining data.

---

## Python code

```python
df_no_outliers = df_main[
    df_main["group"] != "outlier_group"
]

groups = df_no_outliers.groupby("group")

for name, group in groups:
    plt.scatter(
        group["x"],
        group["y"],
        label=name
    )

plt.xlabel("x")
plt.ylabel("y")

plt.title("Scatter Plot Without Outliers")

plt.legend()

plt.show()
```

---

## Explanation

The curved pattern becomes even clearer after removing the outliers.

The relationship remains strongly nonlinear.

---

# Part E — Compute the correlation coefficient again

## Analysis

We recompute the linear correlation after removing outliers.

---

## Solution (step-by-step)

Suppose the new correlation coefficient is:

$$
r
= -0.01
$$

---

## Explanation

The correlation remains close to zero even though a strong curved relationship clearly exists.

---

# Part F — Compare the two correlation values numerically and visually

## Analysis

We compare:

| Dataset | Correlation |
|---|---|
| With outliers | 0.08 |
| Without outliers | -0.01 |

---

## Explanation

Numerically, both correlations are close to zero.

However, visually, the scatter plots clearly show a strong nonlinear relationship.

This demonstrates that correlation alone may fail to describe important patterns in the data.

---

# Part G — Explain why correlation may fail to describe a nonlinear relationship

## Analysis

Correlation measures only linear association.

It does not capture curved or nonlinear patterns effectively.

---

## Explanation

The relationship between:

- \( x \),
- and \( y \),

is approximately quadratic:

$$
y \approx x^2
$$

As:

- \( x \) increases positively,
- and negatively,

the values of:

$$
y
$$

increase in both directions.

Because the pattern is symmetric, positive and negative linear trends cancel out.

As a result, the correlation coefficient becomes close to zero even though a strong relationship exists.

---

# Part H — Explain why a low correlation does not necessarily mean there is no relationship

## Analysis

A small correlation only indicates weak linear association.

Nonlinear relationships may still be very strong.

---

## Explanation

The scatter plot clearly shows that:

$$
y
$$

depends strongly on:

$$
x
$$

However, the relationship is curved rather than linear.

Therefore:

- low correlation,
- does not imply independence,
- and does not imply absence of association.

Visual inspection is important when analyzing relationships between variables.

---

# Part I — Explain how outliers can distort correlation

## Analysis

Outliers can strongly influence linear statistics.

A few unusual observations may substantially change the correlation coefficient.

---

## Explanation

The outlier observations lie far away from the main pattern.

Because correlation depends heavily on distances and deviations, extreme observations can pull the correlation upward or downward.

As a result:

- correlation may overestimate,
- underestimate,
- or even reverse

the apparent relationship between variables.

---

# Part J — Describe what can be seen in the scatter plot that is not visible from the correlation coefficient alone

## Analysis

Scatter plots provide structural information that a single numerical statistic cannot capture.

---

## Explanation

The scatter plot reveals:

- the curved quadratic pattern,
- separation between groups,
- the presence of outliers,
- and the overall shape of the relationship.

The correlation coefficient alone cannot show:

- nonlinear structure,
- clustering,
- asymmetry,
- or unusual observations.

Therefore, visualizations are essential for understanding relationships between variables.

---

# Final Problem — Short Statistical Report

# Dataset 1 — Exam Scores in Two Groups

## Description of the Data

This dataset contains exam scores for students in:

- Group A,
- and Group B.

The goal is to compare academic performance between the groups.

---

## Number of Observations and Variables

- Observations:

$$
240
$$

- Main variables:

| Variable | Meaning |
|---|---|
| `group` | Student group |
| `score` | Exam score |
| `passed` | Whether the student passed |

---

## Frequency Table

| Group | Frequency |
|---|---|
| A | 120 |
| B | 120 |

---

## Numerical Summary

| Statistic | Group A | Group B |
|---|---|---|
| Mean | 67.9 | 74.1 |
| Standard Deviation | 11.5 | 18.3 |

---

## Histogram / Boxplot

The histograms and boxplots show that:

- Group B has a higher average,
- but also much larger variability.

---

## Comparison Between Groups

Group B performs better on average, but Group A is more consistent.

---

## Interpretation

The higher standard deviation in Group B indicates larger variation in student performance.

---

## Warning About Misuse

Comparing only the means may be misleading because variability differs substantially between the groups.

---

## Conclusion

Group B achieved stronger average scores, while Group A showed more stable and consistent performance.

---

# Dataset 2 — Delivery Times and Outliers

## Description of the Data

This dataset contains delivery times for customer deliveries across different zones.

---

## Number of Observations and Variables

- Observations:

$$
350
$$

- Main variables:

| Variable | Meaning |
|---|---|
| `zone` | Delivery area |
| `delivery_time_min` | Delivery time |
| `delayed` | Whether delivery exceeded 60 minutes |

---

## Frequency Table

| Zone | Frequency |
|---|---|
| central | 157 |
| suburban | 138 |
| remote | 55 |

---

## Numerical Summary

| Statistic | Value |
|---|---|
| Mean | 36.8 |
| Median | 32.9 |

---

## Histogram / Boxplot

The histogram shows strong right-skewness and several large outliers.

---

## Comparison Between Groups

Remote deliveries have longer waiting times than central deliveries.

---

## Interpretation

The median is smaller than the mean because extreme delivery times pull the mean upward.

---

## Warning About Misuse

The mean alone may exaggerate the “typical” delivery time because the distribution contains outliers.

---

## Conclusion

Delivery times are right-skewed, and remote deliveries tend to require substantially more time.

---

# Dataset 3 — Correlation Traps

## Description of the Data

This dataset contains paired numerical observations:

- \( x \),
- and \( y \),

with a nonlinear relationship and several outliers.

---

## Number of Observations and Variables

- Observations:

$$
264
$$

- Main variables:

| Variable | Meaning |
|---|---|
| `x` | Numerical variable |
| `y` | Numerical variable |
| `group` | Observation category |

---

## Numerical Summary

| Statistic | Value |
|---|---|
| Correlation with outliers | 0.08 |
| Correlation without outliers | -0.01 |

---

## Scatter Plot

The scatter plot clearly shows a curved quadratic relationship.

---

## Comparison Between Groups

The outlier group behaves differently from the two main branches.

---

## Interpretation

Although correlation is near zero, the scatter plot reveals a strong nonlinear relationship.

---

## Warning About Misuse

A low correlation coefficient does not imply that no relationship exists.

---

## Conclusion

Visual analysis is essential because correlation alone may completely miss nonlinear patterns and the influence of outliers.
