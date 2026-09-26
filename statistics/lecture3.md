## Conditional Probability

**Meaning**

Conditional probability means finding the probability of an event when we already know that another event has happened.

### 1. \(P(B|A)\)

Read as:

**“Probability of B given A.”**

Meaning:

> We already know A happened. What is the probability of B?

Formula:

$$
P(B|A)=\frac{P(A\cap B)}{P(A)}
$$

Remember:

**The event after `|` is the condition, so it becomes the denominator.**

Example:

* A = student is a boy
* B = student passed

$$
P(B|A)=P(\text{Passed}|\text{Boy})
$$

If 60 boys exist and 30 boys passed:

$$
P(\text{Passed}|\text{Boy})
=
\frac{30}{60}
=
0.5
=
50\%
$$

---

### 2. \(P(A|B)\)

Read as:

**“Probability of A given B.”**

Meaning:

> We already know B happened. What is the probability of A?

Formula:

$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$

Example:

If 50 students passed and 30 of those students were boys:

$$
P(\text{Boy}|\text{Passed})
=
\frac{30}{50}
=
0.6
=
60\%
$$

---

### 3. The easiest rule

Look at what comes **after `|`**.

$$
P(B|A)
$$

→ We know **A** → denominator is \(P(A)\)

$$
P(A|B)
$$

→ We know **B** → denominator is \(P(B)\)

### Memory trick

$$
\boxed{\text{Conditional probability}=
\frac{\text{Both}}{\text{Given}}}
$$

---

### 4. Intersection / AND

$$
A\cap B
$$

means:

**A and B happen together.**

In a Venn diagram, \(A\cap B\) is the **overlapping region**.

---

### 5. Multiplication Rule

Conditional probability can be rearranged to find the probability that **both events happen**:

$$
\boxed{P(A\cap B)=P(A)\times P(B|A)}
$$

Example:

$$
P(A)=0.6
$$

$$
P(B|A)=0.5
$$

Therefore:

$$
P(A\cap B)
=
0.6\times0.5
=
0.30
$$

So:

$$
\boxed{P(A\cap B)=30\%}
$$

---

### 6. Three formulas to remember

**Conditional probability:**

$$
\boxed{P(B|A)=\frac{P(A\cap B)}{P(A)}}
$$

**Reverse conditional probability:**

$$
\boxed{P(A|B)=\frac{P(A\cap B)}{P(B)}}
$$

**Multiplication rule:**

$$
\boxed{P(A\cap B)=P(A)P(B|A)}
$$

### One-line memory

**Given → denominator**

**Both → numerator**

**AND → multiplication**
