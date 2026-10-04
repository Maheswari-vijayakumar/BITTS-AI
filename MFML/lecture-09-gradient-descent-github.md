<!-- GitHub Markdown:
     Display equations use $$ ... $$.
     Inline equations use $ ... $.
-->

# Gradient Descent — Exam Notes

**Course:** ZC416 Mathematical Foundations for Machine Learning / Data Science  
**Topic:** Gradient Descent  
**Source:** Lecture 9 PDF — BITS Pilani

---

# 1. Continuous Optimization

Optimization means finding the value of parameters that **minimize or maximize an objective function**.

For Gradient Descent, we are usually interested in:

$$
\min_x f(x)
$$

where:

- \(x\) = parameters
- \(f(x)\) = objective/loss function

## Two types of optimization

### Unconstrained optimization

No restrictions on the parameters.

$$
\min_x f(x)
$$

### Constrained optimization

Parameters must satisfy certain constraints.

Example:

$$
x \geq 0
$$

---

# 2. Gradient

The **gradient** tells us the direction in which a function increases the fastest.

For a function:

$$
f(x_1,x_2)
$$

the gradient is:

$$
\nabla f =
\begin{bmatrix}
\frac{\partial f}{\partial x_1}\\
\frac{\partial f}{\partial x_2}
\end{bmatrix}
$$

### Important idea

$$
\boxed{\text{Gradient} \rightarrow \text{direction of maximum increase}}
$$

Therefore, to decrease the function, we move in the **opposite direction**:

$$
\boxed{-\nabla f}
$$

---

# 3. Local Minimum

A **local minimum** is a point that is lower than the nearby points.

Think of a valley:

```text
        \       /
         \     /
          \___/
            ↑
       local minimum
```

It does **not necessarily mean** it is the lowest point everywhere.

### Local vs Global Minimum

| Type | Meaning |
|---|---|
| Local minimum | Lowest in a nearby region |
| Global minimum | Lowest everywhere |

---

# 4. Example: Fitting a Straight Line

Suppose our dataset is:

| x | y |
|---:|---:|
| 1 | 3.1 |
| 2 | 4.9 |
| 3 | 7.3 |
| 4 | 9.1 |

We want to fit:

$$
\hat y=ax+b
$$

where:

- \(a\) = slope
- \(b\) = intercept

For every data point:

$$
\hat y_i=ax_i+b
$$

---

# 5. Loss Function

We want our predictions to be as close as possible to the actual values.

The PDF uses the squared-error loss:

$$
L(a,b)=\sum_{i=1}^{4}(y_i-\hat y_i)^2
$$

Substituting:

$$
L(a,b)=
\sum_{i=1}^{4}
(y_i-(ax_i+b))^2
$$

Our goal is:

$$
\boxed{\min_{a,b}L(a,b)}
$$

---

# 6. How Gradient Descent Works

Suppose we have:

$$
f(x)
$$

The gradient tells us which direction makes \(f(x)\) increase.

Therefore, we move in the opposite direction:

$$
-\nabla f(x)
$$

The Gradient Descent update is:

$$
\boxed{x_{\text{new}}=x-\gamma\nabla f(x)}
$$

where:

- \(x\) = current parameter
- \(\nabla f(x)\) = gradient
- \(\gamma\) = learning rate / step size

---

# 7. Gradient vs Learning Rate

### Gradient

Tells us:

> **Which direction should I move?**

### Learning rate

Tells us:

> **How big should my step be?**

Therefore:

$$
\boxed{\text{Gradient}=\text{direction}}
$$

$$
\boxed{\text{Learning rate}=\text{step size}}
$$

---

# 8. Simple Gradient Descent Example

Suppose:

$$
L(x)=x^2
$$

Derivative:

$$
\frac{dL}{dx}=2x
$$

Start with:

$$
x=5
$$

Learning rate:

$$
\gamma=0.1
$$

### Step 1: Calculate gradient

$$
\nabla L=2(5)=10
$$

### Step 2: Update

$$
x_{\text{new}}=5-(0.1)(10)
$$

$$
x_{\text{new}}=4
$$

So:

$$
\boxed{x_{\text{new}}=4}
$$

---

# 9. Another Example

Now:

$$
x=4
$$

Gradient:

$$
2(4)=8
$$

Update:

$$
x_{\text{new}}
=
4-(0.1)(8)
$$

$$
=3.2
$$

So:

$$
4\rightarrow3.2
$$

We continue this process until we get close to the minimum.

For:

$$
L(x)=x^2
$$

the minimum is:

$$
\boxed{x=0}
$$

---

# 10. Why Negative Gradient?

