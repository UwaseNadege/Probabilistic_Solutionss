# Task 9 — Events and Probabilities in Weekly Weather Observation

We refer to **Task 4**, where the sample space describing the weather during **seven consecutive days** was defined.

Each day can have one of three possible states:

- Sunny ($S$)
- Cloudy ($C$)
- Rainy ($R$)

We assume:

- the weather on each day is **independent**,
- each state occurs with probability

$$
P(S)=P(C)=P(R)=\frac{1}{3}
$$

---

# 1. Sample Space

For one day:

$$
\Omega_1=\{S,C,R\}
$$

For seven days, the sample space consists of **ordered sequences of seven weather states**:

$$
\Omega_7=\{(x_1,x_2,x_3,x_4,x_5,x_6,x_7): x_i \in \{S,C,R\}\}
$$

Number of elementary outcomes:

$$
|\Omega_7| = 3^7 = 2187
$$

Since all sequences are equally likely, the probability of each elementary outcome is

$$
P(\omega)=\frac{1}{3^7}=\frac{1}{2187}
$$

### Example of One Outcome

A single weekly weather sequence could be:

This represents:

- **Monday** → Sunny  
- **Tuesday** → Cloudy  
- **Wednesday** → Rainy  
- **Thursday** → Sunny  
- **Friday** → Sunny  
- **Saturday** → Cloudy  
- **Sunday** → Rainy  

> I also have an HTML file that visually shows **all 2187 possible weekly outcomes** using colored boxes for S, C, and R — you can scroll through and see all sequences.
---

# 2. Event $A$ — The Entire Weekend Is Sunny

Weekend = **Saturday and Sunday**.

Both must be sunny.

Probability for Saturday:

$$
P(S)=\frac{1}{3}
$$

Probability for Sunday:

$$
P(S)=\frac{1}{3}
$$

Since the days are independent:

$$
P(A)=\frac{1}{3}\cdot\frac{1}{3}
$$

$$
P(A)=\frac{1}{9}
$$

---

# 3. Event $B$ — Wednesday, Thursday, and Friday Are Rainy

Each of these three days must be rainy.

Probability for each day:

$$
P(R)=\frac{1}{3}
$$

Thus

$$
P(B)=\left(\frac{1}{3}\right)^3
$$

$$
P(B)=\frac{1}{27}
$$

---

# 4. Event $C$ — At Least One Sunny Day

It is easier to compute the **complement event**:

"No sunny day occurs".

That means every day is either **cloudy or rainy**.

Probability that one day is **not sunny**:

$$
\frac{2}{3}
$$

“Not sunny” means Cloudy or Rainy.

Since each has probability $\frac{1}{3}$:

$$
P(\text{not sunny}) = \frac{1}{3} + \frac{1}{3} = \frac{2}{3}
$$

Thus

$$
P(\text{no sunny day})=\left(\frac{2}{3}\right)^7
$$

Since days are independent, we multiply the probability for all 7 days


Therefore

$$
P(C)=1-\left(\frac{2}{3}\right)^7
$$

---

# 5. Event $D$ — No Rainy Day During the Week

Each day must be either:

- Sunny
- Cloudy

Probability for one day:

$$
\frac{2}{3}
$$

Thus

$$
P(D)=\left(\frac{2}{3}\right)^7
$$

---

# 6. Event $E$ — Exactly Two Sunny Days

We must:

1. Choose **2 days out of 7** that are sunny.
2. The remaining **5 days must be not sunny**.

Number of ways to choose 2 sunny days:

$$
\binom{7}{2}=21
$$

### Combination Formula

The formula for combinations is:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

---

### Example:

$$
\binom{7}{2} = \frac{7!}{2! \cdot 5!}
$$

---

### Step by Step:

$$
7! = 7 \cdot 6 \cdot 5!
$$

Substitute:

$$
\frac{7 \cdot 6 \cdot 5!}{2 \cdot 1 \cdot 5!}
$$

Cancel $5!$:

$$
\frac{7 \cdot 6}{2} = 21
$$

---

### Final Answer:

$$
\binom{7}{2} = 21
$$

Probability of a specific arrangement:

- 2 sunny days:

$$
\left(\frac{1}{3}\right)^2
$$

- 5 non-sunny days:

$$
\left(\frac{2}{3}\right)^5
$$

Thus

$$
P(E)=\binom{7}{2}\left(\frac{1}{3}\right)^2\left(\frac{2}{3}\right)^5
$$

---

# 7. Additional Event

Define a new event:

Event $F$ — **all seven days are the same type of weather**.

Possible sequences:

- all sunny
- all cloudy
- all rainy

Number of such outcomes:

$$
3
$$

Probability of one specific sequence:

$$
\left(\frac{1}{3}\right)^7
$$

Thus

$$
P(F)=3\left(\frac{1}{3}\right)^7
$$

$$
P(F)=\frac{3}{2187}
$$

$$
P(F)=\frac{1}{729}
$$

---

# Key Idea

Because the weather on each day is assumed **independent**, probabilities for sequences of days are computed by **multiplying the probabilities of the individual days**.

Events involving **"at least" or "none"** are often easier to compute using **complement probabilities**.
```
