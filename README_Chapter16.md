# Chapter 16: Analysis of Variance (One Factor) — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 16 introduces **Analysis of Variance (ANOVA)**—a procedure for testing whether **two or more population means** differ. The **one-factor** (or **one-way**) ANOVA tests differences among groups defined by a single independent variable, with different subjects in each group. The chapter covers the **F test**, variance estimates (sums of squares, mean squares), the F distribution table, **effect size (η²)**, **Tukey's HSD** for multiple comparisons, assumptions, and reporting.

---

## 16.1 Testing a Hypothesis About Sleep Deprivation and Aggression

### Research Design

- **Independent variable (factor):** Hours of sleep deprivation (0, 24, 48)
- **Dependent variable:** Aggression score in a controlled social situation
- **Design:** Random assignment; 3 subjects per group (n = 3)

### Statistical Hypotheses

- **$H_0$:** μ₀ = μ₂₄ = μ₄₈ (all population means equal)
- **$H_1$:** $H_0$ is false (at least one mean differs)

### Why Not t Tests?

- **t test** is for comparing **two** means.
- With **three or more** groups, multiple t tests inflate the **Type I error** rate.
- **ANOVA** provides one overall test of the null hypothesis.

### One-Factor ANOVA

- **One factor:** One independent variable (e.g., sleep deprivation)
- **Different subjects** in each group (independent samples)
- Chapter 17: Repeated measures (same subjects)
- Chapter 18: Two factors

---

## 16.2 Two Sources of Variability

### Variability Between Groups

- Variation among scores of subjects in **different** groups (different treatments)
- Reflects **random error** + **treatment effect** (if $H_0$ is false)

### Variability Within Groups

- Variation among scores of subjects in the **same** group (same treatment)
- Reflects **random error only** (individual differences, measurement error, etc.)
- Also called the **error term**; analogous to pooled variance in the t test

### The Logic

- **If $H_0$ true:** Between-group and within-group variability both reflect random error → F ≈ 1
- **If $H_0$ false:** Between-group variability also reflects treatment effect → F > 1

### Treatment Effect

- Existence of at least one difference between population means

---

## 16.3 F Test

### F Ratio

$$F = \frac{\text{variability between groups}}{\text{variability within groups}} = \frac{MS_{between}}{MS_{within}}$$

### Interpretation

| $H_0$ Status | Numerator | Denominator | F |
|----------|-----------|-------------|---|
| **True** | Random error | Random error | ≈ 1 |
| **False** | Random error + treatment effect | Random error | > 1 |

### Decision Rule

- **Reject $H_0$** if observed F ≥ critical F
- **Retain $H_0$** if observed F < critical F

### Sleep Deprivation Example

- **Outcome A:** F = 0.75 → retain $H_0$ (small mean differences)
- **Outcome B:** F = 7.36 → reject $H_0$ (large mean differences)

---

## 16.4 Details: Variance Estimates

### Mean Square (MS)

$$MS = \frac{SS}{df}$$

- **SS** = sum of squared deviations about a mean
- **df** = degrees of freedom

### Sums of Squares

| Term | Definition | Formula (computation) |
|------|------------|------------------------|
| **SSbetween** | SS of group means about grand mean | Σ(T²/n) − G²/N |
| **SSwithin** | SS of scores about their group means | ΣX² − Σ(T²/n) |
| **SStotal** | SS of all scores about grand mean | ΣX² − G²/N |

**Check:** SStotal = SSbetween + SSwithin

### Degrees of Freedom

| Term | Formula |
|------|---------|
| dftotal | N − 1 |
| dfbetween | k − 1 |
| dfwithin | N − k |

**Check:** dftotal = dfbetween + dfwithin

**Notation:** N = total number of scores; k = number of groups; T = group total; G = grand total

---

## 16.5 Details: Mean Squares and the F Ratio

### Formulas

$$MS_{between} = \frac{SS_{between}}{df_{between}}$$

$$MS_{within} = \frac{SS_{within}}{df_{within}}$$

$$F = \frac{MS_{between}}{MS_{within}}$$

### Sleep Deprivation (Outcome B)

- SSbetween = 54, dfbetween = 2 → MSbetween = 27
- SSwithin = 22, dfwithin = 6 → MSwithin = 3.67
- F = 27 / 3.67 = **7.36**

---

## 16.6 Table for the F Distribution

### Finding Critical F

- **Column:** df for numerator (dfbetween)
- **Row:** df for denominator (dfwithin)
- **Cell:** Critical F for α = .05 or .01

### Sleep Deprivation Example

- dfbetween = 2, dfwithin = 6 → critical F = 5.14 (α = .05)
- Observed F = 7.36 > 5.14 → **reject $H_0$**

### Approximate p-Values

- F < light numbers → p > .05
- F between light and dark → p < .05
- F > dark numbers → p < .01

---

## 16.7 ANOVA Summary Tables

### Standard Format

| Source | SS | df | MS | F |
|--------|-----|-----|-----|-----|
| Between | | | MSbetween | F |
| Within | | | MSwithin | |
| Total | | | | |

- Alternative labels: "Treatment" for Between, "Error" for Within

