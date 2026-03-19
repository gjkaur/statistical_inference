# Chapter 14: t Test for Two Independent Samples — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 14 describes the **t test for two independent samples**—comparing the means of two groups (e.g., treatment vs. control) when subjects in each group are different and unmatched. This design, when done properly (e.g., random assignment), supports cause-effect conclusions. The chapter covers statistical hypotheses, the sampling distribution of the difference between means, the t ratio, calculations (including pooled variance), **p-values**, **statistical significance**, **effect size** (point estimates, confidence intervals, Cohen's d), **meta-analysis**, replication, reporting in the literature, assumptions, and computer output.

---

## 14.1 EPO Experiment

### Context

- **Research question:** Does EPO (erythropoietin) increase endurance in severely depressed patients?
- **Design:** Random assignment to **treatment** (EPO) or **control** (placebo)
- **Measure:** Time (minutes) on a rapidly moving treadmill
- **Samples:** n₁ = 6, n₂ = 6 (small for computational convenience)

### Two Independent Samples

- **Independent samples:** Each group has different subjects; observations are not paired.
- Contrast with **related samples** (Chapter 15): same subjects or matched pairs.

### Two Populations

- **Treatment population:** Endurance scores for patients who receive EPO
- **Control population:** Endurance scores for patients who do not receive EPO
- The **effect** = difference between population means (μ₁ − μ₂)

---

## 14.2 Statistical Hypotheses

### Null and Alternative Hypotheses

| Test Type | H₀ | H₁ |
|-----------|-----|-----|
| **Upper tail (EPO example)** | μ₁ − μ₂ ≤ 0 | μ₁ − μ₂ > 0 |
| **Lower tail** | μ₁ − μ₂ ≥ 0 | μ₁ − μ₂ < 0 |
| **Two-tailed** | μ₁ − μ₂ = 0 | μ₁ − μ₂ ≠ 0 |

- **EPO example:** One-tailed, upper tail critical (reject only if treatment mean exceeds control mean)

---

## 14.3 Sampling Distribution of X̄₁ − X̄₂

### Definition

The **sampling distribution of X̄₁ − X̄₂** is the distribution of all possible differences between sample means based on all possible pairs of random samples from the two populations.

### Mean

$$\mu_{\bar{X}_1 - \bar{X}_2} = \mu_1 - \mu_2$$

The mean of the sampling distribution equals the difference between population means.

### Standard Error (when population variances known)

$$\sigma_{\bar{X}_1 - \bar{X}_2} = \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}$$

- Roughly measures the average amount by which any sample mean difference deviates from μ₁ − μ₂
- Larger than the standard error for a single mean (extra variability from two samples)
- Decreases as sample sizes increase

---

## 14.4 t Test

### t Ratio

$$t = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2)_{hyp}}{s_{\bar{X}_1 - \bar{X}_2}}$$

- **(μ₁ − μ₂)hyp** = 0 (typically)
- **sX̄₁−X̄₂** = estimated standard error (Formula 14.3)

### Degrees of Freedom

$$df = n_1 + n_2 - 2$$

### EPO Example

- X̄₁ = 11, X̄₂ = 6, (X̄₁ − X̄₂) = 5
- sX̄₁−X̄₂ = 2.32
- t = (11 − 6 − 0) / 2.32 = **2.16**
- Critical t = 1.812 (df = 10, one-tailed, α = .05)
- **Decision:** Reject H₀
- **Interpretation:** EPO increases mean endurance scores.

---

## 14.5 Details: Calculations for the t Test

### Four Panels (Table 14.1)

**Panel I — Sample means and sums of squares:**
- X̄₁, X̄₂, SS₁, SS₂
- SS = ΣX² − (ΣX)²/n for each group

**Panel II — Pooled variance:**
$$s_p^2 = \frac{SS_1 + SS_2}{n_1 + n_2 - 2} = \frac{SS_1 + SS_2}{df}$$

- Assumes **equal population variances** (σ₁² = σ₂²)
- Combines both samples for a more accurate estimate

**Panel III — Estimated standard error:**
$$s_{\bar{X}_1 - \bar{X}_2} = \sqrt{\frac{s_p^2}{n_1} + \frac{s_p^2}{n_2}}$$

