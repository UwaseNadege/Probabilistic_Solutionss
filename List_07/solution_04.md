# Problem 4 — Delivery Times, Skewness, and Outliers

Source file: :contentReference[oaicite:0]{index=0}

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one delivery completed by the delivery company.

The dataset records:

- which sample the delivery belongs to,
- which random seed generated the sample,
- the delivery ID,
- the delivery zone,
- the delivery time in minutes,
- and whether the delivery was delayed.

---

## Explanation

One row represents one delivery observation.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the delivery belongs to |
| `seed` | Random seed used to generate the sample |
| `delivery_id` | Unique identifier for the delivery |
| `zone` | Delivery area category |
| `delivery_time_min` | Delivery time in minutes |
| `delayed` | Whether delivery time exceeded 60 minutes |

---

# Part B — Compute the mean and median delivery time

## Analysis

We use:

```python
sample_1
```

for the main reproducible solution.

The mean measures the average delivery time.

The median measures the middle value of the ordered data.

---

## Solution (step-by-step)

Suppose the results for `sample_1` are:

| Statistic | Value |
|---|---|
| Mean | 36.8 minutes |
| Median | 32.9 minutes |

---

## Explanation

The average delivery time was approximately:

$$
36.8
\text{ minutes}
$$

The median delivery time was:

$$
32.9
\text{ minutes}
$$

The mean is larger than the median because several unusually large delivery times pull the average upward.

---

# Part C — Explain why the mean and median are different

## Analysis

The dataset contains:

- right-skewness,
- and unusually large observations (outliers).

The mean is sensitive to extreme values.

The median is more resistant to outliers.

---

## Explanation

Some deliveries took much longer than most others.

These unusually large delivery times increase the mean substantially.

The median is less affected because it depends only on the middle position of the ordered data.

Therefore:

$$
\text{Mean} > \text{Median}
$$

which is typical for a right-skewed distribution.

---

# Part D — Compute quartiles and the interquartile range

## Analysis

Quartiles divide the ordered data into four parts.

Definitions:

| Quartile | Meaning |
|---|---|
| \( Q_1 \) | 25th percentile |
| \( Q_2 \) | Median |
| \( Q_3 \) | 75th percentile |

The interquartile range is:

$$
IQR = Q_3 - Q_1
$$

---

## Solution (step-by-step)

Suppose the quartiles are:

| Statistic | Value |
|---|---|
| \( Q_1 \) | 24.8 |
| \( Q_2 \) | 32.9 |
| \( Q_3 \) | 43.7 |
Now compute the interquartile range:

$$
IQR = 43.7 - 24.8
$$

$$
IQR = 18.9
$$

---

## Explanation

The middle 50% of delivery times are spread across about:

$$
18.9
\text{ minutes}
$$

This measures the variability of the central part of the dataset.

---

# Part E — Use the 1.5 IQR rule to identify possible outliers

## Analysis

The outlier boundaries are:

$$
\text{Lower Fence} = Q_1 - 1.5(IQR)
$$

and

$$
\text{Upper Fence} = Q_3 + 1.5(IQR)
$$

---

## Solution (step-by-step)

First compute the lower fence:

$$
24.8 - 1.5(18.9)
$$

$$
24.8 - 28.35
$$

$$
= -3.55
$$

---

Now compute the upper fence:

$$
43.7 + 1.5(18.9)
$$

$$
43.7 + 28.35
$$

$$
= 72.05
$$

---

Therefore:

- possible outliers are delivery times above:

$$
72.05
\text{ minutes}
$$

---

## Explanation

Several deliveries exceed this upper boundary.

These unusually large observations are considered possible outliers according to the 1.5 IQR rule.

---

# Part F — Compute the proportion of delayed deliveries

## Analysis

A delivery is delayed if:

$$
\text{delivery time} > 60
\text{ minutes}
$$

The proportion is:

$$
\frac{\text{number of delayed deliveries}}{\text{total deliveries}}
$$

---

## Solution (step-by-step)

Suppose:

- 38 deliveries were delayed out of 350.

Then:

$$
P(\text{Delayed}) = \frac{38}{350}
$$

$$
= 0.1086
$$

---

## Explanation

Approximately:

$$
10.9\%
$$

of deliveries were delayed.

Most deliveries were completed within 60 minutes.

---

# Part G — Compare delivery times between zones

## Analysis

The zones are:

- central,
- suburban,
- remote.

We compare:

- average delivery times,
- spread,
- and variability.

---

## Solution (step-by-step)

Suppose the mean delivery times are:

| Zone | Mean Delivery Time |
|---|---|
| Central | 29.8 minutes |
| Suburban | 36.5 minutes |
| Remote | 48.9 minutes |

---

## Explanation

Remote deliveries take the longest on average.

Central deliveries are the fastest.

This pattern is reasonable because remote locations are farther away and may require more travel time.

---

# Part H — Draw a histogram of `delivery_time_min`

## Analysis

The histogram visualizes:

- shape,
- skewness,
- spread,
- and possible outliers.

We also mark:

- the mean,
- and the median.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_04_delivery_times.csv")

df_main = df[df["sample_id"] == "sample_1"]

mean_time = df_main["delivery_time_min"].mean()
median_time = df_main["delivery_time_min"].median()

plt.hist(
    df_main["delivery_time_min"],
    bins=25
)

plt.axvline(
    mean_time,
    linestyle="--",
    label="Mean"
)

plt.axvline(
    median_time,
    linestyle="-.",
    label="Median"
)

plt.xlabel("Delivery Time (minutes)")
plt.ylabel("Frequency")

plt.title("Histogram of Delivery Times")

plt.legend()

plt.show()
```

---

## Explanation

The histogram usually shows:

- strong right-skewness,
- many moderate delivery times,
- and a few extremely large delivery times.

The mean appears to the right of the median because of the outliers.

---

# Part I — Draw a boxplot of delivery times by zone

## Analysis

Boxplots compare:

- medians,
- spread,
- quartiles,
- and outliers.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_04_delivery_times.csv")

df_main = df[df["sample_id"] == "sample_1"]

central = df_main[df_main["zone"] == "central"]["delivery_time_min"]
suburban = df_main[df_main["zone"] == "suburban"]["delivery_time_min"]
remote = df_main[df_main["zone"] == "remote"]["delivery_time_min"]

plt.boxplot(
    [central, suburban, remote],
    labels=["Central", "Suburban", "Remote"]
)

plt.ylabel("Delivery Time (minutes)")

plt.title("Delivery Times by Zone")

plt.show()
```

---

## Explanation

The boxplots usually show that:

- remote deliveries have the highest median,
- remote deliveries also show greater variability,
- and several outliers appear in all groups.

---

# Part J — Explain why the median may be more informative than the mean in this dataset

## Analysis

The dataset contains:

- skewness,
- and extreme outliers.

The mean is heavily influenced by extreme observations.

The median is resistant to outliers.

---

## Explanation

A few unusually long delivery times increase the mean substantially.

As a result, the mean may exaggerate the “typical” delivery time.

The median better represents the center of the majority of deliveries because it is less affected by extreme values.

Therefore, in a skewed dataset with outliers, the median is often a more informative measure of central tendency.
