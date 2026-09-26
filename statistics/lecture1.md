# Descriptive Statistics — Complete Notes

Descriptive statistics is the process of **organizing, summarizing, and describing data**.

The main goal is to understand a dataset using numbers, tables, and graphs without trying to make predictions about a larger population.

---

## 1. Mean

The mean is the **average** of the data.

### Formula

Mean = Sum of all values / Number of values

For a dataset with values x₁, x₂, ..., xₙ:

x̄ = (x₁ + x₂ + ... + xₙ) / n

### Example

Data:

2, 4, 6, 8, 10

Mean:

(2 + 4 + 6 + 8 + 10) / 5

= 30 / 5

= 6

So:

**Mean = 6**

### Important

The mean uses **every value** in the dataset.

Because of this, extreme values can strongly affect the mean.

---

## 2. Median

The median is the **middle value** after arranging the data from smallest to largest.

### Odd number of values

Data:

2, 4, 6, 8, 10

The middle value is:

**6**

So:

Median = 6

### Even number of values

Data:

2, 4, 6, 8

There are two middle values:

4 and 6

Median:

(4 + 6) / 2 = 5

So:

**Median = 5**

### Important

Always **sort the data first** before finding the median.

The median is less affected by extreme values than the mean.

---

## 3. Mode

The mode is the value that occurs **most frequently**.

### Example

Data:

2, 3, 3, 4, 5, 3, 6

The value 3 occurs three times.

Therefore:

**Mode = 3**

### Important

A dataset can have:

* No mode
* One mode
* More than one mode

---

## 4. Mean vs Median vs Mode

| Measure | Meaning             | Affected by extreme values? |
| ------- | ------------------- | --------------------------- |
| Mean    | Average             | Yes                         |
| Median  | Middle value        | Much less                   |
| Mode    | Most frequent value | Usually no                  |

Example:

Data:

2, 3, 4, 5, 100

Mean:

(2 + 3 + 4 + 5 + 100) / 5 = 22.8

Median:

4

The value 100 pulls the mean upward, while the median remains near the center of the original data.

---

## 5. Range

Range measures the total spread of the data.

### Formula

Range = Maximum value − Minimum value

### Example

Data:

10, 12, 15, 18, 20

Range:

20 − 10 = 10

Therefore:

**Range = 10**

### Important

Range is easy to calculate, but it uses only two values:

* Minimum
* Maximum

Therefore, one extreme value can greatly change the range.

---

## 6. Variance

Variance measures how far the observations are spread around the mean.

The basic idea is:

1. Find the mean.
2. Find each value's difference from the mean.
3. Square each difference.
4. Find the average of those squared differences.

For a population:

Variance = Sum of squared deviations / Number of observations

In notation:

σ² = Σ(xᵢ − μ)² / N

### Example

Data:

2, 4, 6

Mean:

(2 + 4 + 6) / 3 = 4

Differences from mean:

2 − 4 = −2

4 − 4 = 0

6 − 4 = 2

Square them:

4, 0, 4

Add:

4 + 0 + 4 = 8

Divide by 3:

8 / 3 = 2.67

Therefore:

**Population variance = 2.67**

### Why do we square?

Without squaring:

−2 + 0 + 2 = 0

The positive and negative deviations cancel each other.

Squaring makes all deviations positive.

---

## 7. Standard Deviation

Standard deviation tells us how much the data typically spreads around the mean.

### Formula

σ = √variance

For a population:

σ = √[Σ(xᵢ − μ)² / N]

Using the previous example:

Variance = 2.67

Standard deviation:

√2.67 ≈ 1.63

Therefore:

**Standard deviation ≈ 1.63**

### Important

Small standard deviation:

→ Values are close to the mean.

Large standard deviation:

→ Values are more spread out.

---

## 8. Variance vs Standard Deviation

| Measure            | What it tells us                          | Unit              |
| ------------------ | ----------------------------------------- | ----------------- |
| Variance           | Amount of spread using squared deviations | Squared units     |
| Standard deviation | Spread around the mean                    | Same unit as data |

Example:

If height is measured in centimeters:

* Variance → cm²
* Standard deviation → cm

Standard deviation is often easier to interpret because it uses the same unit as the original data.

---

## 9. Five-Number Summary

The five-number summary describes the distribution using five values:

1. Minimum
2. Q1
3. Median
4. Q3
5. Maximum

Example:

Data:

1, 2, 3, 4, 5, 6, 7, 8, 9

Five-number summary:

Minimum = 1

Q1 = 2.5

Median = 5

Q3 = 7.5

Maximum = 9

These five values are commonly used to construct a box plot.

---

## 10. Quartiles

Quartiles divide the ordered data into four parts.

### Q1

Q1 is the first quartile.

Approximately 25 percent of the data is below Q1.

### Q2

Q2 is the second quartile.

Q2 is the **median**.

Approximately 50 percent of the data is below Q2.

### Q3

Q3 is the third quartile.

Approximately 75 percent of the data is below Q3.

### Simple picture

Minimum → Q1 → Median → Q3 → Maximum

25% | 25% | 25% | 25%

---

## 11. Interquartile Range (IQR)

IQR measures the spread of the **middle 50 percent** of the data.

### Formula

IQR = Q3 − Q1

### Example

Suppose:

Q1 = 20

Q3 = 35

Then:

IQR = 35 − 20

IQR = 15

Therefore:

**IQR = 15**

### Important

IQR is resistant to extreme values.