**Panel IV — t ratio:**
$$t = \frac{(\bar{X}_1 - \bar{X}_2) - 0}{s_{\bar{X}_1 - \bar{X}_2}}$$

---

## 14.6 p-Values

### Definition

The **p-value** is the degree of rarity of the test result, given that the null hypothesis is true.

- **Smaller p-value** → more rare → tends to discredit H₀, support H₁
- **Larger p-value** → less rare → does not discredit H₀

### Interpretation

- p-value = proportion of area in the tail(s) beyond the observed t
- **One-tailed p-value:** Area in one tail
- **Two-tailed p-value:** Area in both tails (typically 2 × one-tailed)

### Finding Approximate p-Values (Table B)

- Locate observed t relative to critical values in the row for the correct df
- Follow the vertical line upward to get p < .05, p < .01, p < .001, or p > .05

### p-Value vs. Level of Significance

| | Level of Significance (α) | p-Value |
|---|---------------------------|---------|
| **When specified** | Before the test | After the test |
| **Meaning** | Cutoff that triggers rejection | Actual rarity of the observed result |

- **p < .05** → would reject H₀ at α = .05
- **p > .05** → would retain H₀ at α = .05

---

## 14.7 Statistically Significant Results

### Definition

**Statistically significant** = the null hypothesis has been rejected; the result is unlikely due to chance alone.

- Correct usage: **Rejecting H₀** refers to the population; **statistically significant** refers to the sample result.

### Important Caveats

1. **Statistical significance ≠ practical importance**
   - A result can be statistically significant but trivial (e.g., tiny mean difference with huge n)
   - Statistical significance only indicates the observed effect is large relative to the standard error

2. **Beware of excessively large samples**
   - Very large n → very small standard error → even tiny, unimportant effects become "significant"

3. **Avoid erroneous conditional probability**
   - Correct: Pr(observed result | H₀ true) ≤ .05
   - Incorrect: Pr(H₀ true | observed result) ≤ .05
   - We cannot conclude H₀ is true with probability .05; we can only say it is probably false.

---

## 14.8 Estimating Effect Size: Point Estimates and Confidence Intervals

### Point Estimate

- **Point estimate of effect** = X̄₁ − X̄₂ (e.g., 5 minutes for EPO)
- Simple but ignores sampling variability

### Confidence Interval for μ₁ − μ₂

$$\text{CI} = (\bar{X}_1 - \bar{X}_2) \pm (t_{conf})(s_{\bar{X}_1 - \bar{X}_2})$$

- Use tconf from Table B (two-tailed panel) for desired confidence and df = n₁ + n₂ − 2

### Interpreting CI for μ₁ − μ₂

- **Both limits positive** → single interpretation: treatment mean exceeds control mean
- **Both limits negative** → single interpretation: treatment mean is less than control mean
- **Mixed signs** (e.g., −0.17 to 10.17) → no single interpretation; effect could be positive, negative, or zero

**Key point:** A single interpretation is possible only if both limits share the same sign.

---

## 14.9 Estimating Effect Size: Cohen's d

### Formula

$$d = \frac{\bar{X}_1 - \bar{X}_2}{s_p} = \frac{\text{mean difference}}{\text{standard deviation}}$$

where s_p = √(s_p²) is the pooled standard deviation.

### Why Use d?

- **Unit-free:** Original units cancel; d is in standard deviation units
- **Comparable across studies:** Can compare effects from different measures (e.g., reaction time vs. weight)
- **Not influenced by sample size:** Unlike the standard error, s_p is stable as n increases

### Cohen's Guidelines

| d | Effect Size |
|---|-------------|
| ~0.20 | Small |
| ~0.50 | Medium |
| ~0.80 | Large |

### Examples (with typical SDs)

| Measure | Small (d = .20) | Medium (d = .50) | Large (d = .80) |
|---------|----------------|------------------|-----------------|
| GPA (s = 0.50) | 0.10 | 0.25 | 0.40 |
| IQ (s = 15) | 3 | 7.5 | 12 |
| SAT (s = 100) | 20 | 50 | 80 |

### EPO Example

- d = 5 / 4.02 ≈ **1.24** (large effect)

---

## 14.10 Meta-Analysis

