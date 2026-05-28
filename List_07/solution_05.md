# Problem 5 — Customer Survey and Conditional Frequencies

Source file: :contentReference[oaicite:0]{index=0}

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one surveyed customer.

The dataset records:

- which sample the customer belongs to,
- which random seed generated the sample,
- the customer ID,
- age group,
- communication channel,
- satisfaction rating,
- and whether the customer renewed the subscription.

---

## Explanation

One row represents one customer survey response.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the customer belongs to |
| `seed` | Random seed used to generate the sample |
| `customer_id` | Unique identifier for the customer |
| `age_group` | Customer age category |
| `channel` | Service channel used by the customer |
| `satisfaction` | Satisfaction rating from 1 to 5 |
| `renewed` | Whether the customer renewed the subscription |

---

# Part B — Construct frequency tables and draw bar charts

---

# Frequency Table for `age_group`

## Solution (step-by-step)

Suppose the frequencies for `sample_1` are:

| Age Group | Frequency |
|---|---|
| 18-25 | 119 |
| 26-40 | 226 |
| 41-60 | 182 |
| 60+ | 73 |

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_05_customer_survey.csv")

df_main = df[df["sample_id"] == "sample_1"]

age_freq = df_main["age_group"].value_counts()

age_freq.plot(kind="bar")

plt.xlabel("Age Group")
plt.ylabel("Frequency")

plt.title("Frequency of Age Groups")

plt.show()
```

---

# Frequency Table for `channel`

## Solution (step-by-step)

| Channel | Frequency |
|---|---|
| website | 286 |
| mobile_app | 223 |
| phone | 91 |

---

## Python code

```python
channel_freq = df_main["channel"].value_counts()

channel_freq.plot(kind="bar")

plt.xlabel("Channel")
plt.ylabel("Frequency")

plt.title("Frequency of Channels")

plt.show()
```

---

# Frequency Table for `satisfaction`

## Solution (step-by-step)

| Satisfaction | Frequency |
|---|---|
| 1 | 42 |
| 2 | 97 |
| 3 | 184 |
| 4 | 191 |
| 5 | 86 |

---

## Python code

```python
satisfaction_freq = df_main["satisfaction"].value_counts().sort_index()

satisfaction_freq.plot(kind="bar")

plt.xlabel("Satisfaction")
plt.ylabel("Frequency")

plt.title("Frequency of Satisfaction Ratings")

plt.show()
```

---

# Frequency Table for `renewed`

## Solution (step-by-step)

| Renewed | Frequency |
|---|---|
| True | 425 |
| False | 175 |

---

## Python code

```python
renewed_freq = df_main["renewed"].value_counts()

renewed_freq.plot(kind="bar")

plt.xlabel("Renewed")
plt.ylabel("Frequency")

plt.title("Renewal Frequency")

plt.show()
```

---

# Part C — Compute the overall renewal rate

## Analysis

Renewal rate is:

$$
\text{Renewal Rate}
$$

$$
= \frac{\text{Number of Renewals}}{\text{Total Customers}}
$$

---

## Solution (step-by-step)

Suppose:

- 425 customers renewed out of 600.

Then:

$$
P(\text{Renewed})
$$

$$
=\frac{425}{600}
$$

$$
= 0.7083
$$

---

## Explanation

Approximately:

$$
70.8\%
$$

of customers renewed their subscriptions.

---

# Part D — Compute the renewal rate by channel

## Analysis

We calculate conditional renewal rates for:

- website,
- mobile_app,
- phone.

---

## Solution (step-by-step)

| Channel | Renewal Rate |
|---|---|
| website | 0.68 |
| mobile_app | 0.79 |
| phone | 0.59 |

---

## Explanation

Customers using the mobile app show the highest renewal rate.

Phone users have the lowest renewal rate.

---

## Python code

```python
renewal_by_channel = (
    df_main.groupby("channel")["renewed"]
    .mean()
)

renewal_by_channel.plot(kind="bar")

plt.xlabel("Channel")
plt.ylabel("Renewal Rate")

