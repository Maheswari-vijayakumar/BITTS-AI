Here is the complete summary updated to include both worked-out numerical examples from your slides (the Tyre example and the Fast Food Sodium example).

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

## 6. Critical Value Reference Matrix ($Z_\alpha$)

| Test Type | $1\%$ ($\alpha = 0.01$) | $5\%$ ($\alpha = 0.05$) | $10\%$ ($\alpha = 0.10$) |
| --- | --- | --- | --- |
| **Two-Tailed ($\neq$)** | $\Vert{}Z_\alpha\Vert{} = 2.58$<br> | $\Vert{}Z_\alpha\Vert{} = 1.96$<br> | $\Vert{}Z_\alpha\Vert{} = 1.645$<br> |
| **Right-Tailed ($>$)** | $Z_\alpha = 2.33$<br> | $Z_\alpha = 1.65$<br> | $Z_\alpha = 1.28$<br> |
| **Left-Tailed ($<$)** | $Z_\alpha = -2.33$<br> | $Z_\alpha = -1.65$<br> | $Z_\alpha = -1.28$<br> |

* **Decision Rule:** For a right-tailed test, reject $H_0$ if $z_{\text{calculated}} \ge Z_\alpha$. For a left-tailed test, reject $H_0$ if $z_{\text{calculated}} \le Z_\alpha$. For a two-tailed test, reject $H_0$ if $\Vert{}z_{\text{calculated}}\Vert{} \ge \Vert{}Z_\alpha\Vert{}$.



---

## 7. Step-by-Step Testing Procedure & Worked Examples

### Worked Example 1: Tyre Life Span (Two-Tailed Concept)

* **Problem:** Company claims tyre mean life is $50,000\text{ km}$. You test $n = 30$ tyres, finding $\bar{x} = 47,000\text{ km}$ and $s = 5,500\text{ km}$.



1. **Hypotheses:** $H_0: \mu = 50,000$, $H_a: \mu \neq 50,000$

2. **Standard Error:** $\sigma_{\bar{x}} = \frac{5500}{\sqrt{30}} \approx 1004.2\text{ km}$
3. **Test Statistic ($z$):** $z = \frac{47000 - 50000}{1004.2} = -2.99$
4. **Conclusion:** $p\text{-value} = 0.0013$ ($0.13\%$). Since $0.0013 \le 0.05$, **Reject $H_0$**. The advertisement claim is likely false.



---

### Worked Example 2: Fast Food Sodium Content (Right-Tailed)

* **Problem:** Restaurant claims mean sodium is no more than $920\text{ mg}$. A sample of $n = 44$ has $\bar{x} = 925\text{ mg}$ and $s = 18\text{ mg}$ at $\alpha = 0.05$.



1. **Hypotheses:** $H_0: \mu \le 920$ **(Claim)**, $H_a: \mu > 920$

2. **Test Statistic ($z$):**

$$z = \frac{\bar{x} - \mu}{\frac{s}{\sqrt{n}}} = \frac{925 - 920}{\frac{18}{\sqrt{44}}} = \frac{5}{2.7136} = 1.842$$



3. **Critical Value:** Right-tailed test at $\alpha = 0.05 \rightarrow Z_\alpha = 1.65$.


4. **Decision:** $1.842 > 1.65 \rightarrow$ **Reject $H_0$**.


5. **Conclusion:** There is sufficient evidence at $\alpha = 0.05$ to reject the restaurant's claim that sodium is no more than $920\text{ mg}$. The sodium content is significantly higher.
