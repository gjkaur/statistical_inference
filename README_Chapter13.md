# Chapter 13: t Test for One Sample — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 13 introduces the **t test for a single population mean**—the counterpart of the $z$ test when the **population standard deviation ($\sigma$) is unknown**. Because $\sigma$ is usually unknown in practice, the $t$ test is used far more often than the $z$ test. The chapter covers the **sampling distribution of $t$**, **degrees of freedom**, estimating the standard error with the sample standard deviation, the **$t$ ratio**, **confidence intervals based on $t$**, and the assumptions of the test.

---

## 13.1 Gas Mileage Investigation

### Context

- **Scenario:** Federal law requires new cars to average 45 mpg. Compliance is tested via random samples.
- **Penalty:** $200 per car if the test indicates substandard performance.
- **$H_0\colon \mu \ge 45$** (population mean meets or exceeds 45 mpg)
- **$H_1\colon \mu < 45$** (population mean is below 45 mpg)
- **Test:** One-tailed, lower tail critical; $\alpha = 0.01$ (Type I error is serious for the manufacturer)
- **Sample:** $n = 6$ cars (small for computational simplicity)

### Why t Instead of z?

- The **population standard deviation ($\sigma$)** is unknown.
- $\sigma$ must be **estimated** with the sample standard deviation ($s$).
- Estimating $\sigma$ changes the sampling distribution and requires the **$t$ test** instead of the $z$ test.

---

## 13.2 Sampling Distribution of t

### Definition

The **sampling distribution of t** is the distribution that would be obtained if a value of t were calculated for each sample mean for all possible random samples of a given size from some population.

- Discovered by William Gosset (pen name "Student"); hence "Student's t distribution."
- There is a **family** of t distributions, one for each value of **degrees of freedom (df)**.

### Degrees of Freedom (One Sample)

$$df = n - 1$$

- When we use the n deviations about the sample mean to estimate population variability, only **n − 1** are free to vary.
- The sum of deviations about the mean must equal zero; this restriction removes one degree of freedom.
- For the gas mileage example: df = 6 − 1 = 5.

### t vs. z Distribution

| Property | t Distribution | z Distribution |
|----------|----------------|----------------|
| Shape | Symmetrical, bell-shaped, unimodal | Same |
| Center | Peaks at 0 | Same |
| Tails | **More inflated** (especially with small df) | Thinner |
| As df → ∞ | Approaches standard normal | Same as standard normal |

- **Critical t values are larger** than critical z values (e.g., at α = .01, one-tailed: t = 3.365 vs. z = 2.33 for df = 5).
- This compensates for the extra variability when estimating σ with s.

### Finding Critical t Values (Table B)

1. Locate the row for the correct **df** (n − 1).
2. Locate the column for the test type (one-tailed or two-tailed) and **α**.
3. For one-tailed tests, add a negative sign if the lower tail is critical.

**If df is missing:** Use the row with the **next smallest** df (e.g., if df = 36, use df = 30). This makes the test slightly more conservative.

---

## 13.3 t Test

### t Ratio Formula

$$t = \frac{\bar{X} - \mu_{\text{hyp}}}{s_{\bar{X}}} = \frac{\bar{X} - \mu_{\text{hyp}}}{s/\sqrt{n}}$$

where:
- **$\bar{X}$** = sample mean
- **$\mu_{\text{hyp}}$** = hypothesized population mean
- **$s_{\bar{X}}$** = estimated standard error of the mean = $s/\sqrt{n}$

### Gas Mileage Example

- $\bar{X} = 43$, $\mu_{\text{hyp}} = 45$, $s_{\bar{X}} = 0.89$
- t = (43 − 45) / 0.89 = **−2.25**
- Critical t = −3.365 (df = 5, one-tailed, α = .01)
- **Decision:** Retain $H_0$ because −2.25 > −3.365 (less negative than critical)
- **Interpretation:** The population mean could equal 45 mpg or more; the manufacturer should not be penalized.

### Greater Variability of t

- Because the tails of t are more inflated than z, the **critical t** is larger than the critical z.
- This makes it slightly harder to reject $H_0$ when using t—correctly accounting for the uncertainty in estimating σ.

---

## 13.4 Common Theme of Hypothesis Tests

All hypothesis tests (z, t, F, U, T, H, etc.) follow the same logic:

- If the observed result qualifies as a **rare outcome** under $H_0$ → **reject $H_0$**.
- Otherwise → **retain $H_0$**.
- To assess rarity, convert the observed value to a test statistic (e.g., t) and compare it to critical values from the appropriate sampling distribution.

---

## 13.5 Reminder About Degrees of Freedom

- **Degrees of freedom** = number of values free to vary given one or more mathematical restrictions.
- When using sample data to estimate a population characteristic, not all observations are free to vary.
- Example: Six gas mileage values (40, 44, 46, 41, 43, 44) have mean 43; only five deviations are free to vary (the sixth is determined by the zero-sum constraint).
- df is used throughout the remainder of the book for various tests.

