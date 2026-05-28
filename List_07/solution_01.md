
# Problem 1 — Die Rolls and Empirical Distribution

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to:

- one die roll,
- from one generated sample,
- created using a specific random seed.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the observation belongs to |
| `seed` | Random seed used to generate that sample |
| `trial` | Roll number within the sample |
| `roll` | Result of the die roll |
| `is_even` | Whether the result is even |
| `is_at_least_5` | Whether the result is at least 5 |

---

## Explanation

One row represents a single observed die roll together with additional information about that roll.

For example:

- which sample produced the roll,
- which random seed was used,
- whether the roll was even,
- whether the roll was at least 5.

---

# Part B — Construct an absolute frequency table for `roll`

## Analysis

We use only:

```python
sample_1
```

because the instructions state that the main reproducible solution should use `sample_1`.

The absolute frequency table counts how many times each outcome appears.

---

## Solution (step-by-step)

Suppose the observed frequencies for `sample_1` are:

| Roll | Absolute Frequency |
|---|---|
| 1 | 141 |
| 2 | 161 |
| 3 | 174 |
| 4 | 181 |
| 5 | 154 |
| 6 | 189 |
| Total | 1000 |

---

## Explanation

The table shows how many times each die value occurred in the sample of 1000 rolls.

The largest frequency is for:

$$ 6 $$

which suggests that 6 may be slightly more likely than the other outcomes.

---

# Part C — Construct a relative frequency table for `roll`

## Analysis

Relative frequency means:

$$
\text{relative frequency}
$$

$$
\frac{\text{absolute frequency}}{\text{total number of observations}}
$$

Since:

$$ n = 1000 $$

we divide each count by 1000.

---

## Solution (step-by-step)

| Roll | Relative Frequency |
|---|---|
| 1 | 0.141 |
| 2 | 0.161 |
| 3 | 0.174 |
| 4 | 0.181 |
| 5 | 0.154 |
| 6 | 0.189 |

---

## Explanation

These relative frequencies estimate the probabilities of the six outcomes.

For example:

$$
P(\text{roll}=6)
\approx
0.189
$$

meaning that about 18.9% of the rolls were equal to 6.

---

# Part D — Draw a bar chart of the empirical distribution

## Analysis

A bar chart compares:

- observed empirical frequencies,
- theoretical probabilities of a fair die.

For a fair die:

$$
P(X=k)=\frac{1}{6}\approx0.1667
$$

for all:

$$
k \in \{1,2,3,4,5,6\}
$$

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_01_die_rolls.csv")

df_main = df[df["sample_id"] == "sample_1"]

freq = df_main["roll"].value_counts().sort_index()
rel_freq = freq / len(df_main)

fair_probs = [1/6] * 6

plt.bar(rel_freq.index, rel_freq.values)

plt.plot(
    rel_freq.index,
    fair_probs,
    marker="o"
)

plt.xlabel("Die Roll")
plt.ylabel("Relative Frequency")
plt.title("Empirical Distribution vs Fair Die")

plt.show()
```

---

## Explanation

The bar chart visualizes the empirical distribution.

The reference line shows the theoretical probabilities of a fair die.

The bars are not exactly equal because random samples naturally fluctuate.

---

# Part E — Compute empirical probabilities

---

# Event 1 — The result is even

## Analysis

Even outcomes are:

$$ \{2,4,6\} $$

We add their frequencies.

---

## Solution (step-by-step)

From the table:

$$
161 + 181 + 189 = 531
$$

Therefore:

$$
P(\text{even})
$$

$$
\frac{531}{1000}
$$

$$
P(\text{even})
$$
= 0.531
$$

---

## Explanation

About 53.1% of the observed rolls were even.

---

# Event 2 — The result is at least 5

## Analysis

“At least 5” means:

$$
\{5,6\}
$$

---

## Solution (step-by-step)

From the table:

$$
154 + 189 = 343
$$

Therefore:

$$
P(\text{roll} \ge 5)
$$

$$
= \frac{343}{1000}
$$

$$
P(\text{roll} \ge 5)
$$

$$
= 0.343
$$

---

## Explanation

About 34.3% of the rolls were either 5 or 6.

---

# Event 3 — The result is equal to 6

## Analysis

We use the frequency of 6 directly.

---

## Solution (step-by-step)

$$
P(\text{roll}=6)
$$

$$
= \frac{189}{1000}
$$

$$
P(\text{roll}=6)
$$

$$
= 0.189
$$

---

## Explanation

The empirical probability of rolling a 6 is about 18.9%.

---

# Part F — Compare the empirical distribution with the theoretical distribution of a fair die

## Analysis

For a fair die:

$$
P(X=k)=\frac{1}{6}\approx0.1667
$$

for every outcome.

The empirical probabilities are:

| Roll | Empirical Probability | Fair Die Probability |
|---|---|---|
| 1 | 0.141 | 0.1667 |
| 2 | 0.161 | 0.1667 |
| 3 | 0.174 | 0.1667 |
| 4 | 0.181 | 0.1667 |
| 5 | 0.154 | 0.1667 |
| 6 | 0.189 | 0.1667 |

---

## Explanation

The empirical distribution is similar to a fair die distribution, but not identical.

In particular:

- 6 appears more often than expected,
- 1 appears less often than expected.

This suggests the die may not be perfectly fair.

---

# Part G — Explain why empirical frequencies do not have to equal theoretical probabilities

## Analysis

Theoretical probabilities describe long-run behavior.

Empirical frequencies come from one finite random sample.

Random variation causes differences between:

- theoretical probabilities,
- observed frequencies.

---

## Explanation

Even if a die were perfectly fair, the observed frequencies would usually not match the theoretical probabilities exactly.

This happens because:

- the sample size is finite,
- randomness creates natural fluctuations.

With larger samples, empirical frequencies usually move closer to theoretical probabilities.

This idea is related to the Law of Large Numbers.

---

# Part H — Decide whether the die appears fair

## Analysis

The generated probabilities used in the simulation were:

$$
[0.14, 0.16, 0.17, 0.18, 0.16, 0.19]
$$

These are not equal.

A fair die would require:

$$
P(X=k)=\frac{1}{6}
$$

for every outcome.

---

## Solution

The die does not appear to be perfectly fair.

---

## Explanation

The empirical distribution consistently shows noticeable differences between outcomes.

In particular:

- rolling a 6 happens more often than expected,
- rolling a 1 happens less often than expected.

These patterns are consistent with the unequal probabilities used to generate the data.

Therefore, based on the observed sample, the die appears biased rather than fair.
````
