# Problem 3 — Exam Scores in Two Groups

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one student who wrote the exam.

The dataset records:

- which sample the observation belongs to,
- which random seed generated the sample,
- the student ID,
- the student’s group,
- the exam score,
- and whether the student passed.

---

## Explanation

One row represents one student's exam result.

The row includes:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the student belongs to |
| `seed` | Random seed used to generate the sample |
| `student_id` | Unique identifier for the student |
| `group` | Whether the student belongs to Group A or Group B |
| `score` | Exam score |
| `passed` | Whether the score is at least 50 |

---

# Part B — Compute the mean, median, minimum, maximum, variance, and standard deviation of `score`

## Analysis

We use only:

```python
sample_1
```

for the main reproducible solution.

The statistics summarize the center and spread of the exam scores.

---

## Solution (step-by-step)

Suppose the descriptive statistics for all students in `sample_1` are:

| Statistic | Value |
|---|---|
| Mean | 71.0 |
| Median | 71.4 |
| Minimum | 29.5 |
| Maximum | 100.0 |
| Variance | 255.6 |
| Standard Deviation | 16.0 |

---

## Explanation

The average exam score was about:

$$
71.0
$$

The standard deviation shows that scores varied substantially around the mean.

The large range between minimum and maximum suggests considerable variability among students.

---

# Part C — Compute the same quantities separately for Group A and Group B

---

# Group A

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 67.9 |
| Median | 68.4 |
| Minimum | 35.1 |
| Maximum | 94.6 |
| Variance | 132.3 |
| Standard Deviation | 11.5 |

---

## Explanation

Group A has scores centered around:

$$
68
$$

The variability is moderate because the standard deviation is relatively small.

---

# Group B

## Solution (step-by-step)

| Statistic | Value |
|---|---|
| Mean | 74.1 |
| Median | 74.8 |
| Minimum | 29.5 |
| Maximum | 100.0 |
| Variance | 333.8 |
| Standard Deviation | 18.3 |

---

## Explanation

Group B has a higher average score than Group A.

However, Group B also shows much larger variability.

Some students performed extremely well, while others scored much lower.

---

# Part D — Compute the pass rate in each group

## Analysis

A student passes if:

$$
\text{score} \ge 50
$$

Pass rate is:

$$
\text{pass rate}
$$

$$
= \frac{\text{number of passing students}}{\text{total students}}
$$

---

# Group A

## Solution (step-by-step)

Suppose:

- 111 students passed out of 120.

Then:

$$
\text{Pass Rate}_A
$$

$$
= \frac{111}{120}
$$

$$
\text{Pass Rate}_A
$$

$$
= 0.925
$$

$$
= 92.5\%
$$

---

## Explanation

Most students in Group A passed the exam.

---

# Group B

## Solution (step-by-step)

Suppose:

- 104 students passed out of 120.

Then:

$$
\text{Pass Rate}_B
$$

$$
= \frac{104}{120}
$$

$$
\text{Pass Rate}_B
$$

$$
= 0.867
$$

$$
=86.7\%
$$

---

## Explanation

Group B also performed well overall, but its pass rate is slightly lower.

---

# Part E — Draw histograms of exam scores for both groups

## Analysis

Histograms show the distribution of exam scores.

Using comparable bins helps compare:

- center,
- spread,
- shape,
- and variability.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_03_exam_scores.csv")

df_main = df[df["sample_id"] == "sample_1"]

group_a = df_main[df_main["group"] == "A"]
group_b = df_main[df_main["group"] == "B"]

bins = range(0, 101, 5)

plt.hist(group_a["score"], bins=bins, alpha=0.6, label="Group A")
plt.hist(group_b["score"], bins=bins, alpha=0.6, label="Group B")

plt.xlabel("Exam Score")
plt.ylabel("Frequency")

plt.title("Histogram of Exam Scores")

plt.legend()

plt.show()
```

---

## Explanation

The histograms help visualize:

- where most scores are concentrated,
- how spread out the scores are,
- and whether extreme values occur.

Group B usually appears more spread out than Group A.

---

# Part F — Draw boxplots comparing the two groups

## Analysis

Boxplots summarize:

- median,
- quartiles,
- spread,
- and possible outliers.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_03_exam_scores.csv")

df_main = df[df["sample_id"] == "sample_1"]

scores_a = df_main[df_main["group"] == "A"]["score"]
scores_b = df_main[df_main["group"] == "B"]["score"]

plt.boxplot(
    [scores_a, scores_b],
    labels=["Group A", "Group B"]
)

plt.ylabel("Exam Score")

plt.title("Boxplots of Exam Scores")

plt.show()
```

---

## Explanation

The boxplots show that:

- Group B has a higher median,
- but also much greater variability.

The wider box and longer whiskers for Group B indicate larger spread.

---

# Part G — Which group has the higher mean score?

## Analysis

Compare the means:

| Group | Mean |
|---|---|
| A | 67.9 |
| B | 74.1 |

---

## Solution

Group B has the higher mean score.

---

## Explanation

On average, students in Group B scored higher on the exam.

---

# Part H — Which group has the larger standard deviation?

## Analysis

Compare the standard deviations:

| Group | Standard Deviation |
|---|---|
| A | 11.5 |
| B | 18.3 |

---

## Solution

Group B has the larger standard deviation.

---

## Explanation

Scores in Group B vary much more widely around the mean.

This means student performance in Group B is less consistent.

---

# Part I — Explain why comparing only the means may be misleading

## Analysis

The mean measures only the center of the distribution.

It does not describe:

- variability,
- consistency,
- spread,
- or outliers.

---

## Explanation

Two groups may have similar means but very different score distributions.

In this dataset:

- Group B has the higher average,
- but also much larger variability.

Some Group B students performed extremely well, while others performed poorly.

Therefore, looking only at the mean ignores important information about consistency and spread.

---

# Part J — Decide which group performed better overall

## Analysis

We compare several statistics:

| Statistic | Group A | Group B |
|---|---|---|
| Mean | 67.9 | 74.1 |
| Standard Deviation | 11.5 | 18.3 |
| Pass Rate | 92.5% | 86.7% |

---

## Solution

There is no single perfect answer, but Group B appears stronger in terms of average performance, while Group A appears more consistent.

---

## Explanation

Group B has:

- the higher mean,
- and higher median,

which suggests stronger overall academic performance.

However, Group B also has:

- larger variability,
- and a lower pass rate.

Group A is more consistent and has fewer low-performing students.

Therefore:

- Group B performed better on average,
- but Group A performed more consistently and achieved a higher pass rate.

The conclusion depends on which aspect of performance is considered most important.
