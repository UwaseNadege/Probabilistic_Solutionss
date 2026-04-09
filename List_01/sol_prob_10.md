# Task 10 — Events and Probabilities in Buffon's Needle Experiment

We refer to **Task 5**, where the sample space of Buffon’s needle experiment was defined.

A needle of length $L$ is thrown randomly onto a floor with **parallel lines spaced by distance $d$**.

Assume:

- $L \le d$
- $X$ = distance from the **center of the needle** to the nearest line
- $\theta$ = **angle between the needle and the lines**

Ranges of the variables:

$$
X \in [0,\tfrac{d}{2}]
$$

$$
\theta \in [0,\tfrac{\pi}{2}]
$$

The symbol ∈ is a set theory symbol that means:

“is an element of” or “belongs to.”

We assume:

- $X$ and $\theta$ are **independent**
- both variables are **uniformly distributed**

Therefore the sample space is

$$
\Omega = \{(x,\theta) : x \in [0,\tfrac{d}{2}],\ \theta \in [0,\tfrac{\pi}{2}] \}
$$

The **area of the sample space** is

$$
|\Omega|=\frac{d}{2}\cdot\frac{\pi}{2}=\frac{d\pi}{4}
$$

Since the distribution is uniform, probabilities correspond to **areas of regions inside this rectangle**.

---

# 1. Event $A$ — The Needle Intersects a Line

The needle intersects a line when the **projection of half the needle onto the perpendicular direction to the lines exceeds $X$**.

Intersection condition:

$$
X \le \frac{L}{2}\sin\theta
$$

Thus the probability is

$$
P(A)=\frac{2L}{\pi d}
$$

This is the **classical result of Buffon's needle problem**.

---

# 2. Event $B$ — The Needle Does Not Intersect Any Line

This is the **complement of event $A$**.

Therefore

$$
P(B)=1-P(A)
$$

$$
P(B)=1-\frac{2L}{\pi d}
$$

---

# 3. Event $C$ — The Angle Is Smaller Than $\frac{\pi}{6}$

The angle $\theta$ is uniformly distributed in

$$
[0,\tfrac{\pi}{2}]
$$

Thus the probability equals the ratio of interval lengths:

$$
P(C)=\frac{\frac{\pi}{6}}{\frac{\pi}{2}}
$$

$$
P(C)=\frac{1}{3}
$$

---

# 4. Event $D$ — The Center Is Less Than $\frac{d}{4}$ from the Nearest Line

The variable $X$ is uniformly distributed in

$$
[0,\tfrac{d}{2}]
$$

Thus

$$
P(D)=\frac{\frac{d}{4}}{\frac{d}{2}}
$$

$$
P(D)=\frac{1}{2}
$$

---

# 5. Event $E$ — The Needle Intersects a Line and $\theta > \frac{\pi}{4}$

We combine two conditions:

1. Intersection condition

$$
X \le \frac{L}{2}\sin\theta
$$

2. Angle condition

$$
\theta > \frac{\pi}{4}
$$

Thus the probability corresponds to the **area of the region**

$$
\{(x,\theta):\theta \in [\tfrac{\pi}{4},\tfrac{\pi}{2}],\ x\le\frac{L}{2}\sin\theta\}
$$

The probability is

$$
P(E)=\frac{2}{\pi d}\int_{\pi/4}^{\pi/2} L\sin\theta \, d\theta
$$

Compute the integral:

$$
\int \sin\theta\,d\theta=-\cos\theta
$$

Thus

$$
P(E)=\frac{2L}{\pi d}\left[\cos\left(\tfrac{\pi}{4}\right)-\cos\left(\tfrac{\pi}{2}\right)\right]
$$

Since

$$
\cos\left(\tfrac{\pi}{4}\right)=\frac{\sqrt2}{2},\quad
\cos\left(\tfrac{\pi}{2}\right)=0
$$

we obtain

$$
P(E)=\frac{2L}{\pi d}\cdot\frac{\sqrt2}{2}
$$

$$
P(E)=\frac{\sqrt2\,L}{\pi d}
$$

---

# 6. Additional Event

Define event $F$:

The **angle is greater than $\frac{\pi}{3}$**.

Since $\theta$ is uniform on $[0,\tfrac{\pi}{2}]$,

$$
P(F)=\frac{\frac{\pi}{2}-\frac{\pi}{3}}{\frac{\pi}{2}}
$$

$$
P(F)=\frac{\frac{\pi}{6}}{\frac{\pi}{2}}
$$

$$
P(F)=\frac{1}{3}
$$

---

# Key Idea

Unlike previous tasks with **finite sample spaces**, Buffon's needle experiment has a **continuous sample space**.

Therefore probabilities are computed using **geometric probability**, where:

- the sample space corresponds to a **region in the plane $(x,\theta)$**,
- probabilities correspond to **areas of regions inside this space**.
```
