# Chapter 20: Tests for Ranked (Ordinal) Data — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 20 describes **nonparametric** (or **distribution-free**) tests for **ranked (ordinal) data** or when parametric assumptions (normality, equal variances) are violated. The chapter covers three tests: **Mann-Whitney U** (two independent samples), **Wilcoxon T** (two related samples), and **Kruskal-Wallis H** (three or more independent samples). These are alternatives to the t and F tests when data are ordinal or when normality/equal variance assumptions cannot be met.

---

## 20.1 Use Only When Appropriate

### When to Use U, T, or H Tests

1. **Original data are ranked (ordinal)** — e.g., rankings from 1 to n
2. **Quantitative data violate assumptions** — populations not normal and/or variances unequal, especially when:
   - Sample sizes are **small** (< ~10)
   - Sample sizes are **small and unequal** (unequal variances)

### When to Use t and F Tests Instead

- When data are **quantitative** and populations appear **normal** with **equal variances**
- **t and F tests are more powerful** — more likely to detect a false H₀ when assumptions hold

---

## 20.2 A Note on Terminology

### Nonparametric Tests

- **Parameter** = descriptive measure of a population (e.g., mean)
- **Nonparametric tests** (U, T, H, χ²) evaluate hypotheses about **entire population distributions**, not specific parameters

### Distribution-Free Tests

- Make **no assumptions** about the form of the population distribution
- Contrast with t and F tests, which assume normality and equal variances

### Caveat

- If we assume similar variabilities and shapes, we sacrifice "distribution-free" status for more precise conclusions about central tendency (e.g., medians)

---

## 20.3 Mann-Whitney U Test (Two Independent Samples)

### When to Use

- **Two independent groups**
- Data are **ranked** or quantitative data violate normality/equal variance assumptions

### Statistical Hypotheses

- **H₀:** Population distribution 1 = Population distribution 2
- **H₁:** Population distribution 1 ≠ Population distribution 2

### Interpretation

- **Strict:** Rejection of H₀ means the two populations differ in some unspecified way (central tendency, variability, shape, or combination)
- **If** we assume similar variabilities and shapes → rejection implies different **central tendencies** (medians)

### Procedure

1. **Rank** all observations from both groups combined (1 = smallest)
2. **Handle ties:** Assign median of ranks that would have been used
3. **Sum ranks** for each group: R₁, R₂
4. **Computational check:** R₁ + R₂ = n(n + 1)/2
5. **Calculate U₁ and U₂:**
   - U₁ = n₁n₂ + [n₁(n₁ + 1)/2] − R₁
   - U₂ = n₁n₂ + [n₂(n₂ + 1)/2] − R₂
6. **U** = smaller of U₁ or U₂

### Decision Rule

- **Reject H₀** if observed U **≤** critical U
- **Retain H₀** if observed U **>** critical U

*Note: Unlike t and F, smaller U → more likely to reject*

### Critical Values

- Table E (Appendix C): use n₁ and n₂
- Separate tables for directional and nondirectional tests

### TV Viewing Example

- n₁ = 8, n₂ = 7; U = 20; critical U = 10
- U = 20 > 10 → **retain H₀**

---

## 20.4 Wilcoxon T Test (Two Related Samples)

### When to Use

- **Two related groups** (repeated measures or matched pairs)
- Data are **ranked** or difference scores violate normality

### Statistical Hypotheses

- **H₀:** Population distribution 1 = Population distribution 2
- **H₁:** Population distribution 1 ≠ Population distribution 2

### Procedure

1. **Difference scores:** D = X₁ − X₂ for each pair
2. **Ignore zeros;** rank absolute values from smallest to largest
3. **Handle ties:** Assign median rank
4. **Separate ranks** into plus (positive D) and minus (negative D)
5. **Sum:** R+ = sum of ranks for positive D; R− = sum of ranks for negative D
6. **Computational check:** R+ + R− = n(n + 1)/2 (n = number of nonzero differences)
7. **T** = smaller of R+ or R−

