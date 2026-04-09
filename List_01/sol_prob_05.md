# Task 5 — Buffon's Needle Experiment

We consider **Buffon’s Needle Experiment**, a classical problem in geometric probability.

A needle of length $L$ is dropped randomly onto a floor with **equally spaced parallel lines**.  
The distance between neighboring lines is $d$.

Unlike previous tasks (coin tosses, die rolls, card draws), the outcome here is **not discrete**.  
Instead, it depends on **continuous geometric variables** describing the position and orientation of the needle.

---

# 1. Description of the Sample Space

The **sample space** $\Omega$ consists of **all possible positions and orientations of the needle** when it lands on the floor.

Each outcome corresponds to a particular:

- position of the needle relative to the nearest line,
- orientation angle of the needle.

Thus every possible landing configuration of the needle corresponds to **one elementary outcome**.

---

# 2. Parameters Determining a Single Outcome

The outcome of one needle throw can be completely described using **two variables**:

- $x$ — the **distance from the center of the needle to the nearest parallel line**.
- $\theta$ — the **angle between the needle and the parallel lines**.

These two parameters fully determine whether the needle **intersects a line**.

---

# 3. Representation of an Elementary Outcome

An elementary outcome can therefore be represented as the **ordered pair**

$$(x,\theta)$$

where

- $x$ describes the **position** of the needle relative to the nearest line,
- $\theta$ describes the **orientation angle** of the needle.

---

# 4. Mathematical Representation of the Sample Space

Because the lines are **periodic and symmetric**, we can restrict the variables to the following ranges:

$$x \in [0,\tfrac{d}{2}]$$

$$\theta \in [0,\tfrac{\pi}{2}]$$

Therefore the sample space can be written as

$$\Omega = \{(x,\theta) : x \in [0,\tfrac{d}{2}],\ \theta \in [0,\tfrac{\pi}{2}] \}$$

This set contains **all possible combinations of position and orientation** of the needle.

---

# 5. Why the Sample Space is Continuous

In the previous tasks:

- coin tosses,
- die rolls,
- card draws,

the sample spaces were **finite sets**.  
Each experiment had a **countable number of elementary outcomes**.

In Buffon's needle experiment, however:

- the distance $x$ can take **any real value** in an interval,
- the angle $\theta$ can also take **any real value** in an interval.

Thus the set of possible outcomes is **uncountably infinite**.

Because the variables vary **continuously**, the sample space is a **continuous sample space**, and probabilities must be described using **geometric probability or probability density functions**, rather than simple counting.
```
