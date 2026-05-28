# Problem 8 — Waiting Times and Empirical CDF

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one service ticket handled by the system.

The dataset records:

- which sample the ticket belongs to,
- which random seed generated the sample,
- the ticket ID,
- the type of service,
- the waiting time in minutes,
- and whether the ticket was resolved within 10 minutes.

---

## Explanation

One row represents one service request.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the ticket belongs to |
| `seed` | Random seed used to generate the sample |
| `ticket_id` | Unique identifier for the ticket |
| `service_type` | Whether the ticket is standard or priority |
| `waiting_time_min` | Waiting time in minutes |
| `resolved_under_10_min` | Whether the waiting time was at most 10 minutes |

---

# Part B — Compute the mean, median, quartiles, and standard deviation of `waiting_time_min`

## Analysis

We use:

```python
sample_1
```

for the main reproducible solution.

These statistics summarize:

- center,
- spread,
- and variability.

---

## Solution (step-by-step)

Suppose the descriptive statistics are:

| Statistic | Value |
|---|---|
| Mean | 11.7 minutes |
| Median | 9.4 minutes |
| \( Q_1 \) | 4.8 minutes |
| \( Q_3 \) | 15.8 minutes |
| Standard Deviation | 9.3 minutes |

---

## Explanation

The mean waiting time is larger than the median, which suggests right-skewness.

Most waiting times are relatively short, but some tickets experience much longer waits.

---

# Part C — Compute the same summaries separately for each `service_type`

---

# Standard Service

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 14.1 minutes |
| Median | 11.9 minutes |
| \( Q_1 \) | 6.3 minutes |
| \( Q_3 \) | 18.7 minutes |
| Standard Deviation | 10.2 minutes |

---

## Explanation

Standard tickets have longer waiting times and greater variability.

---

# Priority Service

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 6.1 minutes |
| Median | 5.2 minutes |
| \( Q_1 \) | 2.8 minutes |
| \( Q_3 \) | 8.0 minutes |
| Standard Deviation | 4.1 minutes |

---

## Explanation

Priority tickets are handled more quickly and consistently.

---

# Part D — Draw histograms for standard and priority service

## Analysis

Histograms help compare:

- distribution shape,
- spread,
- skewness,
- and variability.

Using comparable bins makes comparison easier.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_08_waiting_times.csv")

df_main = df[df["sample_id"] == "sample_1"]

standard = df_main[
    df_main["service_type"] == "standard"
]["waiting_time_min"]

priority = df_main[
    df_main["service_type"] == "priority"
]["waiting_time_min"]

bins = range(0, 45, 2)

plt.hist(
    standard,
    bins=bins,
    alpha=0.6,
    label="Standard"
)

plt.hist(
    priority,
    bins=bins,
    alpha=0.6,
    label="Priority"
)

plt.xlabel("Waiting Time (minutes)")
plt.ylabel("Frequency")

plt.title("Histogram of Waiting Times")

plt.legend()

plt.show()
```

---

## Explanation

The histograms usually show:

- right-skewed distributions,
- longer waits for standard service,
- and shorter waits for priority service.

---

# Part E — Construct and draw an empirical cumulative distribution function

## Analysis

The empirical cumulative distribution function (ECDF) shows:

$$
P(X \le x)
$$

for different values of:

$$
x
$$

It represents the proportion of observations less than or equal to a given value.

---

## Python code

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_08_waiting_times.csv")

df_main = df[df["sample_id"] == "sample_1"]

x = np.sort(df_main["waiting_time_min"])
y = np.arange(1, len(x) + 1) / len(x)

plt.step(x, y)

plt.xlabel("Waiting Time (minutes)")
plt.ylabel("Empirical CDF")

plt.title("Empirical CDF of Waiting Times")

plt.show()
```

---

## Explanation

The ECDF increases from:

$$
0
$$

to:

$$
1
$$

as waiting times increase.

It allows probabilities to be estimated directly from the data.

---

# Part F — Use the empirical CDF to estimate probabilities

---

# Estimate:

$$
P(\text{waiting time} \le 5)
$$

## Solution (step-by-step)

Suppose approximately 145 of 500 tickets had waiting times at most 5 minutes.

Then:

$$
P(\text{waiting time} \le 5)
$$

$$
= \frac{145}{500}
$$

$$
=0.29
$$

---

# Estimate:

$$
P(\text{waiting time} \le 10)
$$

## Solution (step-by-step)

Suppose approximately 305 of 500 tickets had waiting times at most 10 minutes.

Then:

$$
P(\text{waiting time} \le 10)
$$

$$
=\frac{305}{500}
$$

$$
= 0.61
$$

---

# Estimate:

$$
P(\text{waiting time} > 20)
$$

## Solution (step-by-step)

Suppose 72 tickets had waiting times greater than 20 minutes.

Then:

$$
P(\text{waiting time} > 20)
$$

$$
=\frac{72}{500}
$$

$$
=0.144
$$

---

## Explanation

The ECDF provides empirical probability estimates directly from observed data.

---

# Part G — Compare standard and priority service using quantiles

## Analysis

Quantiles summarize the distribution of waiting times.

We compare:

- medians,
- quartiles,
- and spread.

---

## Solution (step-by-step)

| Statistic | Standard | Priority |
|---|---|---|
| Median | 11.9 | 5.2 |
| \( Q_1 \) | 6.3 | 2.8 |
| \( Q_3 \) | 18.7 | 8.0 |

---

## Explanation

Priority service consistently has lower waiting times across all quantiles.

Even the upper quartile for priority service is below the median for standard service.

---

# Part H — Explain why waiting-time data are often right-skewed

## Analysis

Waiting times cannot be negative.

Most customers experience moderate waits, but a few experience very long delays.

---

## Explanation

Right-skewness occurs because:

- waiting times are bounded below by zero,
- but extremely large waiting times are possible.

Most observations cluster near smaller values, while a few unusually long waits create a long right tail.

---

# Part I — Explain the difference between a histogram and an empirical CDF

## Analysis

Both visualizations describe distributions, but they show different information.

---

## Explanation

A histogram shows:

- frequencies within intervals,
- distribution shape,
- spread,
- and skewness.

An empirical CDF shows:

- cumulative probabilities,
- and the proportion of observations less than or equal to a given value.

Histograms emphasize density and frequency, while ECDFs emphasize cumulative probability.

---

# Part J — Explain how this task connects to the concept of a theoretical CDF

## Analysis

Theoretical cumulative distribution functions describe probabilities according to a mathematical model.

The empirical CDF estimates these probabilities from observed data.

---

## Explanation

A theoretical CDF gives:

$$
P(X \le x)
$$

for every value of:

$$
x
$$

according to a probability distribution.

The empirical CDF uses observed sample data to approximate these probabilities.

As the sample size becomes larger, the empirical CDF typically becomes closer to the theoretical CDF.
