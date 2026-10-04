Here is a complete, structured summary of all the Hypothesis Testing concepts covered across your lecture slides and our discussion.

---

## 1. Fundamental Concepts of Hypothesis Testing

* **Definition:** Hypothesis testing uses sample statistics to make an inferential decision about an entire population parameter.


* **Population vs. Sample:** We cannot test every item in a population (e.g., all manufactured tyres). Instead, we draw a representative sample of size $n$, measure its properties, and determine if the sample data contradicts a claim about the population.



---

## 2. Null ($H_0$) vs. Alternative ($H_a$) Hypotheses

| Hypothesis | Definition | Mathematical Symbols |
| --- | --- | --- |
| **Null Hypothesis ($H_0$)** | Statement about a population parameter that assumes equality or status quo.

 | $\le, =, \ge$<br> |
| **Alternative Hypothesis ($H_a$ or $H_1$)** | Complement of $H_0$; represents strict inequality and the claim to be tested.

 | $>, \neq, <$<br> |

---

## 3. Direction of Tests (Tails)

The direction of the test is governed strictly by the symbol in the alternative hypothesis ($H_a$):

* **Left-Tailed Test ($H_a: \mu < k$):** The critical/rejection region lies entirely in the left tail.


* **Right-Tailed Test ($H_a: \mu > k$):** The critical/rejection region lies entirely in the right tail.


* **Two-Tailed Test ($H_a: \mu \neq k$):** The critical/rejection region is split equally between both left and right tails.

---

## 4. Decision Errors in Hypothesis Testing

Because decisions are based on samples, two types of errors can occur:

| Decision | $H_0$ is True | $H_0$ is False |
| --- | --- | --- |
| **Do not reject $H_0$** | Correct decision

 | **Type II Error ($\beta$):** Null is false, but not rejected.

 |
| **Reject $H_0$** | **Type I Error ($\alpha$):** Null is true, but rejected.

 | Correct decision

 |

---

## 5. Level of Significance ($\alpha$) and $p$-Value

* **Level of Significance ($\alpha$):** The maximum tolerable probability of making a Type I error (commonly $1\%$, $5\%$, or $10\%$).


* **$p$-Value:** The probability of obtaining a sample statistic as extreme as, or more extreme than, the observed sample data, assuming $H_0$ is true.



### Decision Rule Based on $p$-Value:

1. **$p \le \alpha$:** Reject $H_0$ (statistically significant; support $H_a$).


2. **$p > \alpha$:** Fail to reject $H_0$ (not statistically significant).



---

## 6. Step-by-Step Testing Procedure (Single Mean)

1. **Formulate Hypotheses:** Set up $H_0$ and $H_a$.


2. **Select Significance Level ($\alpha$):** Choose $0.01$, $0.05$, or $0.10$.


3. **Compute Test Statistic ($z$):**

$$z = \frac{\bar{x} - \mu}{\sigma_{\bar{x}}} = \frac{\bar{x} - \mu}{\frac{s}{\sqrt{n}}}$$



4. **Determine Critical Value ($Z_\alpha$) or $p$-Value:** Compare computed $z$ against standard normal $Z$-table values.


5. **Formulate Conclusion:** Reject or fail to reject $H_0$ and state the real-world interpretation.



---

## 7. Critical Value Reference Matrix ($Z_\alpha$)

| Test Type | $1\%$ ($\alpha = 0.01$) | $5\%$ ($\alpha = 0.05$) | $10\%$ ($\alpha = 0.10$) |
| --- | --- | --- | --- |
| **Two-Tailed ($\neq$)** | $\Vert{}Z_\alpha\Vert{} = 2.58$<br> | $\Vert{}Z_\alpha\Vert{} = 1.96$<br> | $\Vert{}Z_\alpha\Vert{} = 1.645$<br> |
| **Right-Tailed ($>$)** | $Z_\alpha = 2.33$<br> | $Z_\alpha = 1.65$<br> | $Z_\alpha = 1.28$<br> |
| **Left-Tailed ($<$)** | $Z_\alpha = -2.33$<br> | $Z_\alpha = -1.65$<br> | $Z_\alpha = -1.28$<br> |

* **Decision Rule:** For a right-tailed test, reject $H_0$ if $z_{\text{calculated}} \ge Z_\alpha$. For a left-tailed test, reject $H_0$ if $z_{\text{calculated}} \le Z_\alpha$. For a two-tailed test, reject $H_0$ if $\Vert{}z_{\text{calculated}}\Vert{} \ge \Vert{}Z_\alpha\Vert{}$.
