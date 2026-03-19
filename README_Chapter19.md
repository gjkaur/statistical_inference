# Chapter 19: Chi-Square (χ²) Test for Qualitative (Nominal) Data — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 19 introduces the **chi-square (χ²) test** for **qualitative (nominal) data**—when observations are classified into categories and analyzed as **frequencies**. The chapter covers two tests: (1) **one-variable χ²** (goodness-of-fit)—testing whether observed frequencies match hypothesized proportions; and (2) **two-variable χ²** (test of independence)—testing whether two qualitative variables are related. Also covered: expected frequencies, degrees of freedom, **Cramer's phi** (φ²c) for effect size, **odds ratios**, and precautions.

---

## ONE-VARIABLE χ² TEST

## 19.1 Survey of Blood Types

### Context

- **Claim:** Blood types in U.S. population: O (.44), A (.41), B (.10), AB (.05)
- **Sample:** 100 students; observed frequencies: O=38, A=38, B=20, AB=4
- **Question:** Does the sample distribution match the claimed proportions?

### Qualitative (Nominal) Data

- Data are **categorical** (blood type, political affiliation, etc.)
- No numeric scale; categories are labels only
- **χ² test** is the appropriate hypothesis test for frequency data

### One-Variable vs. Two-Variable

| Test | Classification | Purpose |
|------|----------------|---------|
| **One-variable χ²** | Single variable | Goodness-of-fit: Do observed frequencies match expected? |
| **Two-variable χ²** | Two variables (cross-classified) | Test of independence: Are the two variables related? |

---

## 19.2 Statistical Hypotheses (One-Variable)

### Null Hypothesis

- Specifies **hypothesized proportions** for each category
- Example: H₀: P_O = .44, P_A = .41, P_B = .10, P_AB = .05
- Proportions must sum to 1.00

### Alternative Hypothesis

- H₁: H₀ is false (proportions differ from hypothesized in some way)

---

## 19.3 Details: Calculating χ² (One-Variable)

### Expected Frequency

$$f_e = (\text{expected proportion})(\text{total sample size})$$

- Example: f_e(O) = (.44)(100) = 44

### Observed vs. Expected

- **f_o** = observed frequency (actual count in sample)
- **f_e** = expected frequency (if H₀ is true)

### χ² Formula

$$\chi^2 = \Sigma \frac{(f_o - f_e)^2}{f_e}$$

- Sum over all categories
- Larger discrepancies → larger χ² → more likely to reject H₀
- Squaring makes all contributions positive; division by f_e weights by expected size

### Blood Type Example

- χ² = (38−44)²/44 + (38−41)²/41 + (20−10)²/10 + (4−5)²/5 = **11.24**

---

## 19.4 Table for the χ² Distribution (One-Variable)

### Degrees of Freedom

$$df = c - 1$$

where c = number of categories.

- One df is lost because frequencies must sum to the total sample size.

### Finding Critical χ²

- Use Table D (Appendix C): row = df, column = α
- Blood types: df = 3, α = .05 → critical χ² = **7.81**

---

## 19.5 χ² Test (One-Variable)

### Decision Rule

- **Reject H₀** if observed χ² ≥ critical χ²
- **Retain H₀** if observed χ² < critical χ²

### Blood Type Example

- Observed χ² = 11.24 > 7.81 → **reject H₀**
- Interpretation: Distribution of blood types in the student population differs from the U.S. claim.

### Nondirectional

- χ² is always nondirectional (all discrepancies squared → rejection region in upper tail only)

---

## TWO-VARIABLE χ² TEST

## 19.6 Lost Letter Study

### Context

- **Factor 1:** Type of neighborhood (downtown, suburbia, campus)
- **Factor 2:** Letter returned (yes/no)
- **Design:** 200 letters "lost"; cross-classified by neighborhood and return status

### Cross-Classification Table

| | Downtown | Suburbia | Campus | Total |
|---|-----------|----------|--------|-------|
| **Yes** | 39 | 30 | 51 | 120 |
| **No** | 21 | 40 | 19 | 80 |
| **Total** | 60 | 70 | 70 | 200 |

---

## 19.7 Statistical Hypotheses (Two-Variable)

### Null Hypothesis

- **H₀:** The two variables are **independent** (no relationship)
- No predictability: knowing one variable does not help predict the other
- Example: H₀: Type of neighborhood and return rate are independent

### Alternative Hypothesis

- H₁: H₀ is false (the two variables are related)

---

## 19.8 Details: Calculating χ² (Two-Variable)

### Expected Frequency (Two-Variable)

$$f_e = \frac{(\text{row total})(\text{column total})}{\text{grand total}}$$

- Example: f_e(yes, downtown) = (120)(60)/200 = **36**

### Logic

- If H₀ is true, the proportion in each row should be the same across columns
- Expected frequency = (row proportion) × (column total) = (row total/grand total) × (column total)

