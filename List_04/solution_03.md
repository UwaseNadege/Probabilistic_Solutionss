# Problem 3 — Weather (7 Days × 3 States)

---

## Question

Consider a week described day by day in terms of weather.  

Each day can be:

- \( S \) — sunny  
- \( C \) — cloudy  
- \( R \) — rainy  

Representation:

```
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   .   .
C     .   .   .   .   .   .   .
R     .   .   .   .   .   .   .
```

---

### Part A — Marking Events

Mark all outcomes satisfying the statement:

- Monday is sunny  
- the weekend (Saturday and Sunday) is rainy  
- it rains on Wednesday or Friday  
- there is no rainy day during the week  
- Thursday is not sunny  

---

### Part B — Interpretation

Describe the event represented by each case below:

**Case 1**

```
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   X   X
C     .   .   .   .   .   .   .
R     .   .   .   .   .   .   .
```

**Case 2**

```
      Mon Tue Wed Thu Fri Sat Sun
S     X   X   X   X   X   X   X
C     X   X   X   X   X   X   X
R     .   .   .   .   .   .   .
```

---

# 📌 Solution

---

## 1. Sample Space

Each day has 3 possible states:

$$
\Omega = \{S, C, R\}^7
$$

This means:

- a weekly outcome is a sequence of 7 weather states  
- each day is independent  

---

# 🔹 Part A — Marking Events

---

## 1. Monday Is Sunny

Only sequences where:

$$
\text{Mon} = S
$$

---

## 2. Weekend Is Rainy

Saturday and Sunday must be:

$$
\text{Sat} = R,\quad \text{Sun} = R
$$

---

## 3. It Rains on Wednesday or Friday

This means:

$$
\text{Wed} = R \quad \text{OR} \quad \text{Fri} = R
$$

(Union of two events)

---

## 4. No Rainy Day During the Week

For every day:

$$
\text{Day} \in \{S, C\}
$$

So:

- no \( R \) anywhere in the week

---

## 5. Thursday Is Not Sunny

$$
\text{Thu} \in \{C, R\}
$$

---

# 🔹 Part B — Interpretation

---

## Case 1

```
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   X   X
C     .   .   .   .   .   .   .
R     .   .   .   .   .   .   .
```

### Step 1 — Identify allowed states

- Saturday = S  
- Sunday = S  

All other days are not restricted.

### Step 2 — Interpretation

This means:

- **Saturday and Sunday are sunny**

### ✅ Event:

$$
\text{“The weekend is sunny”}
$$

---

## Case 2

```
      Mon Tue Wed Thu Fri Sat Sun
S     X   X   X   X   X   X   X
C     X   X   X   X   X   X   X
R     .   .   .   .   .   .   .
```

### Step 1 — Identify pattern

- All days allow only \( S \) or \( C \)  
- No \( R \) is allowed at all  

### Step 2 — Interpretation

This means:

- **there is no rainy day during the entire week**

### ✅ Event:

$$
\text{“No rainy day during the week”}
$$

---

#  Final Conceptual Understanding

- Each week is an element of \( \Omega = \{S,C,R\}^7 \)
- Each event is a **subset of sequences**

---

### Key Ideas:

- Each column = one day  
- Each row = possible state  
- Marking = **allowed outcomes**

---

### Logical Meaning:

| Statement | Meaning |
|----------|--------|
| AND | intersection |
| OR | union |
| NOT | complement |

---

👉 This representation allows us to **see structure across time**, not just list sequences.
