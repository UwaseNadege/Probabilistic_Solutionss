# Task 2 — Hypergeometric Model (Sampling from a Batch)

---

## **Problem**

A warehouse contains 20 components, of which:
- 5 are **defective**,  
- 15 are **functional**.  

We randomly select **4 components without replacement** for inspection.

### **Tasks**

1. Describe the random experiment.  
2. Define the random variable \(X\) as the number of defective elements in the sample.  
3. Determine the possible values of \(X\).  
4. Provide the probability distribution.  
5. Explain what a success means in this model.  

---

## **1. Description of the Random Experiment**

We randomly select **4 components from 20**, one after another, **without replacement**.

- “Without replacement” means:
  - once a component is selected, it is **not returned**,  
  - so probabilities **change during the process**.

Each selected component can be:
- defective (D),  
- functional (F).  

- **Important idea:**  
Because we do not replace items, the trials are **not independent**.

---

## **2. Definition of the Random Variable**

We define:

$$
X = \text{number of defective components in the sample of 4}
$$

- So \(X\) counts how many defectives appear in the selected group.

---

## **3. Possible Values of \(X\)**

- Minimum value:  
  - we could select **no defective components** → \(X = 0\)

- Maximum value:  
  - there are only 5 defective components total,  
  - but we only draw 4 → maximum is \(X = 4\)

So:

$$
X \in \{0, 1, 2, 3, 4\}
$$

---

## **4. Probability Distribution**

This is a **hypergeometric model** because:

- finite population (20 components),  
- two types (defective / functional),  
- sampling **without replacement**.

---

### **General Formula**

$$
P(X = k) =
\frac{C(5,k) \cdot C(15, 4-k)}{C(20,4)}
$$

- **Explanation of the formula:**

  - \(C(5,k)\): choose \(k\) defective components from 5  
  - \(C(15,4-k)\): choose the remaining components from 15 functional ones  
  - \(C(20,4)\): total ways to choose 4 components  

---

### **Compute the denominator**

$$
C(20,4) =
\frac{20!}{4! \cdot 16!} \\
= 4,845
$$

---

### **Now compute probabilities**

#### **For \(X = 0\)**

$$
P(X=0) =
\frac{C(5,0)\cdot C(15,4)}{C(20,4)} \\
= \frac{1 \cdot 1,365}{4,845} \\
= \frac{1,365}{4,845}
$$

---

#### **For \(X = 1\)**

$$
P(X=1) =
\frac{C(5,1)\cdot C(15,3)}{C(20,4)} \\
= \frac{5 \cdot 455}{4,845} \\
= \frac{2,275}{4,845}
$$

---

#### **For \(X = 2\)**

$$
P(X=2) =
\frac{C(5,2)\cdot C(15,2)}{C(20,4)} \\
= \frac{10 \cdot 105}{4,845} \\
= \frac{1,050}{4,845}
$$

---

#### **For \(X = 3\)**

$$
P(X=3) =
\frac{C(5,3)\cdot C(15,1)}{C(20,4)} \\
= \frac{10 \cdot 15}{4,845} \\
= \frac{150}{4,845}
$$

---

#### **For \(X = 4\)**

$$
P(X=4) =
\frac{C(5,4)\cdot C(15,0)}{C(20,4)} \\
= \frac{5 \cdot 1}{4,845} \\
= \frac{5}{4,845}
$$

---

### **Summary Table**

| \(X\) | Probability |
|------|------------|
| 0 | $1365 / 4845$ |
| 1 | $2275 / 4845$ |
| 2 | $1050 / 4845$ |
| 3 | $150 / 4845$ |
| 4 | $5 / 4845$ |

---

## **5. Definition of Success**

We define:

$$
\text{Success} = \text{"a selected component is defective"}
$$

So:

- Each time we pick a defective component → it counts as **1 success**  
- The random variable \(X\) counts the **total number of successes**

---

## ✅ **Final Interpretation**

This is a **hypergeometric distribution**:

$$
X \sim \text{Hypergeometric}(N=20, K=5, n=4)
$$

where:

- \(N = 20\): total components  
- \(K = 5\): defective components  
- \(n = 4\): number of draws  

---

## 🧠 **Key Idea**

- We are selecting **without replacement**,  
- so probabilities **change after each draw**,  
- which is why we use the **hypergeometric model instead of binomial**.