### Decision Rule

- **Reject H₀** if observed T **≤** critical T
- **Retain H₀** if observed T **>** critical T

### Critical Values

- Table F (Appendix C): use n (number of nonzero difference scores)

### TV Viewing (Matched Pairs) Example

- n = 7; T = 1.5; critical T = 2
- T = 1.5 ≤ 2 → **reject H₀**

---

## 20.5 Kruskal-Wallis H Test (Three or More Independent Samples)

### When to Use

- **Three or more independent groups**
- Data are **ranked** or quantitative data violate ANOVA assumptions

### Statistical Hypotheses

- **H₀:** All population distributions are equal
- **H₁:** H₀ is false (at least one population differs)

### Procedure

1. **Rank** all observations from all groups combined (1 = smallest)
2. **Handle ties:** Assign median rank
3. **Sum ranks** for each group: R₁, R₂, R₃, ...
4. **Computational check:** ΣRᵢ = n(n + 1)/2
5. **Calculate H:**

$$H = \frac{12}{n(n+1)} \left[ \frac{R_1^2}{n_1} + \frac{R_2^2}{n_2} + \frac{R_3^2}{n_3} + \cdots \right] - 3(n + 1)$$

### Degrees of Freedom

$$df = \text{number of groups} - 1$$

### Critical Values

- Use **χ² table** (Table D) with df = k − 1
- Requires each group to have at least ~4 observations

### Decision Rule

- **Reject H₀** if observed H **≥** critical χ²
- **Retain H₀** if observed H **<** critical χ²

*Note: Unlike U and T, larger H → more likely to reject*

### TV Cartoon Example

- 3 groups, n = 15; H = 0.11; critical χ² = 5.99 (df = 2)
- H = 0.11 < 5.99 → **retain H₀**

---

## 20.6 General Comment: Ties

### Assumption

- Underlying distributions are **continuous** → no two values should be exactly equal
- In practice, **ties** occur (e.g., two observations of 5)

### Handling Ties

- Assign **median rank** to tied values (e.g., two values that would be ranks 4 and 5 both get 4.5)
- **Many ties** + test result near but not reaching significance → consider a tie-corrected formula (see advanced texts)

---

## Summary: Test Selection

| Design | Parametric Test | Nonparametric Alternative |
|--------|----------------|---------------------------|
| Two independent samples | t test (Ch. 14) | **Mann-Whitney U** |
| Two related samples | t test (Ch. 15) | **Wilcoxon T** |
| Three+ independent samples | One-factor F (Ch. 16) | **Kruskal-Wallis H** |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Nonparametric tests** | Evaluate entire distributions; not specific parameters |
| **Distribution-free tests** | No assumptions about population distribution form |
| **Mann-Whitney U test** | Ranked data; two independent samples |
| **Wilcoxon T test** | Ranked data; two related samples |
| **Kruskal-Wallis H test** | Ranked data; three or more independent samples |

---

## Key Equations

**Mann-Whitney U:**
$$U_1 = n_1 n_2 + \frac{n_1(n_1+1)}{2} - R_1$$
$$U_2 = n_1 n_2 + \frac{n_2(n_2+1)}{2} - R_2$$
$$U = \text{smaller of } U_1 \text{ or } U_2$$

**Wilcoxon T:**
$$T = \text{smaller of } R_+ \text{ or } R_-$$

**Kruskal-Wallis H:**
$$H = \frac{12}{n(n+1)} \Sigma \frac{R_i^2}{n_i} - 3(n+1)$$

---

## Quick Reference: Decision Rules

| Test | Reject H₀ when |
|------|----------------|
| **U** | Observed U ≤ critical U |
| **T** | Observed T ≤ critical T |
| **H** | Observed H ≥ critical χ² |

---

## Next Chapter

**Chapter 21: Postscript: Which Test?** — Flow chart and guidelines for selecting the appropriate statistical test.

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
