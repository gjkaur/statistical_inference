# Chapter 10: Introduction to Hypothesis Testing: The z Test — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 10 introduces **hypothesis testing**—using a sample to decide whether a claim about a population is supported. The **z test for a population mean** is the first hypothesis test. The chapter presents the step-by-step procedure: null and alternative hypotheses, decision rule, calculations, decision, and interpretation. The sampling distribution (Chapter 9) is the reference for deciding whether the observed result is common or rare.

---

## 10.1 Testing a Hypothesis About SAT Scores

### The Problem

- **Claim:** Mean SAT math score for local freshmen = national average of 500.
- **Data:** Random sample of 100 freshmen, sample mean **X̄ = 533**.
- **Question:** Is 533 different enough from 500 to conclude the population mean differs from 500?

### Hypothesized Sampling Distribution

- If the null hypothesis is true (**μ = 500**), the sampling distribution is centered at 500.
- **Standard error:** σ_X̄ = σ/√n = 110/√100 = **11** (same as σ divided by √n).
- **Shape:** Approximately normal (n = 100)

### Common vs. Rare Outcomes

| Outcome | Location | Action |
|---------|----------|--------|
| **Common** | Near center of sampling distribution | **Retain H₀** — difference could be due to chance |
| **Rare** | In the tails of sampling distribution | **Reject H₀** — difference unlikely due to chance alone |

### Boundaries

- Example: If X̄ is between 478 and 522 → common → retain H₀.
- If X̄ > 522 or X̄ < 478 → rare → reject H₀.
- Observed X̄ = 533 > 522 → **reject H₀** → mean probably exceeds 500.

---

## 10.2 z Test for a Population Mean

### Why Use z?

- Convert **X̄** to a **z score** so we can use the standard normal table.
- Same logic as before, but in standard units.
- **Hypothesized mean** (500) → z = 0; **σ_X̄** (11) → z = 1.

### z Formula

**Readable form:** z = (X̄ − μ_hyp) / σ_X̄, where σ_X̄ = σ/√n.

$$z = \frac{\bar{X} - \mu_{\text{hyp}}}{\sigma_{\bar{X}}} = \frac{\bar{X} - \mu_{\text{hyp}}}{\sigma/\sqrt{n}}$$

- **X̄** = observed sample mean  
- **μ_hyp** = hypothesized population mean (the μ in H₀)  
- **σ_X̄** = standard error = σ/√n  

### SAT Example

- X̄ = 533, μ_hyp = 500, σ_X̄ = 11  
- z = (533 − 500) / 11 = 33/11 = **3**  
- Critical z = ±1.96; observed z = 3 > 1.96 → **reject H₀**

### Assumptions of the z Test

1. **Normality** — Population is normal **or** n is large enough for the Central Limit Theorem.
2. **σ known** — Population standard deviation must be known.

*When σ is unknown, use the t test (Chapter 13).*

### Critical z Values (Table in Appendix C)

- **Two-tailed, α = .05:** z = ±1.96
- **Two-tailed, α = .01:** z = ±2.58
- **One-tailed, α = .05:** z = ±1.65
- **One-tailed, α = .01:** z = ±2.33

---

## 10.3 Step-by-Step Procedure

1. **State the research problem**
2. **Identify statistical hypotheses** (H₀ and H₁)
3. **Specify the decision rule**
4. **Calculate z**
5. **Make a decision** (retain or reject H₀)
6. **Interpret** the decision in context

---

## 10.4 Statement of the Research Problem

- Describe the question in words.
- Example: "Does the mean SAT math score for all local freshmen differ from the national average of 500?"

---

## 10.5 Null Hypothesis (H₀)

**The null hypothesis usually states that nothing special is happening in the population.**

- **Symbolic form:** H₀: μ = 500 (or some other specific value)
- **Role:** Provides the value **μ_hyp** at the center of the sampling distribution.
- **Scope:** Always about the **population**, not the sample.
- **Goal:** We typically hope to **reject** H₀ in favor of the research hypothesis.

### Finding the Number for H₀