That makes it useful when the data contains outliers.

---

## 12. Quartile Deviation

Quartile deviation is also called the **semi-interquartile range**.

### Formula

Quartile deviation = IQR / 2

or:

Quartile deviation = (Q3 − Q1) / 2

### Example

Q1 = 20

Q3 = 35

IQR = 35 − 20 = 15

Quartile deviation:

15 / 2 = 7.5

Therefore:

**Quartile deviation = 7.5**

---

## 13. Box Plot

A box plot visually represents the five-number summary.

It contains:

* Minimum
* Q1
* Median
* Q3
* Maximum

The box represents the middle 50 percent of the data.

The middle line inside the box represents the median.

The distance between Q1 and Q3 is the IQR.

### Structure

Minimum → Whisker → Q1 → Box → Median → Box → Q3 → Whisker → Maximum

---

## 14. Outliers

An outlier is a value that is unusually far from the rest of the data.

A common rule uses the IQR.

### Lower boundary

Lower fence = Q1 − 1.5 × IQR

### Upper boundary

Upper fence = Q3 + 1.5 × IQR

Values below the lower fence or above the upper fence are considered potential outliers.

### Example

Suppose:

Q1 = 10

Q3 = 20

First calculate IQR:

IQR = 20 − 10 = 10

Lower fence:

10 − 1.5 × 10 = −5

Upper fence:

20 + 1.5 × 10 = 35

Therefore:

Values below −5 or above 35 are potential outliers.

---

## 15. Symmetry

A distribution is symmetric when the left and right sides have approximately the same shape.

For a roughly symmetric distribution:

Mean ≈ Median

Example:

1, 2, 3, 4, 5

Mean = 3

Median = 3

The data is symmetric around 3.

---

## 16. Skewness

Skewness describes whether the distribution has a longer tail on one side.

There are two main types:

### Right-Skewed

The distribution has a longer tail toward the right.

Typically:

Mean > Median

Example:

2, 3, 4, 5, 20

The large value 20 pulls the mean to the right.

So:

Mean > Median

### Left-Skewed

The distribution has a longer tail toward the left.

Typically:

Mean < Median

The smaller extreme values pull the mean toward the left.

---

## 17. Symmetric vs Skewed

| Distribution | Typical relationship |
| ------------ | -------------------- |
| Symmetric    | Mean ≈ Median        |
| Right-skewed | Mean > Median        |
| Left-skewed  | Mean < Median        |

### Memory trick

The **mean gets pulled toward the tail**.

Right tail → mean moves right.

Left tail → mean moves left.

---

## 18. Choosing the Right Measure

| Situation                                 | Center | Spread             |
| ----------------------------------------- | ------ | ------------------ |
| Symmetric data without strong outliers    | Mean   | Standard deviation |
| Skewed data                               | Median | IQR                |
| Data with strong outliers                 | Median | IQR                |
| Most frequent category/value is important | Mode   | —                  |

### Example

If salaries are:

30k, 32k, 35k, 38k, 500k

The 500k salary is an extreme value.

The mean will be strongly affected.

So median and IQR are generally more representative of the typical observation and spread.

---

## 19. Complete Example

Consider this dataset:

2, 4, 4, 6, 8, 10

### Step 1: Mean

Mean:

(2 + 4 + 4 + 6 + 8 + 10) / 6

= 34 / 6

≈ 5.67

### Step 2: Median

There are 6 values.

The two middle values are 4 and 6.

Median:

(4 + 6) / 2 = 5

### Step 3: Mode

The value 4 occurs twice.

Mode = 4

### Step 4: Range

Range:

10 − 2 = 8

### Step 5: Five-number summary

Minimum = 2

Q1 = 4

Median = 5

Q3 = 8

Maximum = 10

### Step 6: IQR

IQR:

8 − 4 = 4

### Step 7: Quartile deviation

Quartile deviation:

4 / 2 = 2

---

## 20. Descriptive Statistics — Calculation Guide

| If you need to find... | What to do                                             |
| ---------------------- | ------------------------------------------------------ |
| Mean                   | Add all values and divide by the number of values      |
| Median                 | Sort the data and find the middle                      |
| Mode                   | Find the most frequent value                           |
| Range                  | Maximum − Minimum                                      |
| Variance               | Find squared deviations from the mean and average them |
| Standard deviation     | Take the square root of variance                       |
| Q1                     | Find the 25th percentile / lower quartile              |
| Q2                     | Find the median                                        |
| Q3                     | Find the 75th percentile / upper quartile              |
| IQR                    | Q3 − Q1                                                |
| Quartile deviation     | IQR / 2                                                |
| Lower outlier fence    | Q1 − 1.5 × IQR                                         |
| Upper outlier fence    | Q3 + 1.5 × IQR                                         |

---

## 21. Final Memory Map

**Center:**

Mean
Median
Mode

**Spread:**

Range
Variance
Standard deviation
IQR
Quartile deviation

**Position:**

Q1
Q2
Q3

**Five-number summary:**

Minimum → Q1 → Median → Q3 → Maximum

**Shape:**

Symmetric
Right-skewed
Left-skewed

**Outliers:**

Below Q1 − 1.5 × IQR

or

Above Q3 + 1.5 × IQR

### Most important relationships

Mean → sensitive to outliers

Median → resistant to outliers

Standard deviation → measures spread around the mean

IQR → measures spread of the middle 50 percent

Right skew → Mean > Median

Left skew → Mean < Median

Symmetric → Mean ≈ Median
