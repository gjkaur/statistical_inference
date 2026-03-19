# Chapter 12: Estimation (Confidence Intervals) — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 12 introduces **estimation**—using sample data to estimate unknown population parameters. Instead of testing a hypothesis about a specific value, we estimate the value itself. The chapter covers **point estimates**, **confidence intervals for the population mean (μ)**, interpretation of confidence intervals, the effect of **level of confidence** and **sample size**, when to use confidence intervals vs. hypothesis tests, and **confidence intervals for population percents** (proportions).

---

## 12.1 Point Estimate for μ

### Definition

A **point estimate** uses a single value to represent the unknown population mean.

- **Best point estimate for μ** = the sample mean, X̄
- Example: If a random sample of 100 local freshmen has mean SAT score 533, then **533** is the point estimate of the population mean.

### Basic Deficiency

- Point estimates tend to be **inaccurate** because of sampling variability.
- A single sample mean is unlikely to equal the population mean exactly.
- Point estimates convey **no information** about the degree of inaccuracy.
- Statisticians therefore supplement point estimates with **interval estimates** (confidence intervals).

---

## 12.2 Confidence Interval (CI) for μ

### Definition

A **confidence interval** uses a range of values that, with a known degree of certainty, includes the unknown population mean.

- Example: With 95% confidence, the interval **511.44 to 554.56** includes the mean SAT math score for all local freshmen.

### Why Confidence Intervals Work

Based on three properties of the sampling distribution of the mean:

1. **Mean** of the sampling distribution = unknown population mean μ
2. **Standard error** σX̄ = σ/√n
3. **Shape** approximates normal (when n is large enough for the Central Limit Theorem)

### The Logic

- **95% of all sample means** fall within 1.96 standard errors of the unknown population mean.
- For each sample mean, construct an interval: X̄ ± 1.96 σX̄
- **95% of these intervals** will include the unknown population mean (true intervals).
- **5% of these intervals** will fail to include it (false intervals).

### Formula for Confidence Interval

$$\text{CI} = \bar{X} \pm (z_{conf})(\sigma_{\bar{X}})$$

where:
- **X̄** = sample mean
- **zconf** = z score from the standard normal table for the desired level of confidence (e.g., 1.96 for 95%)
- **σX̄** = standard error = σ/√n

### SAT Example

- X̄ = 533, σX̄ = 11, zconf = 1.96
- CI = 533 ± (1.96)(11) = 533 ± 21.56
- **95% CI:** 511.44 to 554.56

### Assumptions

1. **Population standard deviation (σ) is known**
2. **Population is normal** OR **sample size is sufficiently large** (n ≥ 25) for the Central Limit Theorem

*When σ is unknown, use the t-based confidence interval (Chapter 13).*

### Note: Proportion/Percent as a Special Case

- A **proportion** (or percent) is a special type of mean: code observations as 0 or 1, then add the 1s and divide by n.
- The standard error of a proportion can be obtained from the formula for the standard error of the mean (see Section 12.7 for CI for population percent).

---

## 12.3 Interpretation of a Confidence Interval

### What "95% Confidence" Means

- **Long-term performance:** If many 95% confidence intervals were constructed from repeated samples, approximately **95%** would include the population mean.
- **Single interval:** Any one interval is either true or false—we never know which.
- **Practical interpretation:** When the level of confidence is 95% or more, we can be **reasonably confident** that our one observed interval includes the true population mean.

### Common Misinterpretations (Avoid These)

| Incorrect | Correct |
|-----------|---------|
| "95% of the data fall within the interval" | The interval estimates the **population mean**, not individual scores |
| "The population mean definitely is in the interval" | We can never be certain; we are reasonably confident |
| "This interval is true 95% of the time" | The interval is fixed once constructed; it either contains μ or it doesn't |

---

## 12.4 Level of Confidence

### Definition

The **level of confidence** indicates the percent of time that a series of confidence intervals includes the unknown population characteristic.

### Common Levels

| Level | zconf | Use |
|-------|-------|-----|
| **95%** | 1.96 | Most common; default choice |
| **99%** | 2.58 | When a false interval has serious consequences |

### Effect on Width

- **Higher level of confidence** → larger zconf → **wider** (less precise) interval
- **Lower level of confidence** → smaller zconf → **narrower** (more precise) interval

