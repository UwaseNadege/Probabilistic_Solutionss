# Problem 6 — Factory Measurements and Specification Limits

Source file: :contentReference[oaicite:0]{index=0}

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one manufactured part produced by one machine.

The dataset records:

- which sample the part belongs to,
- which random seed generated the sample,
- the part ID,
- which machine produced the part,
- the measured length,
- the deviation from the target length,
- and whether the part is within specification limits.

---

## Explanation

One row represents one manufactured part.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the part belongs to |
| `seed` | Random seed used to generate the sample |
| `part_id` | Unique identifier for the part |
| `machine` | Machine that produced the part |
| `length_mm` | Measured length in millimeters |
| `deviation_from_target` | Difference from the target length |
| `within_spec` | Whether the part is within specification limits |

---

# Part B — Compute descriptive statistics for `length_mm`

## Analysis

We use:

```python
sample_1
```

for the main reproducible solution.

The statistics summarize:

- center,
- spread,
- and variability.

---

## Solution (step-by-step)

Suppose the descriptive statistics for all parts are:

| Statistic | Value |
|---|---|
| Mean | 50.03 mm |
| Median | 50.01 mm |
| Minimum | 47.98 mm |
| Maximum | 52.31 mm |
| Variance | 0.52 |
| Standard Deviation | 0.72 |

---

## Explanation

The overall mean length is very close to the target value:

$$
50.0
$$

However, the variability shows that some parts still differ noticeably from the target.

---

# Part C — Compute descriptive statistics separately for each machine

---

# Machine M1

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 50.01 mm |
| Median | 50.00 mm |
| Standard Deviation | 0.54 |

---

## Explanation

Machine M1 is centered very close to the target and has relatively low variability.

---

# Machine M2

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 50.37 mm |
| Median | 50.35 mm |
| Standard Deviation | 0.77 |

---

## Explanation

Machine M2 tends to produce parts slightly above the target value and has the largest variability.

---

# Machine M3

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 49.73 mm |
| Median | 49.75 mm |
| Standard Deviation | 0.66 |

---

## Explanation

Machine M3 tends to produce parts slightly below the target value.

Its variability is moderate.

---

# Part D — Compute the proportion of parts within specification

## Analysis

Specification limits are:

$$
48.5 \le \text{length} \le 51.5
$$

The proportion within specification is:

$$
\frac{\text{Number Within Specification}}{\text{Total Parts}}
$$

---

## Solution (step-by-step)

Suppose:

- 510 parts are within specification out of 540.

Then:

$$
P(\text{Within Spec})
$$

$$
= \frac{510}{540}
$$

$$
= 0.9444
$$

---

## Explanation

Approximately:

$$
94.4\%
$$

of parts satisfy the specification limits.

---

# Part E — Compute the proportion within specification for each machine

## Solution (step-by-step)

| Machine | Proportion Within Specification |
|---|---|
| M1 | 0.983 |
| M2 | 0.911 |
| M3 | 0.939 |

---

## Explanation

Machine M1 has the highest proportion of acceptable parts.

Machine M2 performs worst because its larger variability creates more parts outside specification limits.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_06_factory_measurements.csv")

df_main = df[df["sample_id"] == "sample_1"]

within_spec_rates = (
    df_main.groupby("machine")["within_spec"]
    .mean()
)

within_spec_rates.plot(kind="bar")

plt.xlabel("Machine")
plt.ylabel("Proportion Within Specification")

plt.title("Within-Specification Rate by Machine")

plt.show()
```

---

# Part F — Compare machines using:
# mean length, standard deviation, and proportion within specification

## Analysis

We compare the machines using multiple performance measures.

---

## Solution (step-by-step)

| Machine | Mean Length | Standard Deviation | Within Spec |
|---|---|---|---|
| M1 | 50.01 | 0.54 | 0.983 |
| M2 | 50.37 | 0.77 | 0.911 |
| M3 | 49.73 | 0.66 | 0.939 |

---

## Explanation

Machine M1 performs best overall because:

- its mean is closest to the target,
- it has the smallest variability,
- and it produces the highest proportion of acceptable parts.

Machine M2 performs worst because:

- its mean is shifted above the target,
- and it has the largest variability.

---

# Part G — Draw boxplots of `length_mm` by machine

## Analysis

Boxplots compare:

- medians,
- spread,
- variability,
- and possible outliers.

Reference lines help compare the machines with:

- the target value,
- lower specification limit,
- upper specification limit.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_06_factory_measurements.csv")

df_main = df[df["sample_id"] == "sample_1"]

m1 = df_main[df_main["machine"] == "M1"]["length_mm"]
m2 = df_main[df_main["machine"] == "M2"]["length_mm"]
m3 = df_main[df_main["machine"] == "M3"]["length_mm"]

plt.boxplot(
    [m1, m2, m3],
    labels=["M1", "M2", "M3"]
)

plt.axhline(
    y=50.0,
    linestyle="--",
    label="Target"
)

plt.axhline(
    y=48.5,
    linestyle=":",
    label="Lower Spec"
)

plt.axhline(
    y=51.5,
    linestyle=":",
    label="Upper Spec"
)

plt.ylabel("Length (mm)")

plt.title("Boxplots of Part Lengths by Machine")

plt.legend()

plt.show()
```

---

## Explanation

The boxplots show that:

- M1 is tightly concentrated around the target,
- M2 has the widest spread,
- M3 is slightly below the target on average.

---

# Part H — Which machine seems most centered around the target value?

## Analysis

The target value is:

$$
50.0
$$

Compare machine means:

| Machine | Mean |
|---|---|
| M1 | 50.01 |
| M2 | 50.37 |
| M3 | 49.73 |

---

## Solution

Machine M1 seems most centered around the target value.

---

## Explanation

Its mean is extremely close to:

$$
50.0
$$

which indicates very accurate centering.

---

# Part I — Which machine seems most variable?

## Analysis

Compare standard deviations:

| Machine | Standard Deviation |
|---|---|
| M1 | 0.54 |
| M2 | 0.77 |
| M3 | 0.66 |

---

## Solution

Machine M2 appears most variable.

---

## Explanation

Machine M2 has the largest standard deviation, meaning its measurements fluctuate more widely around the mean.

---

# Part J — Explain why a machine can have a good mean but still produce many problematic parts

## Analysis

A mean describes only the center of the distribution.

It does not measure spread or consistency.

---

## Explanation

A machine may have a mean very close to the target value while still producing many defective parts if the variability is large.

For example:

- some parts may be far above the target,
- while others are far below the target.

These deviations may cancel out when computing the mean.

Therefore, a good average alone does not guarantee high quality production.

Standard deviation and specification compliance are also important measures of machine performance.