The gradient points toward **maximum increase**.

We want to decrease the objective.

Therefore:

$$
\boxed{\text{Move in the opposite direction of the gradient}}
$$

Hence:

$$
\boxed{x_{new}=x-\gamma\nabla f(x)}
$$

---

# 11. Gradient = 0

At a local minimum, the function becomes flat.

Therefore, we often look for:

$$
\boxed{\nabla f(x)=0}
$$

However:

> Gradient = 0 does **not automatically mean minimum**.

It can also be a maximum or another stationary point.

---

# 12. Example: Polynomial

Consider:

$$
l(x)=x^4+7x^3+5x^2-17x+3
$$

Derivative:

$$
l'(x)=4x^3+21x^2+10x-17
$$

To find stationary points:

$$
l'(x)=0
$$

The second derivative is:

$$
l''(x)=12x^2+42x+10
$$

The second derivative helps determine the shape around the stationary point.

### Shape intuition

```text
Local minimum:

     \     /
      \___/


Local maximum:

      /\
     /  \
```

---

# 13. Why Gradient Descent?

For simple low-order functions, we may solve the optimization problem analytically.

But for complicated real-world functions, finding the minimum analytically may not be possible.

Gradient Descent provides an iterative method:

$$
\boxed{x_{i+1}=x_i-\gamma_i\nabla f(x_i)}
$$

We repeatedly move toward lower objective values.

---

# 14. Learning Rate

The learning rate is usually represented by:

$$
\gamma
$$

or:

$$
\alpha
$$

It controls the size of the step.

## Learning Rate Too Small

Training becomes slow.

## Learning Rate Too Large

We may jump over the minimum.

This can cause:

$$
\boxed{\text{Overshooting / Oscillation}}
$$

---

# 15. Learning Rate Decay

A large learning rate can be useful when we are far from the minimum.

But near the minimum, we want smaller steps.

Therefore:

$$
\boxed{\text{Large learning rate initially}}
$$

and:

$$
\boxed{\text{Small learning rate later}}
$$

This is called **learning rate decay**.

---

# 16. Variable Learning Rate

Instead of using a constant:

$$
\alpha
$$

we use:

$$
\alpha_t
$$

The update becomes:

$$
\boxed{
w_{n+1}=w_n-\alpha_t\nabla J
}
$$

The learning rate changes as training progresses.

---

# 17. Learning Rate Decay Methods

## 17.1 Exponential Decay

$$
\boxed{
\alpha_t=\alpha_0e^{-kt}
}
$$

where:

- \(\alpha_0\) = initial learning rate
- \(k\) = decay parameter
- \(t\) = training progress

## 17.2 Inverse Decay

$$
\boxed{
\alpha_t=\frac{\alpha_0}{1+kt}
}
$$

As \(t\) increases:

$$
\alpha_t\downarrow
$$

## 17.3 Step Decay

Reduce the learning rate after fixed intervals.

| Iterations | Learning Rate |
|---:|---:|
| 0–100 | 0.10 |
| 101–200 | 0.05 |
| 201–300 | 0.025 |
| 301–400 | 0.0125 |

---

# 18. Bold Driver Algorithm

Bold Driver automatically adjusts the learning rate based on whether the objective improves.

### If objective improves

Increase learning rate by approximately 5%.

$$
\boxed{\alpha_{\text{new}}=\alpha\times1.05}
$$

### If objective gets worse

Undo the step and reduce the learning rate by approximately 50%.

$$
\boxed{\alpha_{\text{new}}=\alpha\times0.5}
$$

## Percentage Example

Suppose:

$$
\alpha=0.4
$$

Increase by 5%:

$$
0.4\times1.05=0.42
$$

If we reduce 0.42 by 50%:

$$
0.42\times0.5=0.21
$$

---

# 19. Line Search

Line Search addresses:

> **How far should we move in the descent direction?**

The gradient gives the direction:

$$
\boxed{g_t=-\nabla J(w_t)}
$$

This is the **steepest descent direction**.

The update can be written:

$$
\boxed{
w_{t+1}=w_t+\alpha_tg_t
}
$$

where:

- \(g_t\) = direction
- \(\alpha_t\) = step size

---

# 20. Line Search Example

| Step size \(\alpha\) | Loss |
|---:|---:|
| 0.1 | 8 |
| 0.2 | 5 |
| 0.3 | 2 |
| 0.4 | 4 |
| 0.5 | 9 |

The best step is:

$$
\boxed{\alpha=0.3}
$$

because it gives the lowest loss.

---

# 21. Line Search Formula

$$
\boxed{
\alpha_t=\arg\min_\alpha J(w_t+\alpha g_t)
}
$$

