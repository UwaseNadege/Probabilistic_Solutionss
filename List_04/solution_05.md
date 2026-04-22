# Problem 5 — From recorded frequencies to probability

## General setup

Sample space:

$$
\Omega = \{1,2,3,4,5,6\}
$$

Recorded frequencies from 1000 throws:

- n(1)=168  
- n(2)=154  
- n(3)=181  
- n(4)=167  
- n(5)=160  
- n(6)=170  

Observed frequency:

$$
f(A) = \frac{n(A)}{1000}
$$

---

# Part A — From elementary outcomes to events

## Event A = {2,4,6}

### Analysis

$$
n(A)=n(2)+n(4)+n(6)
$$

---

### Solution (step-by-step)

$$
n(A)=154+167+170
$$

$$
n(A)=321+170
$$

$$
n(A)=491
$$

$$
f(A)=\frac{491}{1000}=0.491
$$

### Explanation

The values 154, 167, and 170 come directly from the experimental frequency table for outcomes 2, 4, and 6.

---

## Event B = {1,2,3}

### Analysis

$$
n(B)=n(1)+n(2)+n(3)
$$

---

### Solution (step-by-step)

$$
n(B)=168+154+181
$$

$$
n(B)=322+181
$$

$$
n(B)=503
$$

$$
f(B)=\frac{503}{1000}=0.503
$$

### Explanation

The values are taken directly from the recorded data for outcomes 1, 2, and 3.

---

## Event C = {5,6}

### Analysis

$$
n(C)=n(5)+n(6)
$$

---

### Solution (step-by-step)

$$
n(C)=160+170
$$

$$
n(C)=330
$$

$$
f(C)=\frac{330}{1000}=0.330
$$

### Explanation

The values come directly from the recorded experiment for outcomes 5 and 6.

---

## Event D = {1,3,5}

### Analysis

$$
n(D)=n(1)+n(3)+n(5)
$$

---

### Solution (step-by-step)

$$
n(D)=168+181+160
$$

$$
n(D)=349+160
$$

$$
n(D)=509
$$

$$
f(D)=\frac{509}{1000}=0.509
$$

### Explanation

The values are taken directly from the experimental results for outcomes 1, 3, and 5.

---

## Event E = {1,2,3,4}

### Analysis

$$
n(E)=n(1)+n(2)+n(3)+n(4)
$$

---

### Solution (step-by-step)

$$
n(E)=168+154+181+167
$$

$$
n(E)=322+181
$$

$$
n(E)=503+167
$$

$$
n(E)=670
$$

$$
f(E)=\frac{670}{1000}=0.670
$$

### Explanation

The values are taken directly from the experiment for outcomes 1–4.

---

# Part B — How frequencies combine

## 1. {2,4,6}

### Check

$$
f(2,4,6)=f(2)+f(4)+f(6)
$$

---

### Solution

$$
0.154+0.167+0.170=0.491
$$

### Explanation

The events are disjoint, so their frequencies can be added.

---

## 2. {1,2,3,4}

### Check

$$
f(1,2,3,4)=f(1,2)+f(3,4)
$$

---

### Solution

$$
f(1,2)=\frac{322}{1000}=0.322
$$

$$
f(3,4)=\frac{348}{1000}=0.348
$$

$$
0.322+0.348=0.670
$$

### Explanation

The set is split into two disjoint parts, so addition is valid.

---

## 3. {1,3,5} and {2,4,6}

### Check

$$
f(1,3,5)+f(2,4,6)=1
$$

---

### Solution

$$
f(1,3,5)=\frac{509}{1000}=0.509
$$

$$
f(2,4,6)=\frac{491}{1000}=0.491
$$

$$
0.509+0.491=1
$$

### Explanation

The two sets form a complete partition of the sample space.

---

## 4. {5,6}

### Check

$$
f(5,6)=1 - f(1,2,3,4)
$$

---

### Solution

$$
1 - 0.670 = 0.330
$$

---

### Explanation

{5,6} is the complement of {1,2,3,4}.

---

# Part C — When addition works and fails

## 1. {1,2} ∪ {5,6}

### Check

$$
f(1,2 \cup 5,6)=f(1,2)+f(5,6)
$$

---

### Solution

