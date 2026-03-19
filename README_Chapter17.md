# Chapter 17: Analysis of Variance (Repeated Measures) — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 17 extends the **one-factor ANOVA** (Chapter 16) to **repeated-measures ANOVA**—when the **same subjects** are measured under all levels of the independent variable. By eliminating variability due to **individual differences**, the repeated-measures design yields a **more powerful** F test. The chapter covers the partitioning of variance (including **SSsubject** and **SSerror**), the F ratio, effect size (η²ₚ), **Tukey's HSD** for multiple comparisons, assumptions (including **sphericity**), and reporting.

---

## 17.1 Sleep Deprivation Experiment with Repeated Measures

### Design Change

- **One-factor ANOVA (Ch. 16):** Different subjects in each group (0, 24, 48 hours)
- **Repeated-measures ANOVA:** Same subjects experience all three levels

### Advantage: Eliminating Individual Differences

- **Individual differences** (personality, fitness, etc.) add variability to scores
- In repeated measures, each subject serves in all conditions → individual differences are **removed** from the error term
- **MSerror** becomes smaller → F tends to be larger → **more power** to detect effects

### Same Data, Different Results

- **Same 9 scores** used for both designs (for comparison)
- **One-factor:** F = 7.36, p < .05; only 0 vs. 48 hours significant
- **Repeated measures:** F = 27, p < .01; **all three** pairwise differences significant

### Table Layout

- Rows = subjects (A, B, C)
- Columns = levels of the factor (0, 24, 48 hours)
- Each cell = one score per subject per condition

---

## 17.2 F Test

### Hypotheses (Same as One-Factor)

- **H₀:** μ₀ = μ₂₄ = μ₄₈
- **H₁:** H₀ is false

### F Ratio

$$F = \frac{MS_{between}}{MS_{error}}$$

- **Numerator:** MSbetween (same as one-factor ANOVA)
- **Denominator:** **MSerror** (not MSwithin)—variability after removing individual differences

### Key Difference

- **MSerror** < **MSwithin** because SSsubject (individual differences) is removed from the error term
- Smaller denominator → larger F → more likely to reject H₀ when it is false

---

## 17.3 Two Complications

### 1. Carryover Effects

- Sufficient time must elapse between conditions to eliminate lingering effects
- If carryover is a concern → **do not use repeated measures**

### 2. Counterbalancing

- Randomly assign subjects to different **orders** of conditions
- Example: Subject A: 0→24→48; Subject B: 48→0→24; Subject C: 24→48→0
- Equalizes how often each level is experienced first, second, or third

---

## 17.4 Details: Variance Estimates

### Partitioning of Sum of Squares

**One-factor:** SStotal = SSbetween + SSwithin

**Repeated measures:** SSwithin is further partitioned:

$$SS_{total} = SS_{between} + SS_{subject} + SS_{error}$$

where SSwithin = SSsubject + SSerror

### New Terms

| Term | Definition |
|------|------------|
| **SSsubject** | Variability due to individual differences (subject means about grand mean) |
| **SSerror** | Remaining variability after removing individual differences |

### Computation Formulas

- **SSbetween:** Σ(T²/n) − G²/N (same as one-factor)
- **SSwithin:** ΣX² − Σ(T²/n) (same as one-factor)
- **SSsubject:** Σ(T_subject²/k) − G²/N
- **SSerror:** SSwithin − SSsubject

**Notation:** T_subject = total for each subject across all conditions; k = number of repeated measures (levels)

### Degrees of Freedom

| Term | Formula |
|------|---------|
| dftotal | N − 1 |
| dfbetween | k − 1 |
| dfwithin | N − k |
| dfsubject | n − 1 |
| dferror | dfwithin − dfsubject = (N − k) − (n − 1) |

**Check:** dftotal = dfbetween + dfsubject + dferror

---

## 17.5 Details: Mean Square and the F Ratio

### Formulas

$$MS_{between} = \frac{SS_{between}}{df_{between}}$$

$$MS_{error} = \frac{SS_{error}}{df_{error}}$$

$$F = \frac{MS_{between}}{MS_{error}}$$

### Sleep Deprivation Example

- MSbetween = 54/2 = 27 (same as one-factor)
- MSerror = 4/4 = **1** (vs. MSwithin = 3.67 in one-factor)
- F = 27/1 = **27**

### Why More Powerful?

- Individual differences are subtracted from **both** numerator and denominator
- The **denominator** (error) is typically smaller → shrinks more proportionally
- Result: F increases when H₀ is false

---

## 17.6 Table for the F Distribution

### Finding Critical F

- **Column:** dfbetween (numerator)
- **Row:** **dferror** (denominator)—not dfwithin

### Sleep Deprivation Example