**Example:** 99% CI (504.62 to 561.38) is wider than 95% CI (511.44 to 554.56) for the same SAT data.

### Choosing a Level

- **95%:** Default; most prevalent in research
- **99%:** When a false interval could have serious consequences (e.g., failing to predict a presidential election winner)

---

## 12.5 Effect of Sample Size

### Larger Sample Size

- **Standard error decreases:** σX̄ = σ/√n
- **Result:** Narrower, more precise confidence interval
- As n → ∞, the interval shrinks toward the point estimate

### Unlike Hypothesis Tests

- For confidence intervals, **sample size can never be too large**
- Larger samples always yield more precise estimates
- (For hypothesis tests, very large samples can detect trivially small effects)

### Selecting Sample Size

- Formulas exist to determine the sample size needed for a desired **precision** (width) and **level of confidence**
- Requires knowing or estimating the population standard deviation before the investigation

---

## 12.6 Hypothesis Tests or Confidence Intervals?

### Key Difference

| Approach | What It Tells You |
|----------|-------------------|
| **Hypothesis test** | Whether or not an effect is present |
| **Confidence interval** | The **possible size** of the effect |

### When to Use Which

| Situation | Preferred Approach |
|-----------|---------------------|
| Primary concern: Is an effect present? (e.g., new research area) | **Hypothesis test** |
| Primary concern: How big is the effect? (e.g., established effect) | **Confidence interval** |
| Null hypothesis has been rejected | **Follow up with a confidence interval** to estimate effect size |

### Example: Vitamin C and IQ

- **Hypothesis test:** Indicates whether vitamin C has an effect on IQ
- **Confidence interval:** Indicates the possible size—e.g., 95% CI of 102 to 112 suggests the effect is between 2 and 12 IQ points above 100

---

## 12.7 Confidence Interval for Population Percent

### Context

- Often used in **polls** and **surveys**
- Example: "64% of a random sample of 1,500 Americans favor capital punishment; margin of error ±3%"

### Structure

- **95% CI** = sample percent ± (1.96)(standard error of the percent)
- **Margin of error** = the amount added to and subtracted from the sample percent

### Example

- Sample percent = 64%, margin of error = ±3%
- **95% CI:** 61% to 67%
- Interpretation: We can be reasonably confident that the true population percent is between 61% and 67%.

### Sample Size and Margin of Error

| Sample Size | Approx. Margin of Error (±) |
|-------------|-----------------------------|
| 1,500 | ±3% |
| 500 | ±5% |
| 100 | ±10% |

- Pollsters often use large samples (hundreds or thousands) for narrower intervals
- Surveys: larger samples are generally better (unlike experiments, where very large samples can be problematic)

### A Final Caution

- Confidence intervals reflect only **statistical error** due to random sampling
- **Nonstatistical errors** can compromise results: biased questions, nonresponse, unrepresentative samples
- Interpret poll results cautiously without background information on methodology

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **Point estimate** | Single value (X̄) for μ; simple but tends to be inaccurate |
| **Confidence interval** | Range that includes μ with known probability (e.g., 95%) |
| **95% CI** | In the long run, ~95% of such intervals include μ |
| **Interpretation** | We are reasonably confident our interval includes μ |
| **Level of confidence** | Higher → wider interval; lower → narrower interval |
| **Sample size** | Larger → narrower, more precise interval |
| **vs. Hypothesis test** | CI shows possible effect size; test shows whether effect exists |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Point estimate** | A single value that represents an unknown population characteristic |
| **Confidence interval (CI)** | A range of values that, with a known degree of certainty, includes an unknown population characteristic |
| **Level of confidence** | The percent of time that a series of CIs includes the unknown population characteristic |
| **Margin of error** | The amount added to and subtracted from a sample value (e.g., mean or percent) to obtain the limits of a CI |

---

## Key Equation

**Confidence Interval for μ (when σ is known):**

$$\text{CI} = \bar{X} \pm (z_{conf})(\sigma_{\bar{X}})$$

where σX̄ = σ/√n

---

## Quick Reference: zconf Values

| Level of Confidence | zconf |
|---------------------|-------|
| 90% | 1.65 |
| 95% | 1.96 |
| 99% | 2.58 |

---

## Next Chapter

**Chapter 13: t Test for One Sample** — Hypothesis testing and confidence intervals when the population standard deviation is unknown (using the sample standard deviation and the t distribution).

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