### χ² Formula (Same as One-Variable)

$$\chi^2 = \Sigma \frac{(f_o - f_e)^2}{f_e}$$

- Sum over **all cells** in the table

### Lost Letter Example

- χ² = **14.02**

---

## 19.9 Table for the χ² Distribution (Two-Variable)

### Degrees of Freedom

$$df = (c - 1)(r - 1)$$

where c = number of columns, r = number of rows.

- Lost letter: df = (3−1)(2−1) = **2**

### Critical χ²

- df = 2, α = .05 → critical χ² = **5.99**

---

## 19.10 χ² Test (Two-Variable)

### Lost Letter Example

- Observed χ² = 14.02 > 5.99 → **reject H₀**
- Interpretation: Type of neighborhood and return rate are **not** independent; neighborhood predicts return rate.

---

## 19.11 Estimating Effect Size

### Squared Cramer's Phi (φ²c)

$$\phi^2_c = \frac{\chi^2}{n(k - 1)}$$

where:
- **n** = total sample size
- **k** = smaller of (number of rows, number of columns)

### Interpretation

- Rough estimate of proportion of variance explained (predictability) between the two variables
- Independent of sample size (unlike χ²)

### Guidelines (Cohen)

| φ²c | Effect |
|-----|--------|
| .01 | Small |
| .09 | Medium |
| .25 | Large |

### Lost Letter Example

- φ²c = 14.02 / [200(2−1)] = **.07** (medium)

---

## 19.12 Odds Ratios

### When to Use

- Especially for **2×2 tables**
- Helps interpret importance when φ²c is small but χ² is significant

### Calculating Odds Ratio

1. **Odds** = (frequency of occurrence) / (frequency of nonoccurrence) for each group
2. **Odds ratio** = Odds in Group A / Odds in Group B

### Aspirin/Heart Attack Example

- Placebo: odds = 189/10,845 = .0174
- Aspirin: odds = 104/10,933 = .0095
- **OR** = .0174/.0095 = **1.83**
- Interpretation: Placebo group is 1.83 times more likely to have a heart attack than aspirin group

---

## 19.13 Reports in the Literature

### Example Format

> There is evidence that the return rate of lost letters is related to the type of neighborhood [χ²(2, n = 200) = 14.02, p < .001, φ²c = .07].

---

## 19.14 Some Precautions

### 1. Independent Observations

- Each observation must be **independent**
- One subject should not contribute more than one observation (or one cell count)
- Total observed frequencies should not exceed total number of subjects

### 2. Expected Frequencies

- **All expected frequencies should be ≥ 5** (conservative rule)
- If some are too small, combine categories or increase sample size

### 3. Sample Size

- **Too small:** Low power; may miss real effects
- **Too large:** May detect trivial departures from H₀
- Use power analysis to guide sample size when possible

---

## 19.15 Computer Output

- Software (SAS, SPSS, Minitab) provides χ², df, p-value
- May report **Cramer's V** (φc); **φ²c = V²** for effect size
- **Likelihood ratio chi-square** is an alternative to Pearson χ²

---

## Summary

| Test | H₀ | df | Expected Frequency |
|------|-----|-----|---------------------|
| **One-variable** | Specified proportions | c − 1 | (proportion)(n) |
| **Two-variable** | Independence | (c−1)(r−1) | (row total)(column total)/grand total |

---

## Important Terms

| Term | Definition |
|------|------------|
| **One-variable χ² test** | Goodness-of-fit: observed vs. expected frequencies for one variable |
| **Two-variable χ² test** | Test of independence: are two variables related? |
| **Expected frequency (f_e)** | Frequency expected if H₀ is true |
| **Observed frequency (f_o)** | Actual frequency in the sample |
| **φ²c (Cramer's phi squared)** | Effect size for two-variable χ² |
| **Odds ratio** | Relative occurrence across two groups |

---

## Key Equations

**χ² ratio:**
$$\chi^2 = \Sigma \frac{(f_o - f_e)^2}{f_e}$$

**Expected frequency (one-variable):**
$$f_e = (\text{expected proportion})(\text{total sample size})$$

**Expected frequency (two-variable):**
$$f_e = \frac{(\text{row total})(\text{column total})}{\text{grand total}}$$

**Degrees of freedom:**
- One-variable: df = c − 1
- Two-variable: df = (c − 1)(r − 1)

**Effect size (two-variable):**
$$\phi^2_c = \frac{\chi^2}{n(k - 1)}$$

---

## Quick Reference

| Situation | Test |
|----------|------|
| One variable, test specified proportions | One-variable χ² |
| Two variables, test relationship/independence | Two-variable χ² |

---

## Next Chapter

**Chapter 20: Tests for Ranked (Ordinal) Data** — Mann-Whitney U, Wilcoxon T, and Kruskal-Wallis H tests for when data are ranked or parametric assumptions (normality, equal variances) are violated.

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
