# Task 1 — Coin Tossing

We analyze an experiment consisting of tossing a **fair coin**.
A fair coin has two possible outcomes:

* **Heads** (denoted (H))
* **Tails** (denoted (T))

Because the **order of outcomes matters**, the result of multiple tosses must record the **exact sequence** of outcomes.

---

# 1. Sample Space for One Coin Toss

The **sample space** of an experiment is the set of **all possible elementary outcomes**.

For a **single coin toss**, there are only two possible results:

* Heads
* Tails

Therefore the sample space is

$$
\Omega_1 = {H, T}
$$

### Number of elementary outcomes

$$
|\Omega_1| = 2
$$

This means the experiment has **two possible elementary outcomes**.

### Interpretation

An **elementary outcome** represents the **exact result of the experiment**.

For one toss, an elementary outcome is simply:

* the coin lands **Heads**, or
* the coin lands **Tails**.

---

# 2. Sample Space for Two Coin Tosses

Now consider **two consecutive coin tosses**.

Since **order matters**, the outcomes must record the result of the **first toss and the second toss**.

Each toss has **2 possible outcomes**, so the total number of outcomes will be

$$
2 \times 2 = 4
$$

### Tree Diagram

```
START
 │
 ├── H
 │     ├── H
 │     └── T
 │
 └── T
       ├── H
       └── T
```

### Sample Space

The possible sequences are:

$$
\Omega_2 =
{(H,H), (H,T), (T,H), (T,T)}
$$

### Number of elementary outcomes

$$
|\Omega_2| = 4
$$

### Interpretation

Each elementary outcome represents the **exact sequence of the two tosses**, for example:

* ((H,T)) → first toss **Heads**, second toss **Tails**
* ((T,H)) → first toss **Tails**, second toss **Heads**

---

# 3. Sample Space for Three Coin Tosses

Now consider **three consecutive coin tosses**.

Again, **order matters**, so we record the outcome of each toss.

Each toss has **2 possibilities**, therefore:

$$
2 \times 2 \times 2 = 2^3 = 8
$$

possible outcomes.

### Tree Diagram

```
START
 │
 ├── H
 │     ├── H
 │     │     ├── H
 │     │     └── T
 │     │
 │     └── T
 │           ├── H
 │           └── T
 │
 └── T
       ├── H
       │     ├── H
       │     └── T
       │
       └── T
             ├── H
             └── T
```

### Sample Space

$$
\Omega_3 =
{
(H,H,H), (H,H,T), (H,T,H), (H,T,T),
(T,H,H), (T,H,T), (T,T,H), (T,T,T)
}
$$

### Number of elementary outcomes

$$
|\Omega_3| = 8
$$

---

# 4. Number of Elementary Outcomes

We summarize the number of outcomes:

| Number of Tosses | Sample Space                                                                     | Number of Outcomes |
| ---------------- | -------------------------------------------------------------------------------- | ------------------ |
| 1                | $$( \Omega_1 = {H,T} )$$                                                           | (2)                |
| 2                | $$( \Omega_2 = {(H,H),(H,T),(T,H),(T,T)} )$$                                       | (4)                |
| 3                | $$( \Omega_3 = {(H,H,H),(H,H,T),(H,T,H),(H,T,T),(T,H,H),(T,H,T),(T,T,H),(T,T,T)} )$$ | (8)                |


In general, for **(n) coin tosses**:

$$
|\Omega_n| = 2^n
$$

because each toss has **two possible outcomes**.

---

# 5. Meaning of an Elementary Outcome

An **elementary outcome** represents **one specific sequence of results** in the experiment.

Examples:

* In **one toss**, an outcome is simply (H) or (T).
* In **two tosses**, an outcome is a **pair of results**, such as ((H,T)).
* In **three tosses**, an outcome is a **triple of results**, such as ((T,H,T)).

Thus, an elementary outcome describes the **complete result of the entire experiment**, including the **order in which outcomes occur**.
