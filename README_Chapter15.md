# Chapter 15: t Test for Two Related Samples (Repeated Measures) — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 15 describes the **t test for two related samples**—comparing means when each observation in one sample is **paired** with an observation in the other. The most common case is **repeated measures**: the same subjects are measured twice (e.g., before and after treatment). The chapter covers **difference scores**, the sampling distribution of D̄, the t ratio, calculations, effect size (confidence intervals and Cohen's d), assumptions, an overview of the three t tests, and the **t test for the population correlation coefficient (ρ)**.

---

## 15.1 EPO Experiment with Repeated Measures

### Controlling Individual Differences

- **Individual differences** (attitude, fitness, personality, etc.) add variability to scores and make it harder to detect treatment effects.
- **Repeated measures:** Each subject is measured **twice**—once under treatment, once under control.
- By focusing on **difference scores** (D = X₁ − X₂), we eliminate each subject's unique contribution to both scores.
- Result: **Smaller standard error** → more sensitive test → higher power to detect effects.

### Difference Scores

$$D = X_1 - X_2$$

- **D** = difference between paired scores for each subject
- Converts a two-sample problem into a **one-sample** problem (one sample of D values)

### Mean Difference Score

$$\bar{D} = \frac{\Sigma D}{n}$$

- The sign of D̄ matters: positive → treatment > control; negative → treatment < control

### Comparing the Two EPO Experiments

- **Same data** (X₁ and X₂) used for both independent-samples and repeated-measures designs
- **Independent samples:** Range of X₁ and X₂ = 15; standard error larger
- **Repeated measures:** Range of D = 5; standard error much smaller
- With repeated measures: t = 7.35, p < .001 (vs. t = 2.16, p < .05 for independent samples)

### Two Related Samples

- **Two related samples:** Each observation in one sample is paired one-to-one with an observation in the other.
- **Repeated measures:** Same subjects measured twice (most common).
- **Matched pairs:** Different subjects matched on a relevant variable (e.g., body weight).

### Complications with Repeated Measures

1. **Carryover effects:** Sufficient time must pass between conditions to eliminate lingering treatment effects.
2. **Counterbalancing:** Randomly assign half the subjects to order A→B, half to B→A, to control for **sequence effects**.

---

## 15.2 Statistical Hypotheses

### Null and Alternative Hypotheses

| Test Type | $H_0$ | $H_1$ |
|-----------|-----|-----|
| **Upper tail (EPO example)** | μD ≤ 0 | μD > 0 |
| **Lower tail** | μD ≥ 0 | μD < 0 |
| **Two-tailed** | μD = 0 | μD ≠ 0 |

- **μD** = population mean of all difference scores

---

## 15.3 Sampling Distribution of D̄

### Properties

- **Mean:** μD̄ = μD (mean of sampling distribution = population mean of difference scores)
- **Standard error:** $\sigma_{\bar{D}} = \sigma_D / \sqrt{n}$ (analogous to $\sigma_{\bar{X}} = \sigma / \sqrt{n}$ for a single sample)

---

## 15.4 t Test

### t Ratio

$$t = \frac{\bar{D} - \mu_{D,hyp}}{s_{\bar{D}}}$$

where:
- **D̄** = sample mean of difference scores
- **μD,hyp** = hypothesized population mean (typically 0)
- **sD̄** = estimated standard error of D̄

### Degrees of Freedom

$$df = n - 1$$

where n = number of **pairs** (difference scores).

### EPO Example

- D̄ = 5, sD̄ = 0.68, μD,hyp = 0
- t = (5 − 0) / 0.68 = **7.35**
- Critical t = 2.015 (df = 5, one-tailed, α = .05)
- **Decision:** Reject $H_0$
- **Interpretation:** EPO increases mean endurance when patients are measured twice.

---

## 15.5 Details: Calculations for the t Test

### Three Panels (Table 15.2)

**Panel I — Mean and standard deviation of D:**
1. D = X₁ − X₂ for each pair
2. D̄ = ΣD / n
3. SS_D = ΣD² − (ΣD)²/n
4. sD = √(SS_D / (n − 1))

**Panel II — Estimated standard error:**
$$s_{\bar{D}} = \frac{s_D}{\sqrt{n}}$$

**Panel III — t ratio:**
$$t = \frac{\bar{D} - 0}{s_{\bar{D}}}$$

---

## 15.6 Estimating Effect Size

### Confidence Interval for μD

$$\text{CI} = \bar{D} \pm (t_{conf})(s_{\bar{D}})$$

- Use $t_{\text{conf}}$ from Table B (two-tailed panel) for desired confidence and $\text{df} = n - 1$

### EPO Example

- 95% CI: 5 ± (2.571)(0.68) = **3.25 to 6.75 minutes**
- Both limits positive → single interpretation: EPO facilitates endurance; effect is between 3.25 and 6.75 minutes on average.

### Cohen's d (Two Related Samples)

