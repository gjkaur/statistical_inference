# Chapter 18: Analysis of Variance (Two Factors) — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 18 introduces **two-factor ANOVA**—testing differences among population means when data are categorized by **two independent variables** (factors). The chapter covers **main effects**, **interaction**, three F tests, variance estimates, effect size (η²ₚ), **Tukey's HSD**, **simple effects** (Fse tests), assumptions, and reporting. Interaction—when the effect of one factor depends on the level of the other—often dominates interpretation.

---

## 18.1 A Two-Factor Experiment: Responsibility in Crowds

### Research Design (Bystander Effect)

- **Factor 1 (columns):** Crowd size (0, 2, or 4 people)
- **Factor 2 (rows):** Degree of danger (nondangerous vs. dangerous)
- **Dependent variable:** Delay in alarm reaction to smoke
- **Design:** 2 subjects per cell; 6 cells total (3 × 2)

### Types of Means

| Type | Description |
|------|-------------|
| **Column means** | Mean for each crowd size (ignoring danger) |
| **Row means** | Mean for each danger level (ignoring crowd size) |
| **Cell means** | Mean for each combination of factors |
| **Grand mean** | Overall mean for all subjects |

### Main Effects

- **Main effect of Factor A:** Effect of Factor A when Factor B is ignored (column or row means)
- **Main effect of Factor B:** Effect of Factor B when Factor A is ignored

---

## 18.2 Three F Tests

### Partitioning of Variability

**One-factor:** SStotal = SSbetween + SSwithin

**Two-factor:** SStotal = SScolumn + SSrow + SSinteraction + SSwithin

- **SScolumn** = variability between column means (main effect of Factor A)
- **SSrow** = variability between row means (main effect of Factor B)
- **SSinteraction** = remaining between-cell variability not explained by main effects
- **SSwithin** = variability within cells (error)

### Three F Ratios

| F Ratio | Numerator | Denominator | Tests |
|---------|-----------|-------------|-------|
| **Fcolumn** | MScolumn | MSwithin | Main effect of columns |
| **Frow** | MSrow | MSwithin | Main effect of rows |
| **Finteraction** | MSinteraction | MSwithin | Interaction |

### Smoke Alarm Example

- Fcolumn = 6.75* (crowd size)
- Frow = 36.02* (degree of danger)
- Finteraction = 5.25* (interaction)

---

## 18.3 Interaction

### Definition

**Interaction** occurs when the effect of one factor on the dependent variable is **not consistent** across all levels of the other factor.

- **Graphically:** Nonparallel lines in a line graph
- **Simple effects:** Effect of one factor at a single level of the other factor
- **Interaction** = product of **inconsistent simple effects**

### Visual Cues

| Pattern | Interpretation |
|---------|----------------|
| **Parallel lines** | No interaction |
| **Nonparallel, diverging** | Interaction |
| **Crossed lines** | Strong interaction |

### Importance

- Interaction often **dominates** interpretation
- When interaction is significant, main effects must be **qualified**
- Example: Crowd size affects reaction time for **nondangerous** but not **dangerous** conditions

---

## 18.4 Details: Variance Estimates

### Sums of Squares (Computation Formulas)

| Term | Formula |
|------|---------|
| **SStotal** | ΣX² − G²/N |
| **SSbetween** | Σ(T_cell²/n) − G²/N |
| **SSwithin** | ΣX² − Σ(T_cell²/n) |
| **SScolumn** | Σ(T_column²/rn) − G²/N |
| **SSrow** | Σ(T_row²/cn) − G²/N |
| **SSinteraction** | SSbetween − SScolumn − SSrow |

**Notation:** c = columns, r = rows, n = cell size, N = total scores

### Degrees of Freedom

| Term | Formula |
|------|---------|
| dftotal | N − 1 |
| dfcolumn | c − 1 |
| dfrow | r − 1 |
| dfinteraction | (c − 1)(r − 1) |
| dfwithin | N − (c)(r) |

**Check:** dftotal = dfcolumn + dfrow + dfinteraction + dfwithin

---

## 18.5 Details: Mean Squares and F Ratios

### Formulas

$$MS_{column} = \frac{SS_{column}}{df_{column}}, \quad F_{column} = \frac{MS_{column}}{MS_{within}}$$

$$MS_{row} = \frac{SS_{row}}{df_{row}}, \quad F_{row} = \frac{MS_{row}}{MS_{within}}$$

$$MS_{interaction} = \frac{SS_{interaction}}{df_{interaction}}, \quad F_{interaction} = \frac{MS_{interaction}}{MS_{within}}$$

### ANOVA Table Format

| Source | SS | df | MS | F |
|--------|-----|-----|-----|-----|
| Column | | | | Fcolumn |
| Row | | | | Frow |
| Interaction | | | | Finteraction |
| Within | | | MSwithin | |
| Total | | | | |

---

## 18.6 Table for the F Distribution

- Use Table C: **df numerator** (df for the effect) and **df denominator** (dfwithin)
- Fcolumn and Finteraction: df = (2, 6) → critical F = 5.14 (α = .05)
- Frow: df = (1, 6) → critical F = 5.99 (α = .05)

---

## 18.7 Estimating Effect Size

### Partial η² for Each Effect

$$\eta^2_{p(column)} = \frac{SS_{column}}{SS_{column} + SS_{within}}$$

$$\eta^2_{p(row)} = \frac{SS_{row}}{SS_{row} + SS_{within}}$$

