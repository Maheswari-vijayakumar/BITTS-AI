# Probability — Complete Notes

| # | Concept | Meaning | Formula | Example / Calculation |
|---|---|---|---|---|
| 1 | Random Experiment | An experiment whose exact result is uncertain | — | Roll a die → possible results: 1, 2, 3, 4, 5, 6 |
| 2 | Sample Space (S) | All possible outcomes | S = {all possible outcomes} | Two coin tosses → S = {HH, HT, TH, TT} |
| 3 | Event (A) | One or more outcomes we are interested in | A is a subset of S | Even on a die → A = {2, 4, 6} |
| 4 | Probability | How likely an event is | 0 ≤ P(A) ≤ 1 | Even on a die → P(A) = 3/6 = 1/2 |
| 5 | Equally Likely Probability | Favorable outcomes divided by total outcomes | P(A) = favorable outcomes / total outcomes | Getting 5 → P(5) = 1/6 |
| 6 | Empirical Probability | Probability based on actual observations | P(A) = occurrences / trials | 110 Heads in 200 tosses → 110/200 = 0.55 |
| 7 | Complement (Aᶜ) | Everything that is not A | P(Aᶜ) = 1 − P(A) | P(even) = 1/2 → P(odd) = 1 − 1/2 = 1/2 |
| 8 | Intersection (A ∩ B) | A AND B — common outcomes | A ∩ B | A = {1, 2, 3}, B = {3, 4, 5} → A ∩ B = {3} |
| 9 | Union (A ∪ B) | A OR B — all outcomes from A and B | A ∪ B | A = {1, 2}, B = {2, 3} → A ∪ B = {1, 2, 3} |
| 10 | Mutually Exclusive | A and B cannot happen together | A ∩ B = ∅ | Even vs odd → no common outcome |
| 11 | Mutually Exclusive OR | OR when there is no overlap | P(A ∪ B) = P(A) + P(B) | P(A) = 2/6, P(B) = 2/6 → 4/6 = 2/3 |
| 12 | OR with Overlap | A and B can happen together | P(A ∪ B) = P(A) + P(B) − P(A ∩ B) | 3/6 + 3/6 − 2/6 = 4/6 = 2/3 |
| 13 | Independent Events | A does not affect B | P(A ∩ B) = P(A) × P(B) | Two coin tosses → 1/2 × 1/2 = 1/4 |
| 14 | Dependent Events | A affects B | P(A ∩ B) = P(A) × P(B given A) | 3 red, 2 blue; red twice without replacement → 3/5 × 2/4 = 3/10 |
| 15 | Conditional Probability | Probability of B given that A happened | P(B given A) = P(A ∩ B) / P(A) | If P(A ∩ B) = 0.2 and P(A) = 0.5 → 0.2/0.5 = 0.4 |
| 16 | Axiomatic Rule 1 | Probability cannot be negative | P(A) ≥ 0 | P(A) = −0.2 → impossible |
| 17 | Axiomatic Rule 2 | Entire sample space is certain | P(S) = 1 | A die must produce 1–6 → P(S) = 1 |
| 18 | Axiomatic Rule 3 | Add probabilities of mutually exclusive events | P(A ∪ B) = P(A) + P(B) | 0.3 + 0.4 = 0.7 |

## Most Important Calculation Guide

| Question says | Think | Formula |
|---|---|---|
| A AND B, independent | Both happen and neither affects the other | P(A ∩ B) = P(A) × P(B) |
| A AND B, dependent | Both happen and the first affects the second | P(A ∩ B) = P(A) × P(B given A) |
| A OR B, no common outcome | Mutually exclusive | P(A ∪ B) = P(A) + P(B) |
| A OR B, common outcome exists | There is overlap | P(A ∪ B) = P(A) + P(B) − P(A ∩ B) |
| NOT A | Complement | P(Aᶜ) = 1 − P(A) |

## Key Distinction

### Mutually Exclusive

Ask:

> Can A and B happen together?

If **NO** → mutually exclusive.

A ∩ B = ∅

### Independent

Ask:

> Does A affect B?

If **NO** → independent.

P(A ∩ B) = P(A) × P(B)

## Easy Memory Rules

- **AND → usually multiply**
- **OR → usually add**
- **OR with overlap → add − overlap**
- **NOT → 1 − probability**
- **Independent → one does not affect the other**
- **Dependent → one affects the other**
- **Mutually exclusive → cannot happen together**