- dfbetween = 2, dferror = 4 → critical F = 6.94 (α = .05), 18.00 (α = .01)
- Observed F = 27 > 18.00 → reject at .01 level

---

## 17.7 ANOVA Summary Tables

### Standard Format

| Source | SS | df | MS | F |
|--------|-----|-----|-----|-----|
| Between | | | MSbetween | F |
| Within | | | | |
| Subject | | | | |
| Error | | | MSerror | |
| Total | | | | |

### Comparison with One-Factor

- SS and df for Between and Total are the same
- Within is split into Subject and Error
- **Denominator of F** = MSerror (repeated) vs. MSwithin (one-factor)

---

## 17.8 Estimating Effect Size

### Partial η² (η²ₚ)

$$\eta^2_p = \frac{SS_{between}}{SS_{total} - SS_{subject}} = \frac{SS_{between}}{SS_{between} + SS_{error}}$$

- **Partial** because individual differences are excluded from the total variance
- Proportion of variance explained by the treatment **after** removing subject variability

### Guidelines (Same as η²)

| η²ₚ | Effect |
|-----|--------|
| .01 | Small |
| .09 | Medium |
| .25 | Large |

### Sleep Deprivation Example

- η²ₚ = 54 / (76 − 18) = 54/58 = **.93** (very large)

---

## 17.9 Multiple Comparisons

### Tukey's HSD (Repeated Measures)

$$HSD = q \sqrt{\frac{MS_{error}}{n}}$$

- **q** from Table G: use **k** (number of levels) and **dferror**
- **n** = number of subjects

### Sleep Deprivation Example

- q = 5.04, MSerror = 1, n = 3 → HSD = 2.87
- All three pairwise differences (3, 6, 3) exceed HSD → **all pairs significant**
- (One-factor HSD = 4.77 → only 0 vs. 48 significant)

### Cohen's d for Significant Pairs

$$d = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{MS_{error}}}$$

---

## 17.10 Reports in the Literature

### Example Format

> Mean aggression scores of 2, 5, and 8 were obtained when the same subjects were exposed to 0, 24, and 48 hours of sleep deprivation, respectively. There is evidence that aggression scores increase with hours of sleep deprivation [F(2, 4) = 27, MSE = 1.0, p < .01, η²ₚ = .93]. According to Tukey's HSD test, all pairs of differences were significant (HSD = 2.87, p < .05, 3 ≤ d ≤ 6).

---

## 17.11 Assumptions

### Usual ANOVA Assumptions

1. **Normality**
2. **Equal variances** (homogeneity of variance)

### Additional: Sphericity

- **Sphericity:** Equality of variances of **difference scores** between all pairs of conditions
- Equivalently: equality among all possible population correlations between conditions
- Violations can inflate F; usually not a major concern unless severe

### Remedies

- Increase sample size; use corrected degrees of freedom (e.g., Greenhouse-Geisser); consult advanced texts

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **Design** | Same subjects in all conditions |
| **Advantage** | Removes individual differences → smaller MSerror → more power |
| **SS partitioning** | SSwithin = SSsubject + SSerror |
| **F denominator** | MSerror (not MSwithin) |
| **Effect size** | η²ₚ = SSbetween / (SStotal − SSsubject) |
| **Tukey's HSD** | Use MSerror and dferror |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Repeated-measures ANOVA** | ANOVA with same subjects in all conditions |
| **Partial η² (η²ₚ)** | Proportion of variance explained (excluding subject variability) |
| **Sphericity** | Assumption that variances of difference scores between all pairs of conditions are equal; violations can inflate F. Software may report Mauchly's test or Greenhouse-Geisser correction |

---

## Key Equations

**Partitioning:**
- SStotal = SSbetween + SSsubject + SSerror
- SSwithin = SSsubject + SSerror

**Degrees of freedom:**
- dfsubject = n − 1
- dferror = dfwithin − dfsubject

**Mean squares:**
- MSbetween = SSbetween / dfbetween
- MSerror = SSerror / dferror

**F ratio:**
$$F = \frac{MS_{between}}{MS_{error}}$$

**Effect size:**
$$\eta^2_p = \frac{SS_{between}}{SS_{between} + SS_{error}}$$

**Tukey's HSD:**
$$HSD = q \sqrt{\frac{MS_{error}}{n}}$$

**Cohen's d:**
$$d = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{MS_{error}}}$$

---

## Quick Reference: One-Factor vs. Repeated Measures

| | One-Factor | Repeated Measures |
|---|------------|-------------------|
| **Subjects** | Different per group | Same in all groups |
| **Error term** | MSwithin | MSerror |
| **SS partitioning** | SSwithin | SSsubject + SSerror |
| **Power** | Lower | Higher (typically) |

---

## Next Chapter

**Chapter 18: Analysis of Variance (Two Factors)** — ANOVA with two independent variables and interaction.

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
