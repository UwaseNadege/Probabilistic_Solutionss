# Task 4 — Weekly Weather Observation

We consider an experiment in which the **weather is observed once per day**.  
Each day the weather can be classified into **exactly one** of the following states:

- Sunny ($S$)
- Cloudy ($C$)
- Rainy ($R$)

Because we observe the weather on **multiple consecutive days**, the **order matters**.  
Therefore, each outcome must describe the **sequence of weather states over time**.

---

# 1. Sample Space for One Day

For a single day, the weather can be in one of three possible states.

Therefore the sample space is

$$
\Omega_1 = \{S, C, R\}
$$

### Number of elementary outcomes

$$
|\Omega_1| = 3
$$

### Interpretation

An **elementary outcome** represents the **exact weather state on that day**, for example:

- $S$ → Sunny
- $C$ → Cloudy
- $R$ → Rainy

---

# 2. Sample Space for Two Consecutive Days

Now suppose the weather is observed for **two days in a row**.

Each day has **3 possible states**, and because **order matters**, we must record the sequence.

Examples of outcomes include:

- $(S,S)$
- $(S,C)$
- $(S,R)$
- $(C,S)$
- $(R,R)$

Thus the sample space consists of all **ordered pairs of weather states**.

$$
\Omega_2 = \{(w_1,w_2) : w_1,w_2 \in \{S,C,R\}\}
$$

### Number of elementary outcomes

$$
|\Omega_2| = 3 \times 3 = 3^2
$$

$$
|\Omega_2| = 9
$$

---

# 3. Sample Space for Seven Consecutive Days

Now consider observing the weather for **seven consecutive days**.

Each day has **3 possible states**, and we record the **exact sequence of seven observations**.

Each outcome is therefore an **ordered sequence of seven weather states**:

$$
(w_1, w_2, w_3, w_4, w_5, w_6, w_7)
$$

where each element belongs to the set

$$
\{S, C, R\}
$$

Thus the sample space can be written as

$$
\Omega_7 =
\{(w_1,w_2,w_3,w_4,w_5,w_6,w_7) : w_i \in \{S,C,R\}\}
$$

### Number of elementary outcomes

Each of the 7 days has **3 possible states**, so the total number of outcomes is

$$
|\Omega_7| = 3^7
$$

$$
|\Omega_7| = 2187
$$

---

# 4. Number of Elementary Outcomes

We summarize the results:

| Observation Period | Sample Space | Number of Outcomes |
|-------------------|-------------|--------------------|
| 1 day | $\Omega_1 = \{S,C,R\}$ | 3 |
| 2 days | $\Omega_2$ | $3^2 = 9$ |
| 7 days | $\Omega_7$ | $3^7 = 2187$ |

In general, if weather is observed for **$n$ days**, the number of possible outcomes is

$$
|\Omega_n| = 3^n
$$

because each day has **three possible weather states**.

---

# 5. Meaning of an Elementary Outcome (Weekly Observation)

For the **weekly experiment**, an elementary outcome represents the **exact sequence of weather states for all seven days**.

Example outcomes:

- $(S,S,S,S,S,S,S)$ → sunny all week
- $(R,R,C,S,S,C,R)$
- $(C,S,R,C,S,R,S)$

Thus an elementary outcome describes:

- **the weather state on each day**, and  
- **the exact order in which these states occur during the week**.

Each possible sequence corresponds to **one element of the sample space $\Omega_7$**.
```