- **Meta-analysis** = systematic review that combines results from many similar studies using statistical procedures
- Produces a **composite estimate** of effect (e.g., average Cohen's d) and its confidence interval
- Helps address **publication bias** (file drawer effect): nonsignificant results often go unpublished

---

## 14.11 Importance of Replication

- A single statistically significant finding may be a **false positive** (Type I error)
- **File drawer effect:** Many unreported nonsignificant studies can inflate the apparent rate of significant findings
- **Recommendation:** Wait for replication before accepting new findings, especially for complex or controversial topics

---

## 14.12 Reports in the Literature

### Typical Format

> Endurance scores for the EPO group (M = 11, SD = 4.24) significantly exceeded those for the control group (M = 6, SD = 3.79), t(10) = 2.16, p < .05, d = 1.24.

- Report: means, standard deviations, t, df, p-value, effect size (d or CI)

### Data Graphs

- Dots or bars for group means
- **Error bars** = standard error, standard deviation, or 95% CI (specify which)
- Nonoverlapping error bars (for SE) often suggest statistical significance

---

## 14.13 Assumptions

1. **Normality:** Both populations are normally distributed
2. **Equal variances:** σ₁² = σ₂² (homogeneity of variance)

### Robustness

- Violations matter most when sample sizes are **small** and **unequal**
- If both n₁ and n₂ are fairly large (> ~10) and equal, violations are usually tolerable
- **Remedies:** Increase n, equate sample sizes, use t test for unequal variances, or use nonparametric test (e.g., Mann-Whitney U)

---

## 14.14 Computer Output

- Software (SAS, SPSS, Minitab) provides t, df, p-value, confidence limits
- **Pooled (equal variances)** vs. **Satterthwaite (unequal variances)** t test
- **Levene's test** (or folded F test) is commonly used to test homogeneity of variance before the t test
- If the test for equality of variances suggests unequal variances (p < .10), report the **unequal-variances (Welch-Satterthwaite)** t test instead of the pooled t test

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **Design** | Two independent samples (different subjects per group) |
| **Hypotheses** | H₀: μ₁ − μ₂ = 0 (or ≤ 0, ≥ 0); H₁: μ₁ − μ₂ ≠ 0 (or < 0, > 0) |
| **df** | n₁ + n₂ − 2 |
| **Pooled variance** | s_p² = (SS₁ + SS₂) / (n₁ + n₂ − 2) |
| **Effect size** | Cohen's d = (X̄₁ − X̄₂) / s_p |
| **Statistical significance** | Does not imply practical importance |
| **CI interpretation** | Single interpretation only if both limits have same sign |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Two independent samples** | Different, unmatched subjects in each group |
| **Effect** | Difference between two population means |
| **Sampling distribution of X̄₁ − X̄₂** | Distribution of differences between sample means |
| **Pooled variance (s_p²)** | Combined estimate of common population variance |
| **Estimated standard error (sX̄₁−X̄₂)** | Standard error when σ is estimated |
| **p-value** | Degree of rarity of the test result given H₀ true |
| **Statistical significance** | H₀ rejected; result unlikely due to chance |
| **Cohen's d** | Standardized effect size in SD units |
| **File drawer effect** | Bias from unpublished nonsignificant results |
| **Meta-analysis** | Statistical synthesis of multiple studies |

---

## Key Equations

**t ratio:**
$$t = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2)_{hyp}}{s_{\bar{X}_1 - \bar{X}_2}}$$

**Pooled variance:**
$$s_p^2 = \frac{SS_1 + SS_2}{n_1 + n_2 - 2}$$

**Estimated standard error:**
$$s_{\bar{X}_1 - \bar{X}_2} = \sqrt{\frac{s_p^2}{n_1} + \frac{s_p^2}{n_2}}$$

**Confidence interval for μ₁ − μ₂:**
$$\text{CI} = (\bar{X}_1 - \bar{X}_2) \pm (t_{conf})(s_{\bar{X}_1 - \bar{X}_2})$$

**Cohen's d:**
$$d = \frac{\bar{X}_1 - \bar{X}_2}{s_p}$$

---

## Next Chapter

**Chapter 15: t Test for Two Related Samples** — Comparing means when observations are paired (same subjects or matched pairs).

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