---

## 16.8 F Test Is Nondirectional

- Rejection region is only in the **upper tail** of the F distribution
- All differences are **squared** → positive values only
- F is **nondirectional** (equivalent to two-tailed test)
- **For two groups:** F = t²

---

## 16.9 Estimating Effect Size

### η² (Eta-Squared)

$$\eta^2 = \frac{SS_{between}}{SS_{total}}$$

- **Proportion of variance explained** by the independent variable (0 to 1)
- Independent of sample size

### Interpretation

| η² | Meaning |
|-----|---------|
| 0 | No effect (all variance within groups) |
| 1 | Maximum effect (all variance between groups) |
| .01 | Small effect |
| .09 | Medium effect |
| .25 | Large effect |

### Sleep Deprivation Example

- η² = 54 / 76 = **.71** (very large)

---

## 16.10 Multiple Comparisons

### Why Not Multiple t Tests?

- Multiple t tests inflate the **cumulative Type I error** (e.g., 3 tests at α = .05 → up to ~.15)

### Tukey's HSD Test

- **H**onestly **S**ignificant **D**ifference
- Controls overall Type I error for all pairwise comparisons
- Use **only after** a significant F test

### Formula

$$HSD = q \sqrt{\frac{MS_{within}}{n}}$$

- **q** = Studentized Range Statistic (Table G in Appendix C)
- **k** = number of groups; **dfwithin** = degrees of freedom

### Interpretation

- If |X̄ᵢ − X̄ⱼ| ≥ HSD → reject $H_0$ for that pair
- Sleep deprivation: HSD = 4.77; only 0 vs. 48 hours (difference = 6) is significant

### Cohen's d for Significant Pairs

$$d = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{MS_{within}}}$$

### Other Multiple Comparison Tests

- **Scheffe:** More conservative (fewer Type I errors, more Type II)
- **LSD (protected t):** More liberal

---

## 16.11 Overview: Flow Chart for ANOVA

1. **F test** → Significant? → No → Stop
2. **F test** → Significant? → Yes → **Estimate η²**
3. **Tukey's HSD** → Identify significant pairs
4. **Cohen's d** for each significant pair

---

## 16.12 Reports in the Literature

### Example Format

> Aggression scores for subjects deprived of sleep for 0 hours (X̄ = 2, s = 2.00), 24 hours (X̄ = 5, s = 1.73), and 48 hours (X̄ = 8, s = 2.00) differ significantly [F(2, 6) = 7.36; MSE = 3.67; p < .05; η² = .71]. According to Tukey's HSD test, only the difference between 0 and 48 hours is significant (HSD = 4.77, p < .05, d = 3.13).

---

## 16.13 Assumptions

1. **Normality:** Populations are normally distributed
2. **Equal variances:** Homogeneity of variance across groups

### Robustness

- Violations matter most when sample sizes are **small** and **unequal**
- If n ≥ ~10 per group and equal, usually tolerable

### Alternatives

- Increase n; equalize n; use unequal-variance F; or use Kruskal-Wallis H (Chapter 20)

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **ANOVA** | Tests $H_0$: all population means equal |
| **F ratio** | MSbetween / MSwithin |
| **If $H_0$ true** | F ≈ 1 |
| **If $H_0$ false** | F > 1 |
| **Effect size** | η² = SSbetween / SStotal |
| **Multiple comparisons** | Tukey's HSD (after significant F) |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Analysis of variance (ANOVA)** | Overall test for two or more population means |
| **One-factor ANOVA** | One independent variable, different subjects per group |
| **Treatment effect** | At least one difference between population means |
| **Variability between groups** | Variation among subjects in different groups |
| **Variability within groups** | Variation among subjects in same group (error) |
| **Random error** | Combined effects of uncontrolled factors |
| **F ratio** | MSbetween / MSwithin |
| **Mean square (MS)** | SS / df |
| **Sum of squares (SS)** | Sum of squared deviations about a mean |
| **η² (eta-squared)** | Proportion of variance explained by group membership |
| **Multiple comparisons** | Tests for pairwise mean differences |
| **Tukey's HSD** | Multiple comparison test controlling Type I error |

---

## Key Equations

**Sums of squares:**
- SSbetween = Σ(T²/n) − G²/N
- SSwithin = ΣX² − Σ(T²/n)
- SStotal = ΣX² − G²/N
- SStotal = SSbetween + SSwithin

**Degrees of freedom:**
- dftotal = N − 1
- dfbetween = k − 1
- dfwithin = N − k

**Mean squares:**
- MSbetween = SSbetween / dfbetween
- MSwithin = SSwithin / dfwithin

**F ratio:**
$$F = \frac{MS_{between}}{MS_{within}}$$

**Effect size:**
$$\eta^2 = \frac{SS_{between}}{SS_{total}}$$

**Tukey's HSD:**
$$HSD = q \sqrt{\frac{MS_{within}}{n}}$$

**Cohen's d (for significant pairs):**
$$d = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{MS_{within}}}$$

---

## Next Chapter

**Chapter 17: Analysis of Variance (Repeated Measures)** — One-factor ANOVA when the same subjects are measured under each condition.

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