In simple words:

> Try different step sizes along the chosen direction and find the one that gives the lowest objective.

---

# 22. Gradient Perpendicular to Search Direction

At the optimal point found by line search:

$$
\boxed{
\nabla J(w_{t+1})^Tg_t=0
}
$$

A dot product of zero means the vectors are perpendicular.

Therefore:

$$
\boxed{
\text{Gradient}\perp\text{Search Direction}
}
$$

Why?

If the gradient were not perpendicular, we could move a little further along the same direction and improve the objective.

---

# 23. Unimodal Function

Line search often reduces the problem to finding the minimum of a function of one variable:

$$
J(w_t+\alpha g_t)
$$

A **unimodal** function has one main minimum.

```text
Loss
 ↑
 | \       /
 |  \     /
 |   \___/
 |      ↑
 |   best α
 +--------------→ α
```

---

# 24. Methods for Finding the Best Step

The PDF introduces:

1. Binary Search
2. Golden-Section Search
3. Armijo Search

---

# 25. Binary Search

Suppose:

$$
\alpha\in[0,1]
$$

Start with:

```text
0 ---------------------- 1
```

Check around the middle:

$$
\alpha=0.5
$$

Based on whether the objective is increasing or decreasing, eliminate part of the interval.

Then repeat until the interval becomes small.

---

# 26. Golden-Section Search

Golden-Section Search repeatedly narrows the interval containing the minimum.

It chooses points according to a special ratio related to the golden ratio.

Basic idea:

```text
0 ------------------------------ 1
       ●              ●
       a              b
```

Evaluate the objective at the points and discard the region that cannot contain the minimum.

Repeat until the interval is sufficiently small.

$$
\boxed{
\text{Golden Section}=\text{repeatedly shrink the search interval}
}
$$

---

# 27. Why Don't We Always Use Line Search?

Line Search can find a good step size, but it can be **computationally expensive**.

We may need to evaluate the objective multiple times:

```text
α = 0.1 → calculate objective
α = 0.2 → calculate objective
α = 0.3 → calculate objective
α = 0.4 → calculate objective
...
```

Therefore:

$$
\boxed{
\text{Line Search = potentially better step size but more computation}
}
$$

It is rarely used in vanilla Gradient Descent.

---

# 28. Batch Gradient Descent

Suppose there are \(N\) training examples.

Each example has a loss:

$$
L_1(\theta),L_2(\theta),...,L_N(\theta)
$$

Total loss:

$$
\boxed{
L(\theta)=\sum_{n=1}^{N}L_n(\theta)
}
$$

Batch Gradient Descent uses **all training examples** to calculate the gradient.

$$
\boxed{\text{Batch GD = ALL data}}
$$

---

# 29. Problem with Batch Gradient Descent

Suppose:

$$
N=10,000,000
$$

For every update, we may need to process all 10 million examples.

This can be computationally expensive.

---

# 30. Mini-Batch / Stochastic Gradient Descent

Instead of using the complete dataset, we can use a subset.

Suppose:

$$
S\subseteq\{1,\ldots,N\}
$$

The sample objective can be written as:

$$
\boxed{
J(S)=\sum_{i\in S}(w^TX_i-y_i)^2
}
$$

The gradient calculated from the subset approximates the full gradient:

$$
\boxed{
\nabla J_{\text{subset}}
\approx
\nabla J_{\text{full}}
}
$$

---

# 31. Batch vs Mini-Batch vs SGD

| Method | Data used |
|---|---|
| **Batch GD** | ALL data |
| **Mini-Batch GD** | SOME data |
| **SGD** | ONE data point |

### Example

Dataset:

$$
1000\text{ examples}
$$

Using all 1000:

$$
\boxed{\text{Batch GD}}
$$

Using 50:

$$
\boxed{\text{Mini-Batch GD}}
$$

Using 1 randomly selected example:

$$
\boxed{\text{SGD}}
$$

---

# 32. Gradient Variance

Because mini-batches are random, their gradients may not point exactly in the same direction as the full gradient.

This variation is called **gradient variance**.

### Larger mini-batches

Larger mini-batches generally produce a more stable gradient estimate.

$$
\boxed{
\text{Larger mini-batch}
\Rightarrow
\text{Lower gradient variance}
}
$$

---

# 33. Why Use Mini-Batch GD?

Mini-batch GD provides a practical balance.

| Method | Computation | Gradient |
|---|---|---|
| Batch | Expensive | Accurate |
| Mini-Batch | Moderate | Approximate |
| SGD | Cheap per update | Noisy |

Therefore:

