# 📘 Problem 4 — Building Complex Statements from Simple Ones

---

## ❓ Question

Consider an experiment consisting of two die rolls.

Each outcome is an ordered pair:

$$
(i, j)
$$

where:

- \( i \) = result of the first die  
- \( j \) = result of the second die  

Representation:

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .
```

---

## 🔹 Part A — Basic Statements

We define the following events:

- **A**: sum of the two results is 7  
- **B**: first die is greater than the second  
- **C**: at least one die shows 6  

---

### 🔸 Event A: \( i + j = 7 \)

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X .
3     . . . X . .
4     . . X . . .
5     . X . . . .
6     X . . . . .
```

---

### 🔸 Event B: \( i > j \)

```
      1 2 3 4 5 6
1     . . . . . .
2     X . . . . .
3     X X . . . .
4     X X X . . .
5     X X X X . .
6     X X X X X .
```

---

### 🔸 Event C: At least one die is 6

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     X X X X X X
```

---

# 🔹 Part B — Compound Statements

---

## 1. \( A \cup C \)

### “The sum is 7 OR at least one die shows 6”

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X X
3     . . . X . X
4     . . X . . X
5     . X . . . X
6     X . . . . X
```

---

## 2. \( A \cap C \)

### “The sum is 7 AND at least one die shows 6”

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     X . . . . .
```

---

## 3. \( B \cap C \)

### “First die is greater AND at least one die shows 6”

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     X X X X X .
```

---

## 4. \( A \cap B^c \)

### “Sum is 7 AND first die is NOT greater than second”

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .
```

---

## 5. \( A \cap C^c \)

### “Sum is 7 AND no die shows 6”

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . X .
3     . . . X . .
4     . . X . . .
5     . X . . . .
6     . . . . . .
```

---

## 6. \( C \cap A^c \)

### “At least one die shows 6 AND sum is NOT 7”

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     X X X X X .
```

---

## 7. \( A^c \cap B \)

### “Sum is NOT 7 AND first die is greater”

```
      1 2 3 4 5 6
1     X . . . . .
2     X X . . . .
3     X X X . . .
4     X X . X . .
5     X X X X X .
6     X X X X X X
```

---

## 8. \( B^c \cap C \)

### “First die is NOT greater AND at least one die shows 6”

```
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     . . . . . X
```

---

## 9. \( (A \cup C)^c \)

### “NOT (sum is 7 OR at least one die shows 6)”

```
      1 2 3 4 5 6
1     X X X X X .
2     X X X X . .
3     X X X . X .
4     X X . X X .
5     X . X X X .
6     . X X X X .
```

---

## 10. \( (A \cap C)^c \)

### “NOT (sum is 7 AND at least one die shows 6)”

```
      1 2 3 4 5 6
1     X X X X X .
2     X X X X X X
3     X X X X X X
4     X X X X X X
5     X X X X X X
6     . X X X X X
```

---

# 🔍 Final Conceptual Insight

This problem shows the **core of formal probability reasoning**:

- Each event = a **set**
- Each statement = **set operation**

### Logical ↔ Set Mapping

| Logic | Set |
|------|-----|
| AND | \( \cap \) |
| OR | \( \cup \) |
| NOT | \( ^c \) |

---

👉 Complex statements are just **combinations of simple events**  
👉 Visualization helps reveal the **structure of these combinations**