$$\eta^2_{p(interaction)} = \frac{SS_{interaction}}{SS_{interaction} + SS_{within}}$$

- Each excludes the other two treatment components from the denominator
- Guidelines: small ≈ .01, medium ≈ .09, large ≈ .25

---

## 18.8 Multiple Comparisons

### Tukey's HSD (Two-Factor)

$$HSD = q \sqrt{\frac{MS_{within}}{n}}$$

- **For column means:** n = rn (total per column); use c and dfwithin for q
- **For row means:** n = cn (total per row); use r and dfwithin for q

### When to Use HSD

- **Only** when the main effect is significant **and** interpretation is **not** compromised by a significant interaction
- If interaction is significant → use **simple effects** instead

---

## 18.9 Simple Effects

### When to Use

- When **interaction is significant**
- To identify **which** simple effects are significant vs. nonsignificant

### Fse Test for Simple Effects

$$F_{se} = \frac{MS_{se}}{MS_{within}}$$

- **MSse** = mean square for variability among cell means in one row (or one column)
- **df numerator** = c − 1 or r − 1 (same as main effect)
- **df denominator** = dfwithin

### SS for Simple Effect

$$SS_{se} = \Sigma \frac{T^2_{se}}{n} - \frac{G^2_{se}}{N_{se}}$$

### Smoke Alarm Example

- **Crowd size at nondangerous:** Fse = 11.63* (significant)
- **Crowd size at dangerous:** Fse = 0.38 (nonsignificant)
- Conclusion: Reaction times increase with crowd size for **nondangerous** but not **dangerous** conditions

### HSD for Simple Effects

- If simple effect has >2 groups, use Tukey's HSD with **n = cell size**
- Cohen's d for significant pairs: d = (X̄₁ − X̄₂) / √MSwithin

---

## 18.10 Overview: Flow Chart for Two-Factor ANOVA

### Interaction (Left Panel)

1. **Significant Finteraction?** → Yes → Estimate η²ₚ; conduct **Fse tests** for simple effects
2. **Significant Fse?** → Yes → HSD test; estimate d for significant pairs

### Main Effects (Right Panel)

1. **Significant main effect?** → Yes, **and** not compromised by interaction → Estimate η²ₚ; HSD test; estimate d

---

## 18.11 Reports in the Literature

### Example Format

> Mean reaction times increase with crowd size [F(2, 6) = 6.75, MSE = 5.33, p < .05, η²ₚ = .69]; they are larger for nondangerous than dangerous conditions [F(1, 6) = 36.02, p < .01, η²ₚ = .86]; but these findings must be qualified because of the significant interaction [F(2, 6) = 5.25, p < .05, η²ₚ = .64]. An analysis of simple effects confirms that reaction times increase with crowd size for nondangerous conditions [Fse(2, 6) = 11.63, p < .01] but not for dangerous conditions [Fse(2, 6) = 0.38, ns].

---

## 18.12 Assumptions

- **Normality** and **equal variances** for each cell population
- **Equal cell sizes** preferred (unequal n complicates analysis and interpretation)
- Robust when cell sizes are equal and reasonably large (n ≥ ~10)

---

## 18.13 Other Types of ANOVA

- **Three-factor ANOVA:** Three factors, multiple 2-way interactions, one 3-way interaction
- **Mixed designs:** Repeated measures on one or more factors
- **Principle:** Use the **simplest** design that answers the research question

---

## Summary

| Topic | Key Point |
|-------|-----------|
| **Two factors** | Two independent variables |
| **Three F tests** | Column, row, interaction |
| **Interaction** | Effect of one factor depends on level of other |
| **Simple effects** | Effect of one factor at one level of the other |
| **When interaction significant** | Qualify main effects; use Fse tests |

---

## Important Terms

| Term | Definition |
|------|-------------|
| **Two-factor ANOVA** | ANOVA with two independent variables |
| **Main effect** | Effect of one factor when the other is ignored |
| **Interaction** | Effect of one factor depends on level of the other |
| **Simple effect** | Effect of one factor at a single level of the other |
| **Fse test** | Test for a simple effect |

---

## Key Equations

**Partitioning:**
- SStotal = SScolumn + SSrow + SSinteraction + SSwithin
- SSbetween = SScolumn + SSrow + SSinteraction

**F ratios:**
$$F_{column} = \frac{MS_{column}}{MS_{within}}, \quad F_{row} = \frac{MS_{row}}{MS_{within}}, \quad F_{interaction} = \frac{MS_{interaction}}{MS_{within}}$$

**Effect size:**
$$\eta^2_p = \frac{SS_{effect}}{SS_{effect} + SS_{within}}$$

**Tukey's HSD:**
$$HSD = q \sqrt{\frac{MS_{within}}{n}}$$

**Simple effect:**
$$F_{se} = \frac{MS_{se}}{MS_{within}}$$

---

## Quick Reference: Interpreting Results

| Result | Action |
|--------|--------|
| **Interaction significant** | Qualify main effects; conduct Fse tests |
| **Main effect significant, no interaction** | Report main effect; use HSD if >2 levels |
| **Simple effect significant** | Use HSD for pairwise comparisons; estimate d |

---

## Next Chapter

**Chapter 19: Chi-Square (χ²) Test for Qualitative (Nominal) Data** — Tests for categorical data (one-variable and two-variable χ² tests).

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