---

## 13.6 Details: Estimating the Standard Error ($s_{\bar{X}}$)

### When σ Is Unknown

- Replace σ with **s** (sample standard deviation) in the standard error formula.
- **Estimated standard error of the mean:**

$$s_{\bar{X}} = \frac{s}{\sqrt{n}}$$

### Computing s

1. **Sum of squares:** SS = ΣX² − (ΣX)²/n
2. **Sample variance:** s² = SS / (n − 1) = SS / df
3. **Sample standard deviation:** s = √(SS / df)

**Important:** Use **n − 1** (not n) when dividing SS to obtain s; use **n** when taking the square root for $s_{\bar{X}}$.

---

## 13.7 Details: Calculations for the t Test

### Step-by-Step (Table 13.1)

**Panel I — Finding X̄ and s:**
1. n, ΣX, ΣX²
2. X̄ = ΣX / n
3. SS = ΣX² − (ΣX)²/n
4. $s = \sqrt{\text{SS} / (n - 1)}$

**Panel II — Finding $s_{\bar{X}}$:**
5. $s_{\bar{X}} = s / \sqrt{n}$

**Panel III — Finding t:**
6. $t = (\bar{X} - \mu_{\text{hyp}}) / s_{\bar{X}}$

### Gas Mileage Example (Summary)

| Step | Value |
|------|-------|
| n | 6 |
| ΣX | 258 |
| X̄ | 43 |
| SS | 24 |
| s | 2.19 |
| $s_{\bar{X}}$ | 0.89 |
| $\mu_{\text{hyp}}$ | 45 |
| t | −2.25 |

---

## 13.8 Confidence Intervals for μ Based on t

### When to Use t-Based CI

- When σ is **unknown** and must be estimated with s.
- Same situation as the t test.

### Formula

$$\text{CI} = \bar{X} \pm (t_{\text{conf}})\,(s_{\bar{X}})$$

where:
- $t_{\text{conf}}$ = critical value from the t table for the desired level of confidence and $\text{df} = n - 1$
- Use the **two-tailed** panel of Table B (confidence intervals are symmetrical like two-tailed tests)

### Gas Mileage Example

- $\bar{X} = 43$, $s_{\bar{X}} = 0.89$, $\text{df} = 5$
- 95% confidence: $t_{\text{conf}} = 2.571$ (from Table B, two-tailed panel)
- CI = 43 ± (2.571)(0.89) = 43 ± 2.29
- **95% CI:** 40.71 to 45.29 mpg

**Interpretation:** We can be reasonably confident that the true mean gas mileage for the population is between 40.71 and 45.29 mpg.

---

## 13.9 Assumptions

### Normality

- Strictly speaking, the t test assumes the **population is normally distributed**.
- Violations matter most when **n is very small** (e.g., < 10).

### Robustness

- The t test is **robust** to moderate violations of normality when n is reasonably large.
- If the sample is small and appears to come from a non-normal population (e.g., pronounced skew), consider **increasing the sample size** before testing.

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **When to use t** | Population standard deviation σ is unknown |
| **Estimated standard error** | $s_{\bar{X}} = s/\sqrt{n}$ |

| **Degrees of freedom** | df = n − 1 |
| **t vs. z** | t has fatter tails; critical t > critical z |
| **t ratio** | $t = (\bar{X} - \mu_{\text{hyp}}) / s_{\bar{X}}$ |
| **CI for μ** | $\bar{X} \pm (t_{\text{conf}})(s_{\bar{X}})$ when σ unknown |
| **Assumption** | Population normal (or n not too small) |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Sampling distribution of t** | Distribution of t values for all possible samples of a given size |
| **t ratio** | $(\bar{X} - \mu_{\text{hyp}}) / s_{\bar{X}}$; replaces z when σ is estimated |
| **Degrees of freedom (df)** | Number of values free to vary given one or more restrictions; df = n − 1 for one sample |
| **Estimated standard error ($s_{\bar{X}}$)** | $s/\sqrt{n}$; used when σ is unknown |

---

## Key Equations

**t ratio:**
$$t = \frac{\bar{X} - \mu_{hyp}}{s_{\bar{X}}} = \frac{\bar{X} - \mu_{hyp}}{s/\sqrt{n}}$$

**Estimated standard error:**
$$s_{\bar{X}} = \frac{s}{\sqrt{n}}$$

**Degrees of freedom (one sample):**
$$df = n - 1$$

**Confidence interval for μ (when σ unknown):**
$$\text{CI} = \bar{X} \pm (t_{conf})(s_{\bar{X}})$$

---

## Quick Reference: When to Use z vs. t

| Condition | Use |
|-----------|-----|
| σ **known** | z test, z-based CI |
| σ **unknown** | t test, t-based CI |

---

## Next Chapter

**Chapter 14: t Test for Two Independent Samples** — Comparing means of two independent groups (e.g., treatment vs. control).

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
