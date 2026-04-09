# Task 2 — Rolling a Die

We analyze an experiment consisting of rolling a **fair six-sided die**.

A standard die has **six possible outcomes**:

- 1
- 2
- 3
- 4
- 5
- 6

Because the **order of outcomes matters**, when the die is rolled multiple times we must record the **exact sequence of results**.

---

# 1. Sample Space for One Roll

The **sample space** is the set of all possible outcomes of the experiment.

For a single die roll the possible outcomes are simply the numbers on the die.

$$
\Omega_1 = \{1,2,3,4,5,6\}
$$

### Number of elementary outcomes

$$
|\Omega_1| = 6
$$

### Interpretation

An **elementary outcome** represents the **exact result of one roll**, for example:

- the die shows **3**
- the die shows **6**

---

# 2. Sample Space for Two Consecutive Rolls

Now consider **two consecutive rolls of the die**.

Since **order matters**, we record the result of the **first roll and the second roll**.

Each roll has **6 possible results**, therefore the total number of outcomes is

$$
6 \times 6 = 36
$$

### Tree Diagram (conceptual)

```

START
│
├── 1
│    ├── 1
│    ├── 2
│    ├── 3
│    ├── 4
│    ├── 5
│    └── 6
│
├── 2
│    ├── 1
│    ├── 2
│    ├── 3
│    ├── 4
│    ├── 5
│    └── 6
│
...
│
└── 6
├── 1
├── 2
├── 3
├── 4
├── 5
└── 6

```

### Sample Space

Each outcome is an **ordered pair**:

$$
\Omega_2 = \{(i,j) : i,j \in \{1,2,3,4,5,6\}\}
$$

Examples of outcomes include:

- $(1,1)$
- $(2,5)$
- $(6,3)$
- $(4,4)$

### Number of elementary outcomes

$$
|\Omega_2| = 36
$$

---

# 3. Sample Space for Three Consecutive Rolls

Now consider **three consecutive rolls of the die**.

Each roll again has **6 possible outcomes**, therefore:

$$
6 \times 6 \times 6 = 6^3
$$

$$
6^3 = 216
$$

### Sample Space

Each outcome is an **ordered triple**:

$$
\Omega_3 = \{(i,j,k) : i,j,k \in \{1,2,3,4,5,6\}\}
$$

Examples of outcomes:

- $(1,2,3)$
- $(6,6,6)$
- $(4,1,5)$
- $(3,3,2)$

### Number of elementary outcomes

$$
|\Omega_3| = 216
$$

---

# 4. Number of Elementary Outcomes

We summarize the number of outcomes:

| Number of Rolls | Sample Space | Number of Outcomes |
|-----------------|-------------|--------------------|
| 1 | $\Omega_1 = \{1,2,3,4,5,6\}$ | 6 |
| 2 | $\Omega_2 = \{(i,j)\}$ where $i,j \in \{1,\dots,6\}$ | 36 |
| 3 | $\Omega_3 = \{(i,j,k)\}$ where $i,j,k \in \{1,\dots,6\}$ | 216 |

In general, for **$n$ rolls of a die**:

$$
|\Omega_n| = 6^n
$$

because each roll has **six possible outcomes**.

---

# 5. Meaning of an Elementary Outcome

An **elementary outcome** represents **one complete sequence of results** in the experiment.

Examples:

- For **one roll**, an outcome is a **single number**, such as $4$.
- For **two rolls**, an outcome is an **ordered pair**, such as $(2,5)$.
- For **three rolls**, an outcome is an **ordered triple**, such as $(1,6,3)$.

Thus, an elementary outcome describes the **exact results of all rolls in the experiment**, including the **order in which they occur**.

---

✅ **Key idea**

When rolling a die multiple times and the **order matters**, the number of possible outcomes grows exponentially:

$$
6^n
$$

where $n$ is the number of rolls.
```