$$d = \frac{\bar{D}}{s_D}$$

- **D̄** = mean difference; **sD** = standard deviation of difference scores
- EPO example: d = 5 / 1.67 ≈ **2.99** (very large effect)

---

## 15.7 Assumptions

- **Normality:** The population of difference scores is normally distributed.
- **Robustness:** Violations matter most when n is small (< ~10 pairs).
- **Remedies:** Increase n or use Wilcoxon T test (Chapter 20).

---

## 15.8 Overview: Three t Tests for Population Means

### Decision Tree

1. **One or two samples?**
   - One sample → **t test for one sample** (Chapter 13)
   - Two samples → continue

2. **Are the two samples paired?**
   - Yes (repeated measures or matched pairs) → **t test for two related samples** (Chapter 15)
   - No → **t test for two independent samples** (Chapter 14)

### Summary Table (Table 15.3)

| Type | Sample Mean | $H_0$ | Standard Error | df |
|------|-------------|-----|----------------|-----|
| **One sample** | $\bar{X}$ | $\mu$ = some number | $s_{\bar{X}} = s/\sqrt{n}$ | $n - 1$ |
| **Two independent** | $\bar{X}_1 - \bar{X}_2$ | $\mu_1 - \mu_2 = 0$ | $s_{\bar{X}_1 - \bar{X}_2}$ (Formula 14.3) | $n_1 + n_2 - 2$ |
| **Two related** | $\bar{D}$ | $\mu_D = 0$ | $s_{\bar{D}} = s_D/\sqrt{n}$ | $n - 1$ |

---

## 15.9 t Test for the Population Correlation Coefficient, ρ

### When to Use

- **Two related samples** (paired observations)
- Question: Is there a **relationship** between X and Y? (not a mean difference)
- **Measure:** Sample correlation coefficient r
- **Hypothesis:** $H_0$: ρ = 0 (no correlation in population)

### t Ratio for ρ

$$t = \frac{r - \rho_{\text{hyp}}}{\sqrt{\frac{1 - r^2}{n - 2}}}$$

- **$\rho_{\text{hyp}}$** = 0 (always, for testing zero correlation)
- **df** = n − 2 (two degrees of freedom lost for the regression line)

### Greeting Card Example (Chapter 6)

- r = .80, n = 5
- t = .80 / √[(1 − .64)/3] ≈ 2.29
- Critical t = ±3.182 (df = 3, two-tailed, α = .05)
- **Decision:** Retain $H_0$ — population correlation could equal zero
- **Note:** With n = 5, r = .88 would be needed to reject $H_0$; small n → large sampling variability for r

### Cohen's Guidelines for r

| r | Relationship |
|---|--------------|
| ~.10 | Weak |
| ~.30 | Moderate |
| ~.50 | Strong |

### Assumptions

- Relationship between X and Y is **linear**
- Sample from a **normal bivariate population**

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **Related samples** | Paired observations (repeated measures or matched pairs) |
| **Difference scores** | D = X₁ − X₂; reduces two-sample to one-sample problem |
| **Advantage** | Eliminates individual differences → smaller SE → more power |
| **df** | n − 1 (n = number of pairs) |
| **Cohen's d** | D̄ / sD |
| **Counterbalancing** | Reverse order of conditions for half the subjects |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Difference score (D)** | X₁ − X₂ for each pair |
| **Repeated measures** | Same subject measured more than once |
| **Two related samples** | Each observation in one sample paired with one in the other |
| **Counterbalancing** | Reversing order of conditions for equal numbers of subjects |
| **Population correlation coefficient (ρ)** | Correlation between two variables in the population |

---

## Key Equations

**Difference score:**
$$D = X_1 - X_2$$

**Mean difference:**
$$\bar{D} = \frac{\Sigma D}{n}$$

**t ratio (two related samples):**
$$t = \frac{\bar{D} - \mu_{D,hyp}}{s_{\bar{D}}}$$

**Estimated standard error:**
$$s_{\bar{D}} = \frac{s_D}{\sqrt{n}}$$

**Sample standard deviation of D:**
$$s_D = \sqrt{\frac{SS_D}{n - 1}}$$

**Confidence interval for μD:**
$$\text{CI} = \bar{D} \pm (t_{conf})(s_{\bar{D}})$$

**Cohen's d (related samples):**
$$d = \frac{\bar{D}}{s_D}$$

**t test for ρ:**
$$t = \frac{r - 0}{\sqrt{\frac{1 - r^2}{n - 2}}}$$

---

## Quick Reference: Which t Test?

| Design | t Test |
|--------|--------|
| One sample, compare to known value | One sample |
| Two groups, different subjects | Two independent samples |
| Two conditions, same or matched subjects | Two related samples |
| Test correlation ρ = 0 | t test for ρ |

---

## Next Chapter

**Chapter 16:** Continues with additional statistical tests (check table of contents for specific topic).

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