- From another population (e.g., national average)
- From a theory or standard
- From past data or norms

---

## 10.6 Alternative Hypothesis (H₁)

**The alternative hypothesis is the opposite of the null hypothesis.**

- **Symbolic form:** H₁: μ ≠ 500 (two-tailed in this chapter)
- **Role:** What we conclude if we reject H₀.
- **Research hypothesis:** Usually identified with H₁; the idea that motivates the study.

### Relationship

- **Retain H₀** → No support for H₁
- **Reject H₀** → Support for H₁

---

## 10.7 Decision Rule

**The decision rule states exactly when to reject H₀.**

### Common Rule (α = .05, two-tailed)

- **Reject H₀** if z ≥ 1.96 or z ≤ −1.96
- **Retain H₀** if −1.96 < z < 1.96

### Critical z Scores

- **Critical z** = values that separate common from rare outcomes.
- For α = .05 (two-tailed): critical z = **±1.96**
- 2.5% of area in each tail; 95% in the middle.

### Level of Significance (α)

- **α** = proportion of area in the "rare" (rejection) region.
- **α = .05** → Reject H₀ if the observed result would occur by chance 5% of the time or less when H₀ is true.
- α is chosen before collecting data.

---

## 10.8 Calculations

1. **Standard error:** σ_X̄ = σ/√n  
2. **z ratio:** z = (X̄ − μ_hyp) / σ_X̄  

---

## 10.9 Decision

- **Reject H₀** if |z| ≥ critical z (e.g., 1.96)
- **Retain H₀** if |z| < critical z

### Quick Check

- Sketch the sampling distribution with rejection regions.
- Mark the observed z.
- If it falls in a rejection region → reject H₀.

---

## 10.10 Interpretation

### If H₀ Is Rejected

- Conclude that the population mean **probably differs** from the hypothesized value.
- **Direction:** If X̄ (or z) is in the upper tail → mean probably **exceeds** μ_hyp.  
  If in the lower tail → mean probably **is below** μ_hyp.

### If H₀ Is Retained

- Conclude there is **no evidence** that the population mean differs from the hypothesized value.
- This is a weak conclusion (failure to find a difference, not proof of no difference).

---

## Summary: Hypothesis Test Flow

1. **Research problem** → **H₀ and H₁** → **Decision rule** (α, critical z)
2. **Sample data** → **Compute z** → **Compare z to critical z**
3. **Reject H₀** or **retain H₀** → **Interpretation**

---

## Key Equation

**z ratio for a single population mean**

*Plain:* z = (X̄ − μ_hyp) / σ_X̄, with σ_X̄ = σ/√n.

$$z = \frac{\bar{X} - \mu_{\text{hyp}}}{\sigma_{\bar{X}}} = \frac{\bar{X} - \mu_{\text{hyp}}}{\sigma/\sqrt{n}}$$

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Null hypothesis (H₀) | Hypothesis that nothing special is happening; usually μ = some value |
| Alternative hypothesis (H₁) | Opposite of H₀; what we conclude if we reject H₀ |
| Research hypothesis | Informal hypothesis; usually same as H₁ |
| Decision rule | Rule specifying when to reject H₀ |
| Critical z score | z value that separates common from rare outcomes |
| Level of significance (α) | Proportion of area in rejection region; how rare an outcome must be to reject H₀ |
| z test for a population mean | Test of H₀ about μ using the z statistic |
| Hypothesized sampling distribution | Sampling distribution centered at μ_hyp |

---

## Quick Reference: z Test Checklist

1. State research problem  
2. H₀: μ = _____  
3. H₁: μ ≠ _____  
4. Decision rule: Reject H₀ if |z| ≥ 1.96 (α = .05)  
5. Standard error: σ_X̄ = σ/√n = _____  
6. z = (X̄ − μ_hyp) / σ_X̄ = _____  
7. Decision: Reject or retain H₀ because _____  
8. Interpretation: _____  

---

## Next Chapter

**Chapter 11: More About Hypothesis Testing** — One-tailed vs. two-tailed tests, Type I and Type II errors, power, sample size, and choosing α.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