$$
\boxed{
\text{Mini-Batch GD = practical middle ground}
}
$$

---

# 34. SGD Convergence

With a suitable **decaying learning rate** and under mild assumptions, SGD can converge to a local minimum almost surely.

For exam understanding:

$$
\boxed{
\text{SGD + suitable learning-rate decay}
\Rightarrow
\text{can converge}
}
$$

---

# 35. Gradient Correctness — Finite Difference

We can check whether a calculated gradient is approximately correct using a **finite-difference approximation**.

For a parameter \(w_i\):

$$
\boxed{
\frac{\partial J}{\partial w_i}
\approx
\frac{
J(w_i+\Delta)-J(w_i)
}{\Delta}
}
$$

## Example

Let:

$$
J(w)=w^2
$$

At:

$$
w=2,\qquad\Delta=0.01
$$

Calculate:

$$
J(2)=4
$$

$$
J(2.01)=4.0401
$$

Therefore:

$$
\frac{J(2.01)-J(2)}{0.01}
=
\frac{4.0401-4}{0.01}
$$

$$
=\boxed{4.01}
$$

The exact derivative is:

$$
\frac{d}{dw}w^2=2w
$$

At \(w=2\):

$$
2(2)=4
$$

Therefore:

$$
\boxed{4.01\approx4}
$$

---

# 36. Most Important Formulas

## Gradient Descent

$$
\boxed{
x_{new}=x-\gamma\nabla f(x)
}
$$

## Variable Learning Rate

$$
\boxed{
w_{n+1}=w_n-\alpha_t\nabla J
}
$$

## Exponential Decay

$$
\boxed{
\alpha_t=\alpha_0e^{-kt}
}
$$

## Inverse Decay

$$
\boxed{
\alpha_t=\frac{\alpha_0}{1+kt}
}
$$

## Steepest Descent Direction

$$
\boxed{
g_t=-\nabla J(w_t)
}
$$

## Line Search

$$
\boxed{
\alpha_t=\arg\min_\alpha J(w_t+\alpha g_t)
}
$$

## Line Search Update

$$
\boxed{
w_{t+1}=w_t+\alpha_tg_t
}
$$

## Perpendicularity at Line-Search Optimum

$$
\boxed{
\nabla J(w_{t+1})^Tg_t=0
}
$$

## Total Loss

$$
\boxed{
L(\theta)=\sum_{n=1}^{N}L_n(\theta)
}
$$

## Finite Difference

$$
\boxed{
\frac{\partial J}{\partial w_i}
\approx
\frac{J(w_i+\Delta)-J(w_i)}{\Delta}
}
$$

---

# 37. Exam Cheat Sheet

| Concept | Remember |
|---|---|
| Gradient | Direction of maximum increase |
| Negative gradient | Direction of decrease |
| Gradient Descent | Move opposite gradient |
| Learning rate | Controls step size |
| Large LR | Fast but can overshoot |
| Small LR | Stable but slow |
| Learning-rate decay | Large → small |
| Bold Driver | Improve → +5%; worsen → -50% |
| Line Search | Finds good/best step size |
| Unimodal | One main minimum |
| Binary Search | Narrow interval using midpoint |
| Golden Section | Narrow interval using special ratio |
| Armijo | Inexact practical search |
| Batch GD | All data |
| Mini-Batch GD | Some data |
| SGD | One data point |
| Larger mini-batch | Lower variance |
| Finite Difference | Approximate/check gradient |

---

# 38. Final Mental Model

```text
                GRADIENT DESCENT
                       │
                       ↓
             Find the gradient
                       │
                       ↓
             Which direction?
                       │
                       ↓
              Move opposite
              the gradient
                       │
                       ↓
            How big is the step?
                       │
             ┌─────────┴─────────┐
             ↓                   ↓
       Fixed learning       Line Search
           rate
             │                   │
             ↓                   ↓
       Use α directly       Find good α
             │
             ↓
       Learning-rate decay
             │
             ↓
       Large → Small
```

---

# 39. Final Memory Tricks

### Gradient Descent

> **Gradient = direction**

> **Learning rate = distance**

### Learning Rate

> **Too small = slow**

> **Too large = overshoot**

### Learning Rate Decay

> **Large initially → small later**

### Line Search

> **Gradient tells WHERE**

> **Line Search tells HOW FAR**

### Dataset Size

> **Batch = ALL**

> **Mini-Batch = SOME**

> **SGD = ONE**

### Mini-Batch Variance

> **Larger batch → lower variance**

### Finite Difference

> **Approximate gradient → compare with exact gradient**

---

# End of Lecture 9 — Gradient Descent
