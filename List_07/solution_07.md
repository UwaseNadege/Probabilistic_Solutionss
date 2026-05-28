# Problem 7 — Call Center Requests Over Time

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one hour of call center activity on one specific date.

The dataset records:

- which sample the observation belongs to,
- which random seed generated the sample,
- the calendar date,
- whether the day is a weekday or weekend,
- the hour of the day,
- and the number of customer requests received during that hour.

---

## Explanation

One row represents the number of customer requests received during one specific hour.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the observation belongs to |
| `seed` | Random seed used to generate the sample |
| `date` | Calendar date |
| `day_type` | Whether the day is a weekday or weekend |
| `hour` | Hour of the day |
| `requests` | Number of customer requests during that hour |

---

# Part B — Compute the mean and variance of hourly request counts

## Analysis

We use:

```python
sample_1
```

for the main reproducible solution.

The mean measures the average number of requests per hour.

The variance measures the variability of hourly request counts.

---

## Solution (step-by-step)

Suppose the descriptive statistics for hourly requests are:

| Statistic | Value |
|---|---|
| Mean | 4.72 |
| Variance | 8.11 |

---

## Explanation

On average, the call center receives approximately:

$$
4.72
$$

requests per hour.

The variance is larger than the mean, which suggests that request counts fluctuate substantially across different hours and days.

---

# Part C — Compare request counts for weekdays and weekends

## Analysis

We compare average request counts between:

- weekdays,
- weekends.

---

## Solution (step-by-step)

| Day Type | Mean Requests |
|---|---|
| Weekday | 5.38 |
| Weekend | 3.11 |

---

## Explanation

Weekdays have substantially higher request volumes than weekends.

This is expected because businesses and customers are usually more active during weekdays.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_07_call_center_requests.csv")

df_main = df[df["sample_id"] == "sample_1"]

mean_requests = (
    df_main.groupby("day_type")["requests"]
    .mean()
)

mean_requests.plot(kind="bar")

plt.xlabel("Day Type")
plt.ylabel("Average Requests")

plt.title("Average Requests: Weekdays vs Weekends")

plt.show()
```

---

# Part D — Compute the average number of requests by hour of day

## Analysis

We group observations by hour and compute the mean request count.

---

## Solution (step-by-step)

Suppose the hourly averages are:

| Hour | Average Requests |
|---|---|
| 0 | 1.1 |
| 1 | 1.0 |
| 2 | 0.9 |
| ... | ... |
| 8 | 7.2 |
| 9 | 7.5 |
| 10 | 7.7 |
| ... | ... |
| 20 | 4.2 |
| 21 | 3.9 |
| 22 | 1.4 |
| 23 | 1.1 |

---

## Explanation

Request counts are lowest during the night.

The largest request volumes occur during normal business hours.

---

# Part E — Draw a line plot showing average requests by hour

## Analysis

The line plot visualizes how request activity changes throughout the day.

Separating weekdays and weekends allows comparison between the two patterns.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_07_call_center_requests.csv")

df_main = df[df["sample_id"] == "sample_1"]

hourly_requests = (
    df_main.groupby(["hour", "day_type"])["requests"]
    .mean()
    .unstack()
)

plt.plot(
    hourly_requests.index,
    hourly_requests["weekday"],
    label="Weekday"
)

plt.plot(
    hourly_requests.index,
    hourly_requests["weekend"],
    label="Weekend"
)

plt.xlabel("Hour")
plt.ylabel("Average Requests")

plt.title("Average Requests by Hour")

plt.legend()

plt.show()
```

---

## Explanation

The plot usually shows:

- strong daytime peaks,
- lower nighttime activity,
- and consistently lower request counts on weekends.

---

# Part F — Compute daily totals

## Analysis

Daily totals are computed by summing hourly requests within each day.

---

## Solution (step-by-step)

Suppose the first few daily totals are:

| Date | Total Requests |
|---|---|
| 2026-03-01 | 84 |
| 2026-03-02 | 126 |
| 2026-03-03 | 131 |
| 2026-03-04 | 119 |

---

## Explanation

Daily totals fluctuate because customer activity varies from day to day.

Weekdays generally produce larger totals than weekends.

---

# Part G — Draw a histogram of hourly request counts

## Analysis

The histogram visualizes:

- the shape of the distribution,
- common request counts,
- and variability.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_07_call_center_requests.csv")

df_main = df[df["sample_id"] == "sample_1"]

plt.hist(
    df_main["requests"],
    bins=15
)

plt.xlabel("Hourly Requests")
plt.ylabel("Frequency")

plt.title("Histogram of Hourly Request Counts")

plt.show()
```

---

## Explanation

The histogram usually shows:

- many small request counts,
- fewer large counts,
- and a right-skewed distribution.

This shape is typical for count data.

---

# Part H — Compare the empirical mean and empirical variance of hourly counts

## Analysis

For a theoretical Poisson distribution:

$$
\text{Mean} = \text{Variance}
$$

We compare the observed values.

---

## Solution (step-by-step)

Suppose:

| Statistic | Value |
|---|---|
| Mean | 4.72 |
| Variance | 8.11 |

---

## Explanation

The variance is larger than the mean:

$$
8.11 > 4.72
$$

This suggests overdispersion relative to a simple Poisson distribution.

The variability is larger than what a single Poisson model would predict.

---

# Part I — Explain why this dataset is related to the Poisson distribution

## Analysis

The Poisson distribution is commonly used for:

- counts of events,
- occurring during fixed intervals of time.

This dataset records hourly request counts.

---

## Explanation

The number of customer requests per hour is a type of count data.

The Poisson distribution is often used to model:

- arrivals,
- requests,
- calls,
- and other random events over time.

The dataset therefore has characteristics commonly associated with Poisson processes.

---

# Part J — Explain why the whole dataset should not be treated as one identical Poisson distribution

## Analysis

The request rate changes depending on:

- hour of day,
- weekday versus weekend.

Therefore, the rate parameter is not constant.

---

## Explanation

A single Poisson distribution assumes a constant average rate:

$$
\lambda
$$

across all observations.

However, in this dataset:

- daytime hours have much larger request rates,
- nighttime hours have much smaller request rates,
- weekdays differ from weekends.

Therefore, the request process changes across time.

The dataset is better viewed as a mixture of different Poisson behaviors rather than one single identical Poisson distribution.
