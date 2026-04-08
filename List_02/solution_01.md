# Task 1 — Binomial Model (Quality Control)

---

## **Problem**

In a factory, screws are produced. Each screw can be either **good** or **defective**.  
The probability that a randomly selected screw is defective equals \(p\).  

Assume that:
- inspections are **independent**,  
- the probability \(p\) is the **same for each screw**.  

We consider an experiment consisting of checking **3 consecutive screws**.

### **Tasks**

1. Describe the random experiment.  
2. Determine the sample space \( \Omega \).  
3. Specify the probabilities of the elements of the sample space.  
4. Define what is considered a success in this model.  

---

## **1. Description of the Random Experiment**

We inspect **3 screws one after another**.

For each screw, there are **two possible outcomes**:

- \(D\) — defective  
- \(G\) — good  

So the experiment consists of **3 independent trials**, each with the same probabilities:

$$
P(D) = p, \quad P(G) = 1 - p
$$

- **Why?**  
Because each screw has the same chance of being defective and inspections do not affect each other.

---

## **2. Sample Space \( \Omega \)**

- Each outcome is a **sequence of 3 results** (because we inspect 3 screws).  
- Each position can be either \(D\) or \(G\).  

Number of outcomes:

$$
2^3 = 8
$$

- **Sample space:**

$$
\Omega =
\{DDD, DDG, DGD, DGG, GDD, GDG, GGD, GGG\}
$$

- **Explanation:**  
Each of the 3 positions has 2 choices → multiply:

$$
2 \cdot 2 \cdot 2 = 8
$$

---

## **3. Probabilities of the Elements of \( \Omega \)**

Because the trials are **independent**, the probability of any sequence is:

$$
P(\text{sequence}) = \text{product of probabilities of each position}
$$

---

### **Examples**

#### **All defective**

$$
P(DDD) =
p \cdot p \cdot p \\
= p^3
$$

- **Explanation:** All three screws are defective → multiply \(p\) three times.

---

#### **Two defective, one good (example: DDG)**

$$
P(DDG) =
p \cdot p \cdot (1-p) \\
= p^2(1-p)
$$

- **Explanation:** Two defective (\(p\)) and one good (\(1-p\)).

---

#### **One defective, two good (example: DGG)**

$$
P(DGG) =
p \cdot (1-p) \cdot (1-p) \\
= p(1-p)^2
$$

---

#### **All good**

$$
P(GGG) =
(1-p)^3
$$

---

### **All Probabilities**

| Outcome | Probability |
|--------|------------|
| DDD | $p^3$ |
| DDG | $p^2(1-p)$ |
| DGD | $p^2(1-p)$ |
| GDD | $p^2(1-p)$ |
| DGG | $p(1-p)^2$ |
| GDG | $p(1-p)^2$ |
| GGD | $p(1-p)^2$ |
| GGG | $(1-p)^3$ |

- **Important idea:**  
Sequences with the same number of defective screws have the same probability.

---

## **4. Definition of Success**

In this model, we define:

$$
\text{Success} = \text{"a screw is defective"}
$$

So:

$$
P(\text{success}) = p
$$

---

### **Why this choice?**

- In a **binomial model**, we count the number of “successes”  
- Here we are interested in **defective screws** (quality control problem)  
- So it is natural to treat **defect = success**

---

## ✅ **Final Interpretation**

This experiment is a **binomial experiment** because:

- Fixed number of trials:

$$
n = 3
$$

- Two outcomes: defective or good  
- Constant probability \(p\)  
- Independent trials  

So the number of defective screws follows:

$$
X \sim \text{Bin}(3, p)
$$

---

## 🧠 **Key Idea**

We are not just listing outcomes — we are building a model that allows us to:

- count how many defective screws appear,  
- and compute probabilities using the binomial distribution.
