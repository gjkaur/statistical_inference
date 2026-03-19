# Chapter 11: More about Hypothesis Testing — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 11 extends the hypothesis-testing framework from Chapter 10. It explains **why** hypothesis tests are used, the difference between **strong and weak decisions**, **one-tailed vs. two-tailed tests**, and how to choose the **level of significance**. The chapter introduces the **four possible outcomes** of a hypothesis test (including **Type I** and **Type II errors**), explores how **effect size** and **sample size** influence outcomes, and concludes with **power analysis** for choosing an appropriate sample size.

---

## 11.1 Why Hypothesis Tests?

### Generalizing Beyond Data

- Hypothesis tests are needed when we **generalize from a sample to a larger population**.
- If we had a **census** (complete data), no hypothesis test would be needed—we could interpret differences directly.
- With a **sample**, the observed difference might be due to **chance** (sampling variability), so we must evaluate it statistically.

### Role of the Standard Error

- The **standard error** measures how much sample means vary by chance around the population mean.
- Dividing the observed difference by the standard error gives **z**, which places the result on a scale of common vs. rare outcomes.
- **Small z** → common outcome → retain H0 (difference could be chance).
- **Large z** → rare outcome → reject H0 (difference unlikely due to chance alone).

**Example:** In the SAT example, (533 − 500) / 11 = 3. If σX̄ were 33 instead of 11, z would be 1, and we would retain H0.

### Possibility of Incorrect Decisions

- We never know for certain whether our decision is correct.
- **Type I error:** Rejecting a true H0 (false alarm).
- **Type II error:** Retaining a false H0 (miss).
- Abolishing rejection regions would eliminate Type I errors but would make it impossible to ever reject H0, including when it is false—so both types of errors must be balanced.

---

## 11.2 Strong or Weak Decisions

### Retaining H0 Is a Weak Decision

- Retaining H0 means the observed result is a **common outcome** under H0.
- H0 **could** be true, but the same result could also occur if the true mean were slightly different.
- **Interpretation:** We cannot conclude H0 is true; we only conclude it **could** be true.
- Many statisticians prefer to say we **fail to reject** H0 rather than "retain" it.

### Rejecting H0 Is a Strong Decision

- Rejecting H0 means the observed result is a **rare outcome** (probability ≤ α) under H0.
- This suggests H0 is **probably false** and H1 is **probably true**.
- **Interpretation:** We can report a definitive conclusion in favor of the research hypothesis.

| Decision | Implication |
|----------|-------------|
| **Retain H0** | H0 could be true (weak) |
| **Reject H0** | H0 is probably false; H1 is probably true (strong) |

### Why the Research Hypothesis Is Not Tested Directly

1. **Lacks precision:** A hypothesis test requires a single number for the sampling distribution. H0 supplies this (e.g., μ = 500); H1 typically only specifies an inequality (e.g., μ ≠ 500).
2. **Logical advantage:** Rejecting H0 provides **strong** support for H1. Retaining H0 provides only **weak** support for H0. Since we want strong support for our research hypothesis, we identify it with H1 and test H0 indirectly.

---

## 11.3 One-Tailed and Two-Tailed Tests

### Two-Tailed (Nondirectional) Test

- **H1:** μ ≠ some number
- Rejection regions in **both tails** of the sampling distribution.
- Critical z: **±1.96** (α = .05) or **±2.58** (α = .01).
- Use when we care about deviations in **either direction**.

### One-Tailed (Directional) Test

- **Lower tail critical:** H1: μ < some number → reject only if z is too far **below** the hypothesized mean.
- **Upper tail critical:** H1: μ > some number → reject only if z is too far **above** the hypothesized mean.
- Critical z: **±1.65** (α = .05) or **±2.33** (α = .01) in the relevant tail only.
- **Extra sensitivity:** One-tailed tests are more likely to detect a false H0 when the true effect is in the predicted direction.

### When to Use Which?

| Situation | Test Type |
|-----------|-----------|
| Concern only about deviations in **one** direction, with no interest in the other | One-tailed |
| Concern about deviations in **either** direction | Two-tailed (default) |