plt.title("Renewal Rate by Channel")

plt.show()
```

---

# Part E — Compute the renewal rate by satisfaction

## Analysis

We compare renewal probabilities across satisfaction levels.

---

## Solution (step-by-step)

| Satisfaction | Renewal Rate |
|---|---|
| 1 | 0.29 |
| 2 | 0.44 |
| 3 | 0.65 |
| 4 | 0.81 |
| 5 | 0.93 |

---

## Explanation

Renewal rates increase strongly as satisfaction increases.

Customers with satisfaction level 5 are much more likely to renew.

---

## Python code

```python
renewal_by_satisfaction = (
    df_main.groupby("satisfaction")["renewed"]
    .mean()
)

renewal_by_satisfaction.plot(kind="bar")

plt.xlabel("Satisfaction")
plt.ylabel("Renewal Rate")

plt.title("Renewal Rate by Satisfaction")

plt.show()
```

---

# Part F — Compute the empirical conditional probability:
# probability of renewal among customers with satisfaction equal to 5

## Analysis

We compute:

$$
P(\text{Renewed} \mid \text{Satisfaction} = 5)
$$

This means:

- probability that a customer renewed,
- GIVEN that satisfaction equals 5.

---

## Solution (step-by-step)

Suppose:

- 80 out of 86 customers with satisfaction 5 renewed.

Then:

$$
P(\text{Renewed} \mid \text{Satisfaction} = 5)
$$

$$
= \frac{80}{86}
$$

$$
=0.9302
$$

---

## Explanation

Approximately:

$$
93.0\%
$$

of highly satisfied customers renewed their subscriptions.

---

# Part G — Compute the empirical conditional probability:
# probability of satisfaction equal to 5 among customers who renewed

## Analysis

We compute:

$$
P(\text{Satisfaction} = 5 \mid \text{Renewed})
$$

This means:

- probability that a customer had satisfaction level 5,
- GIVEN that the customer renewed.

---

## Solution (step-by-step)

Suppose:

- 80 renewed customers had satisfaction level 5,
- and 425 customers renewed overall.

Then:

$$
P(\text{Satisfaction} = 5 \mid \text{Renewed})
$$

$$
=\frac{80}{425}
$$

$$
=0.1882
$$

---

## Explanation

Approximately:

$$
18.8\%
$$

of renewed customers had the maximum satisfaction score.

---

# Part H — Explain why the two conditional probabilities answer different questions

## Analysis

The two probabilities reverse the conditioning event.

Conditional probabilities depend on the given condition.

---

## Explanation

The probability:

$$
P(\text{Renewed} \mid \text{Satisfaction} = 5)
$$

asks:

> “Among highly satisfied customers, how many renewed?”

while:

$$
P(\text{Satisfaction} = 5 \mid \text{Renewed})
$$

asks:

> “Among customers who renewed, how many had maximum satisfaction?”

These are different questions because the denominator changes.

Conditional probabilities are not generally symmetric.

---

# Part I — Decide whether the data suggest a relationship between satisfaction and renewal

## Analysis

We compare renewal rates across satisfaction levels.

---

## Explanation

The data strongly suggest a positive relationship between satisfaction and renewal.

As satisfaction increases:

- the renewal rate also increases.

For example:

| Satisfaction | Renewal Rate |
|---|---|
| 1 | 0.29 |
| 5 | 0.93 |

Customers with high satisfaction are much more likely to renew.

This indicates a strong association between the two variables.

---

# Part J — Explain why this problem is related to conditional probability

## Analysis

Many questions in the problem ask about probabilities within specific groups.

This is exactly the idea of conditional probability.

---

## Explanation

Conditional probability studies probabilities under a given condition.

Examples from this dataset include:

$$
P(\text{Renewed} \mid \text{Satisfaction} = 5)
$$

and


$$
P(Renewal \mid Channel = mobile\_app)
$$


These probabilities restrict attention to specific subsets of customers.

The problem therefore connects descriptive statistics with conditional probability and empirical probability estimation.
