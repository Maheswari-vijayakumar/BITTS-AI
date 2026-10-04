Here is the updated master summary incorporating this new light bulb example along with the previous topics.

---

## 1. Fundamental Concepts of Hypothesis Testing

* **Definition:** Hypothesis testing uses sample statistics to make an inferential decision about an entire population parameter.


* **Population vs. Sample:** We cannot test every item in a population (e.g., all manufactured tyres or light bulbs). Instead, we draw a representative sample of size $n$, measure its properties, and determine if the sample data contradicts a claim about the population.



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



### Decision Rules:

1. **Using $p$-Value:** If $p \le \alpha$, reject $H_0$. If $p > \alpha$, fail to reject $H_0$.


2. **Using Critical Values ($Z_\alpha$):**
* **Right-Tailed:** Reject $H_0$ if $z_{\text{calculated}} \ge Z_\alpha$.


* **Left-Tailed:** Reject $H_0$ if $z_{\text{calculated}} \le Z_\alpha$ (i.e., further to the left in the rejection region).


* **Two-Tailed:** Reject $H_0$ if $\vert{}z_{\text{calculated}}\vert{} \ge \vert{}Z_\alpha\vert{}$.





---

## 6. Critical Value Reference Matrix ($Z_\alpha$)

| Test Type | $1\%$ ($\alpha = 0.01$) | $5\%$ ($\alpha = 0.05$) | $10\%$ ($\alpha = 0.10$) |
| --- | --- | --- | --- |
| **Two-Tailed ($\neq$)** | $\vert{}Z_\alpha\vert{} = 2.58$<br> | $\vert{}Z_\alpha\vert{} = 1.96$<br> | $\vert{}Z_\alpha\vert{} = 1.645$<br> |
| **Right-Tailed ($>$)** | $Z_\alpha = 2.33$<br> | $Z_\alpha = 1.65$<br> | $Z_\alpha = 1.28$<br> |
| **Left-Tailed ($<$)** | $Z_\alpha = -2.33$<br> | $Z_\alpha = -1.65$<br> | $Z_\alpha = -1.28$<br> |

---

## 7. Step-by-Step Testing Procedure & All Worked Examples

### Worked Example 1: Tyre Life Span (Two-Tailed Concept)

* **Problem:** Company claims tyre mean life is $50,000\text{ km}$. Sample of $n = 30$ gives $\bar{x} = 47,000\text{ km}$ and $s = 5,500\text{ km}$.



1. **Hypotheses:** $H_0: \mu = 50,000$, $H_a: \mu \neq 50,000$

2. **Test Statistic ($z$):** $z = \frac{47000 - 50000}{\frac{5500}{\sqrt{30}}} \approx -2.99$
3. **Conclusion:** $p\text{-value} = 0.0013$ ($0.13\%$). Since $0.0013 \le 0.05$, **Reject $H_0$**. The advertisement claim is likely false.



---

### Worked Example 2: Fast Food Sodium Content (Right-Tailed Test)

* **Problem:** Restaurant claims mean sodium is no more than $920\text{ mg}$. Sample of $n = 44$ gives $\bar{x} = 925\text{ mg}$ and $s = 18\text{ mg}$ at $\alpha = 0.05$.



1. **Hypotheses:** $H_0: \mu \le 920$ **(Claim)**, $H_a: \mu > 920$

2. **Test Statistic ($z$):**

$$z = \frac{925 - 920}{\frac{18}{\sqrt{44}}} = \frac{5}{2.7136} = 1.842$$



3. **Critical Value:** Right-tailed test at $\alpha = 0.05 \rightarrow Z_\alpha = 1.65$.


4. **Decision:** $1.842 > 1.65 \rightarrow$ **Reject $H_0$**.


5. **Conclusion:** Sufficient evidence to reject the restaurant's claim; mean sodium content is significantly greater than $920\text{ mg}$.



---

### Worked Example 3: Light Bulb Life Span (Left-Tailed Test)

* **Problem:** Manufacturer guarantees mean life is **more than** $750\text{ hours}$ ($\mu > 750$). Sample of $n = 36$ gives $\bar{x} = 745\text{ hours}$ and $s = 60\text{ hours}$ at $\alpha = 0.01$ ($1\%$).



1. **Hypotheses:**
* $H_0: \mu \ge 750$ **(Claim: Manufacturer guarantees $> 750$)**

* $H_a: \mu < 750$



2. **Test Statistic ($z$):**

$$z = \frac{\bar{x} - \mu}{\frac{s}{\sqrt{n}}} = \frac{745 - 750}{\frac{60}{\sqrt{36}}} = \frac{-5}{10} = -0.5$$



3. **Critical Value:** Left-tailed test at $\alpha = 0.01 \rightarrow Z_\alpha = -2.33$.


4. **Decision:** $z = -0.5$ is greater than $-2.33$ (it falls in the **acceptance region** to the right of $-2.33$). Therefore, **Do Not Reject $H_0$**.


5. **Conclusion:** There is not enough statistical evidence at $\alpha = 0.01$ to reject the manufacturer's claim. We cannot conclude that the mean life is less than $750\text{ hours}$.