**Important:** Choose one- or two-tailed **before** collecting data. Never peek at the data to decide.

### Null Hypothesis for One-Tailed Tests

- **Lower tail critical (H1: μ < 500):** H0: μ ≥ 500
- **Upper tail critical (H1: μ > 500):** H0: μ ≤ 500

---

## 11.4 Choosing a Level of Significance (α)

- **α** = probability of rejecting a true H0 (Type I error).
- **α = .05** → reject H0 if observed z would occur by chance with probability ≤ .05.
- **Smaller α** (e.g., .01, .001) → lower risk of Type I error, but harder to reject H0.
- **Larger α** → easier to reject H0, but higher risk of false alarms.

### When to Use Different Levels

| Level | Use When |
|-------|----------|
| **.05** | Default; no special reason to change |
| **.01** | Rejecting a true H0 has serious consequences (e.g., costly new program) |
| **.001** | Rejecting a true H0 would have very serious consequences (e.g., dangerous treatment) |

---

## Critical z Values (Table 11.1)

| Level (α) | Two-Tailed | One-Tailed (Lower) | One-Tailed (Upper) |
|-----------|-----------|--------------------|--------------------|
| **.05** | ±1.96 | −1.65 | +1.65 |
| **.01** | ±2.58 | −2.33 | +2.33 |

---

## 11.5 Testing a Hypothesis About Vitamin C

### Setup

- **Research question:** Does vitamin C increase IQ?
- **Design:** 36 students take 90 mg vitamin C daily for 2 months; IQ tested.
- **Population:** IQ ~ N(100, 15).
- **H0:** μ ≤ 100 (vitamin C has no positive effect)
- **H1:** μ > 100 (vitamin C increases IQ)
- **Test:** One-tailed, upper tail critical; α = .05
- **Decision rule:** Reject H0 if z ≥ 1.65

### Note on Design

- A **control group** (placebo) would be better to rule out placebo effects.
- Two-group designs are covered in Chapters 14–15.

---

## 11.6 Four Possible Outcomes

| | **H0 True** | **H0 False** |
|---|-------------|--------------|
| **Retain H0** | (1) Correct decision | (3) Type II error (miss) |
| **Reject H0** | (2) Type I error (false alarm) | (4) Correct decision |

### Vitamin C Example

1. **Correct (retain true H0):** Conclude no evidence that vitamin C increases IQ when it doesn’t.
2. **Type I error:** Conclude vitamin C increases IQ when it doesn’t (false alarm).
3. **Type II error:** Conclude no evidence that vitamin C increases IQ when it does (miss).
4. **Correct (reject false H0):** Conclude vitamin C increases IQ when it does.

### Identifying Errors

- **Type I:** Rejecting a **true** H0.
- **Type II:** Retaining a **false** H0.
- First identify H0; then ask whether the decision matches the true state of H0.

---

## 11.7 If H0 Really Is True

- The **hypothesized** and **true** sampling distributions are the same.
- **Probability of Type I error** = α (e.g., .05).
- **Probability of correct decision** = 1 − α (e.g., .95).
- To reduce Type I error, use a **smaller** α (e.g., .01 or .001).

---

## 11.8 If H0 Really Is False (Large Effect)

- **Effect** = difference between true and hypothesized population means.
- **Large effect (e.g., 10 points):** True μ = 110, hypothesized μ = 100.
- **Hypothesized distribution:** Centered at 100 (used for decision rule).
- **True distribution:** Centered at 110 (where the observed mean actually comes from).
- **Probability of Type II error (β)** is low (e.g., .01).
- **Probability of correct decision (1 − β)** is high (e.g., .99).

---

## 11.9 If H0 Really Is False (Small Effect)

- **Small effect (e.g., 3 points):** True μ = 103, hypothesized μ = 100.
- True and hypothesized distributions are **closer together**.
- More of the true distribution falls in the **retention** region.
- **β** is higher (e.g., .67); **1 − β** is lower (e.g., .33).

