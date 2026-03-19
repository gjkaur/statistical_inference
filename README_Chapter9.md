# Chapter 9: Sampling Distribution of the Mean — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 9 introduces the **sampling distribution of the mean**—the central concept in inferential statistics. It is the probability distribution of sample means for all possible random samples of a given size from a population. This distribution is the reference for deciding whether an observed sample mean is a common or rare outcome. The chapter covers its **mean**, **standard deviation (standard error)**, and **shape** (Central Limit Theorem).

---

## 9.1 What Is a Sampling Distribution?

**The sampling distribution of the mean is the probability distribution of means for all possible random samples of a given size from some population.**

### Key Ideas

- **Not** the distribution of scores in a single sample.
- **Not** the distribution of scores in the population.
- **Is** the distribution of **sample means** across all possible random samples of size n.

### Why It Matters

- A single sample mean (e.g., 533) could occur by chance even if the population mean is 500.
- The sampling distribution describes **all possible sample means** and their probabilities.
- We use it to decide whether the observed mean is:
  - **Common** → Could be due to chance; nothing special in the population.
  - **Rare** → Unlikely due to chance alone; something special probably in the population.

### "All Possible Random Samples"

- Refers to all **different ways** a sample of size n can be selected from the population.
- This number is usually very large (e.g., astronomical for n=100 from a population of 1000+).
- We **do not** construct it by hand; **statistical theory** gives us its mean, standard deviation, and shape.

---

## 9.2 Creating a Sampling Distribution from Scratch

### Simplified Example

- **Population:** 4 scores: 2, 3, 4, 5 (μ = 3.5)
- **Sample size:** n = 2
- **All possible samples:** 4 × 4 = 16 (with replacement)
- For each sample, compute the mean (X̄).
- The 16 sample means form the **sampling distribution of the mean**.

### Result

- Sample means: 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0
- Probabilities vary (e.g., 3.5 appears 4/16 of the time)
- The distribution is **more compact** than the population (less variability)

### Purpose

- Clarifies what a sampling distribution is.
- In practice, we rely on theory, not enumeration.

---

## 9.3 Some Important Symbols

| Distribution | Mean | Standard Deviation |
|--------------|------|---------------------|
| **Sample** | X̄ | s |
| **Population** | μ | σ |
| **Sampling distribution of the mean** | μX̄ | σX̄ (standard error) |

### Notes

- **μX̄** (mu sub X-bar) = mean of the sampling distribution
- **σX̄** (sigma sub X-bar) = standard error of the mean
- Greek letters (μ, σ) = populations and sampling distributions (all possibilities)
- English letters (X̄, s) = samples (observed data)

---

## 9.4 Mean of All Sample Means (μX̄)

**The mean of the sampling distribution of the mean always equals the population mean.**

$$\mu_{\bar{X}} = \mu$$

### Implications

- μX̄ and μ are **interchangeable** in inferential statistics.
- If the population mean is 500, the sampling distribution is centered at 500.
- The observed sample mean (e.g., 533) is evaluated as a deviation from μ (or μX̄).

### Intuition

- Individual sample means vary above and below μ.
- Averaging over all possible sample means cancels out this variation, leaving μ.

---

## 9.5 Standard Error of the Mean (σX̄)

**The standard error of the mean equals the population standard deviation divided by the square root of the sample size.**

$$\sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}}$$

### Interpretation

> **The standard error of the mean is a rough measure of the average amount by which sample means deviate from the population mean (or from μX̄).**

### Properties

- **Smaller than σ** whenever n ≥ 2 (sample means vary less than individual scores).
- **Decreases as n increases** — Larger samples → less variability among sample means → more precise estimates.
- The "error" refers to **generalization error** (samples not perfectly representing the population), not calculation error.

### Example

- σ = 110 (SAT math), n = 100
- σX̄ = 110 / √100 = 110 / 10 = **11**
- Variability is reduced by a factor of 10.

### Rules of Thumb (When Shape Is Normal)

- ~68% of sample means within ±1 σX̄ of μ
- ~95% of sample means within ±2 σX̄ of μ
- ~5% of sample means beyond ±2 σX̄ of μ

---

## 9.6 Shape of the Sampling Distribution

### Central Limit Theorem

**Regardless of the shape of the population, the shape of the sampling distribution of the mean approximates a normal curve if the sample size is sufficiently large.**

### "Sufficiently Large"

| Population Shape | Sufficient Sample Size |
|-------------------|------------------------|
| **Normal** | Any size (even n = 1) |
| **Non-normal** | Typically n = 25 to 100 |

### Why It Works

- **Intermediate values dominate:** Large samples usually include a mix of small, medium, and large scores; the mean tends to be intermediate.
- **Extreme values are rarer:** Samples with many extreme scores in one direction are less common, so extreme sample means are less frequent.
- Result: Bell-shaped (normal) distribution of sample means.

### Practical Use

- With n = 100, we can treat the sampling distribution as approximately normal.
- We can use the **standard normal table** (Table A) for probability statements about sample means.

---

## 9.7 Other Sampling Distributions

### For the Mean

- Different **populations** → different sampling distributions.
- Different **sample sizes** → different σX̄ (μX̄ = μ always).
- Each (population, n) pair has its own sampling distribution of the mean.

### For Other Statistics

- Sampling distributions exist for: **medians**, **proportions**, **standard deviations**, **variances**, **correlations**, **differences between means**, etc.
- Later chapters use these for hypothesis tests and confidence intervals.

---

## Summary: Three Key Properties

| Property | Formula/Description |
|----------|---------------------|
| **Mean** | μX̄ = μ (equals population mean) |
| **Standard deviation** | σX̄ = σ / √n (standard error) |
| **Shape** | Approximately normal if n is large enough (Central Limit Theorem) |

---

## Key Equations

**Mean of the Sampling Distribution:**
$$\mu_{\bar{X}} = \mu$$

**Standard Error of the Mean:**
$$\sigma_{\bar{X}} = \frac{\sigma}{\sqrt{n}}$$

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Sampling distribution of the mean | Probability distribution of means for all possible random samples of size n |
| Mean of the sampling distribution (μX̄) | Equals the population mean μ |
| Standard error of the mean (σX̄) | σ/√n; variability of sample means |
| Central limit theorem | Sampling distribution of the mean is approximately normal for large n |

---

## Quick Reference: Sampling Distribution vs. Population vs. Sample

```
POPULATION                    SAMPLE                    SAMPLING DISTRIBUTION
All observations              One set of n observations  All possible sample means
Mean: μ                       Mean: X̄                    Mean: μX̄ = μ
SD: σ                         SD: s                      SD: σX̄ = σ/√n
Shape: any                    Shape: reflects population  Shape: ≈ normal (if n large)
```

---

## Next Chapter

**Chapter 10: Introduction to Hypothesis Testing: The z Test** — Using the sampling distribution to test hypotheses about a population mean; null and alternative hypotheses; decision rules; z test.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
