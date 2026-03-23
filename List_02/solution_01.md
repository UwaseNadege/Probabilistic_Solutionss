# Task List 03 — Algebra of Events and Conditional Probability

> **Note:** This task list is still being developed. Exercises are placeholders for future work.

---

## **Introduction**

Probability theory studies not only **numerical probabilities**, but also the **structure of events** and their relations.  

Key concepts to understand before computing probabilities:

- What an **event** is  
- How events can be **combined**  
- How to describe events using **set operations**  
- How probabilities behave under **union, intersection, complement**  
- How additional information affects **conditional probability**

This list focuses on two closely connected topics:

1. **Algebra of Events**  
2. **Conditional Probability**

Main goal: fluently move between:

- Verbal descriptions of events  
- Set-theoretic notation  
- Probability formulas  
- Concrete probabilistic models  

---

## **Theoretical Background**

### **Random Experiment, Sample Space, and Events**

- A **random experiment**: a process whose outcome cannot be predicted with certainty.  
- **Sample space**: $\Omega$, set of all possible **elementary outcomes**.  
- **Elementary event**: a one-element subset of $\Omega$.  
- **Event**: any subset $A \subseteq \Omega$.

---

### **Event as a Set**

Events are treated as **sets**. Therefore, operations on events = operations on sets:

- **Union:** $A \cup B$ = at least one occurs  
- **Intersection:** $A \cap B$ = both occur  
- **Complement:** $A^c$ = $A$ does not occur  
- **Difference:** $A \setminus B$ = $A$ occurs but $B$ does not  

---

### **Special Types of Events**

- **Mutually Exclusive / Disjoint:** $A \cap B = \emptyset$  
- **Certain event:** $\Omega$, probability $P(\Omega) = 1$  
- **Impossible event:** $\emptyset$, probability $P(\emptyset) = 0$

---

### **Basic Probability Properties**

- $0 \le P(A) \le 1$  
- $P(A \cup B) = P(A) + P(B)$ for disjoint events  
- **Complement rule:** $P(A^c) = 1 - P(A)$  
- **Inclusion–Exclusion:** $P(A \cup B) = P(A) + P(B) - P(A \cap B)$  

---

### **Conditional Probability**

- $P(A \mid B) = \frac{P(A \cap B)}{P(B)}, \quad P(B) > 0$  
- **Multiplication rule:** $P(A \cap B) = P(B) P(A \mid B) = P(A) P(B \mid A)$  

---

### **Independence of Events**

- $A$ and $B$ independent if $P(A \cap B) = P(A) P(B)$  
- Equivalent: $P(A \mid B) = P(A)$ if $P(B) > 0$  
- Independence ≠ mutual exclusivity  

---

### **Law of Total Probability**

- If $\{B_1, B_2, \dots, B_n\}$ forms a partition of $\Omega$, then:

$$
P(A) = \sum_{i=1}^n P(A \mid B_i) P(B_i)
$$

---

### **Bayes’ Formula**

- For $B_1, \dots, B_n$ partition of $\Omega$, $P(A) > 0$:

$$
P(B_k \mid A) = \frac{P(A \mid B_k) P(B_k)}{\sum_{i=1}^n P(A \mid B_i) P(B_i)}
$$

- Allows **reversing conditional probabilities**.

---

### **How to Read Event Statements Correctly**

- “At least one” → often **complement**  
- “Exactly one” → separate cases  
- “Both” → **intersection**  
- “At least one of” → **union**  
- “Given that” → **conditional probability**

---

## **Task 01 – Basic Event Notation and Set Operations**

For each random experiment:

1. **Define the sample space** $\Omega$  
2. **Define events in words**  
3. **Write corresponding unions, intersections, complements, differences**

### **Experiments & Event Descriptions**

| Experiment | Event Statements |
|------------|----------------|
| One toss of a coin | Result is heads, result is not tails |
| One roll of a fair die | Die shows an even number, die shows a number > 3 |
| Two tosses of a coin | At least one head, both tosses give the same result |
| Drawing one card from a deck | Card is a heart, card is a face card |

---

> **Note:** Actual computations, probabilities, and solutions will be developed once exercises are finalized.