**Rule:** The smaller the effect, the higher β and the lower the probability of correctly rejecting a false H0.

---

## 11.10 Influence of Sample Size

### Larger Sample Size

- **Standard error** decreases: σX̄ = σ/√n.
- Retention region shrinks toward the hypothesized mean.
- True sampling distribution becomes narrower.
- **Result:** Higher probability of detecting a false H0 (lower β, higher 1 − β).

### Sample Size Can Be Too Large

- Very large n → very small σX̄ → very sensitive test.
- May detect **trivially small** effects (e.g., ½-point IQ increase) that are not practically important.

### Sample Size Can Be Too Small

- Very small n → large σX̄ → insensitive test.
- May **miss** large, important effects (Type II error).

### Guideline

- Choose a sample size that is **neither unduly small nor excessively large**.
- **Power curves** help select an appropriate sample size.

---

## 11.11 Power and Sample Size

### Power

- **Power** = 1 − β = probability of **detecting** a particular effect when H0 is false.
- Power is the complement of the probability of a Type II error.

### Power Analysis

1. Specify the **smallest important effect** you want to detect.
2. Specify a **target power** (e.g., .80).
3. Use **power curves** or software (Minitab, G*Power, etc.) to find the required sample size.

### Reducing Required Sample Size

If the prescribed sample size is too large, it can be reduced by: enlarging the smallest important effect; lowering power (e.g., from .80 to .70); increasing α (e.g., from .05 to .10); using a one-tailed test if appropriate; or a combination of these. *Reference: Cohen, J. (1992). A power primer. Psychological Bulletin, 112, 155–159.*

### Power Curves

- Show how power varies with **effect size** for a fixed sample size.
- Example (vitamin C): For n = 29, power ≈ .80 for a 7-point effect; power ≈ .40 for a 4-point effect; power ≈ .95 for a 10-point effect.

### Reducing Required Sample Size

- Increase the smallest important effect.
- Lower the target power (e.g., from .80 to .70).
- Increase α (e.g., from .05 to .10).
- Use a one-tailed test instead of two-tailed (when appropriate).

### You Need Not Predict the True Effect

- Specify only the **smallest effect worth detecting**.
- If the true effect is **larger**, power will be **higher** than specified.
- If the true effect is **smaller**, you are less likely to detect it—which may be acceptable for unimportant effects.

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **Retain H0** | Weak decision; H0 could be true |
| **Reject H0** | Strong decision; H0 probably false |
| **One-tailed** | More sensitive in predicted direction; use only when justified in advance |
| **Two-tailed** | Default when direction is uncertain |
| **α** | Probability of Type I error; usually .05 |
| **β** | Probability of Type II error |
| **Power (1 − β)** | Probability of detecting an effect when H0 is false |
| **Effect size** | Larger effect → lower β, higher power |
| **Sample size** | Larger n → lower σX̄ → higher power |

---

## Important Terms

| Term | Definition |
|------|-------------|
| **Two-tailed (nondirectional) test** | Rejection regions in both tails |
| **One-tailed (directional) test** | Rejection region in one tail |
| **Type I error** | Rejecting a true H0 (false alarm) |
| **Type II error** | Retaining a false H0 (miss) |
| **Alpha (α)** | Probability of Type I error; level of significance |
| **Beta (β)** | Probability of Type II error |
| **Power (1 − β)** | Probability of detecting an effect when H0 is false |
| **Effect** | Difference between true and hypothesized population mean |
| **Hypothesized sampling distribution** | Centered at μhyp; used to construct decision rule |
| **True sampling distribution** | Centered at true μ; produces the observed mean |
| **Power curve** | Graph of power vs. effect size for fixed n |

---

## Quick Reference: Critical z Values

| α | Two-Tailed | One-Tailed |
|---|------------|------------|
| .05 | ±1.96 | ±1.65 |
| .01 | ±2.58 | ±2.33 |

---

## Next Chapter

**Chapter 12: Estimation** — Confidence intervals for estimating population parameters.

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
