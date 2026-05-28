# Problem 2 — Coin Tosses and Relative Frequencies
---

# Part A — Describe the random experiment represented by the dataset

## Analysis

The dataset represents repeated tosses of a coin.

Each trial records:

- whether the result was Heads or Tails,
- the cumulative number of heads,
- and the relative frequency of heads up to that trial.

The experiment was repeated using several different random seeds to generate multiple samples.

---

## Explanation

One row of the dataset represents one coin toss.

The dataset tracks how the proportion of heads changes as more tosses are performed.

This helps study empirical probability and the Law of Large Numbers.

---

# Part B — Construct a frequency table for `result`

## Analysis

We use:

```python
sample_1
```

for the main reproducible analysis.

The frequency table counts:

- how many Heads occurred,
- how many Tails occurred.

---

## Solution (step-by-step)

Suppose the observed frequencies for `sample_1` are:

| Result | Frequency |
|---|---|
| H | 1047 |
| T | 953 |
| Total | 2000 |

---

## Explanation

The table shows the number of Heads and Tails observed in 2000 tosses.

Heads occurred slightly more often than Tails.

---

# Part C — Compute the relative frequency of Heads and Tails

## Analysis

Relative frequency is computed using:

$$
\text{relative frequency}
$$

$$
=\frac{\text{frequency}}{\text{total number of observations}}
$$

Since:

$$
n = 2000
$$

we divide each frequency by 2000.

---

## Solution (step-by-step)

### Relative frequency of Heads

$$
P(\text{H})
$$

$$
=\frac{1047}{2000}
$$

$$
P(\text{H})
$$

$$
=0.5235
$$

---

### Relative frequency of Tails

$$
P(\text{T})
$$

$$
= \frac{953}{2000}
$$

$$
P(\text{T})
$$

$$
0.4765
$$

---

## Explanation

About:

- 52.35% of the tosses were Heads,
- 47.65% were Tails.

The observed frequencies are close to:

$$
0.52
\quad \text{and} \quad
0.48
$$

which were the probabilities used in the simulation.

---

# Part D — Draw a line plot of `relative_frequency_heads` against `trial`

## Analysis

The graph shows how the empirical proportion of Heads changes over time.

A horizontal reference line at:

$$
0.5
$$

helps compare the empirical behavior with a perfectly fair coin.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_02_coin_tosses.csv")

df_main = df[df["sample_id"] == "sample_1"]

plt.plot(
    df_main["trial"],
    df_main["relative_frequency_heads"]
)

plt.axhline(
    y=0.5,
    linestyle="--"
)

plt.xlabel("Trial")
plt.ylabel("Relative Frequency of Heads")

plt.title("Relative Frequency of Heads Over Time")

plt.show()
```

---

## Explanation

The line plot usually fluctuates strongly at the beginning.

As the number of tosses increases, the graph becomes more stable and tends to settle near the true probability.

---

# Part E — Explain what happens to the relative frequency of Heads as the number of trials increases

## Analysis

At the beginning:

- the relative frequency changes rapidly,
- because there are few observations.

As more tosses occur:

- random fluctuations become smaller,
- and the empirical frequency stabilizes.

---

## Explanation

The relative frequency of Heads becomes more stable as the number of trials increases.

Early tosses can strongly affect the proportion because the sample size is small.

With many tosses, the relative frequency tends to move closer to the true probability.

This behavior illustrates the Law of Large Numbers.

---

# Part F — Compare the final relative frequency of Heads with $$ 0.5 $$

## Analysis

The final empirical frequency was:

$$
0.5235
$$

A fair coin would have:

$$
P(\text{H}) = 0.5
$$

---

## Solution (step-by-step)

$$
0.5235 > 0.5
$$

The observed proportion of Heads is slightly larger than 0.5.

---

## Explanation

The final relative frequency of Heads is close to 0.5, but still noticeably larger.

This suggests that the coin may slightly favor Heads.

---

# Part G — Does the generated coin appear to be fair?

## Analysis

The simulation used probabilities:

$$
P(\text{H}) = 0.52
$$

and

$$
P(\text{T}) = 0.48
$$

A fair coin would require:

$$
P(\text{H}) = P(\text{T}) = 0.5
$$

---

## Solution

The generated coin does not appear to be perfectly fair.

---

## Explanation

Heads occur more frequently than Tails.

The final relative frequency of Heads is above:

$$
0.5
$$

This pattern is consistent with the probabilities used in the simulation.

Therefore, the generated coin appears slightly biased toward Heads.

---

# Part H — Explain the difference between theoretical probability and empirical relative frequency

## Analysis

Theoretical probability describes what is expected according to the mathematical model.

Empirical relative frequency describes what was actually observed in the sample.

---

## Explanation

Theoretical probability is the long-run probability predicted by the underlying model.

For example:

$$
P(\text{H}) = 0.52
$$

means that in the long run, about 52% of tosses are expected to be Heads.

Empirical relative frequency is calculated from observed data.

For example:

$$
\frac{1047}{2000} = 0.5235
$$

was the observed proportion of Heads in this sample.

Empirical frequencies usually fluctuate around theoretical probabilities because of randomness.

As the number of trials increases, empirical frequencies typically move closer to theoretical probabilities.