$$
f(1,2)=\frac{322}{1000}=0.322
$$

$$
f(5,6)=\frac{330}{1000}=0.330
$$

$$
0.322+0.330=0.652
$$

---

### Explanation

The sets are disjoint, so addition works.

---

## 2. M = {1,2,3}, N = {3,4,5}

### Step 1

$$
f(M)=\frac{503}{1000}=0.503
$$

$$
f(N)=\frac{508}{1000}=0.508
$$

---

### Step 2

$$
f(M \cup N)=\frac{830}{1000}=0.830
$$

---

### Step 3

$$
f(M)+f(N)=1.011
$$

---

### Explanation

Outcome 3 belongs to both sets, so it is counted twice.

---

# Part D — Covering the whole sample space (explained)

## 1. All outcomes

### What is happening?

We are adding the frequencies of ALL possible outcomes:

$$
f(1)+f(2)+f(3)+f(4)+f(5)+f(6)
$$

### Step-by-step idea

Each frequency is:

$$
f(i)=\frac{n(i)}{1000}
$$

So:

$$
f(1)+f(2)+f(3)+f(4)+f(5)+f(6)
$$

$$
\frac{n(1)+n(2)+n(3)+n(4)+n(5)+n(6)}{1000}
$$

Now substitute values:

$$
=\frac{168+154+181+167+160+170}{1000}
$$

Add step by step:

$$
168+154=322
$$

$$
322+181=503
$$

$$
503+167=670
$$

$$
670+160=830
$$

$$
830+170=1000
$$

So:

$$
\frac{1000}{1000}=1
$$

### Meaning

All possible outcomes together ALWAYS give total probability 1 because nothing is missing.

---

## 2. Partition idea

We split the sample space into two groups:

- {1,2,3}
- {4,5,6}

### Step-by-step

First group:

$$
f(1,2,3)=\frac{168+154+181}{1000}
$$

$$
= \frac{503}{1000}=0.503
$$

Second group:

$$
f(4,5,6)=\frac{167+160+170}{1000}
$$

$$
= \frac{497}{1000}=0.497
$$

Now add:

$$
0.503+0.497=1
$$

### Meaning

We split ALL outcomes into two non-overlapping groups → so nothing is double counted and nothing is missing.

---

## 3. General statement

If we split the sample space into parts:

$$
 A_1, A_2, ..., A_k
$$
### Conditions:

- No overlap:
- 
$$
  A_i \cap A_j = \emptyset
$$
  
- Together they cover everything:

$$
 A_1 \cup A_2 \cup ... \cup A_k = \Omega
$$

### Then:

$$
f(A_1)+f(A_2)+...+f(A_k)=1
$$

### Meaning

We are just saying:

> “If you split everything into clean, non-overlapping groups, then adding all their frequencies must give the full sample space.”

---

# Part E — Probability rules (explained)

## 1. Probability is between 0 and 1

$$
0 \le P(A) \le 1
$$

### Why?

- 0 = impossible event (never happens)
- 1 = certain event (always happens)
- Everything else is between these extremes

---

## 2. Impossible event

$$
P(\emptyset)=0
$$

### Why?

The empty set has no outcomes → nothing can happen → probability is 0.

---

## 3. Certain event

$$
P(\Omega)=1
$$

### Why?

Ω contains ALL outcomes → something from Ω MUST happen → probability is 1.

---

## 4. Addition rule (disjoint events)

$$
P(A \cup B)=P(A)+P(B)
$$

### Condition:

This ONLY works if:

$$
A \cap B = \emptyset
$$

### Why?

Because:
- nothing overlaps
- nothing is counted twice

So we can safely add.

---

## 5. Complement rule

$$
P(A^c)=1-P(A)
$$

### Meaning:

- A^c = everything NOT in A
- So together:

$$
A \cup A^c = \Omega
$$

### Why formula works:

Since total is 1:

$$
P(A) + P(A^c) = 1
$$

So:

$$
P(A^c)=1-P(A)
$$

---

# Final intuition

- Ω = everything that can happen  
- Probability = how the 1 unit is split  
- Splitting must always sum to 1  

# Part F — Conclusion

- Outcomes = raw results  
- Frequencies = experimental data  
- Probability = mathematical model of long-term behavior
