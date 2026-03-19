# Chapter 6: Describing Relationships: Correlation — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 6 introduces how to **describe relationships between pairs of variables**. Two variables are related when pairs of scores show a consistent pattern. Relationships are displayed with **scatterplots** and summarized with **correlation coefficients**. The main measure is the **Pearson r**, which describes the linear relationship between quantitative variables.

---

## 6.1 An Intuitive Approach

### Types of Relationships

| Type | Pattern | Example |
|------|---------|---------|
| **Positive** | High with high, low with low (similar relative positions) | Cards sent ↑ → cards received ↑ |
| **Negative** | High with low, low with high (opposite relative positions) | Heavy smoking ↑ → life expectancy ↓ |
| **Little or none** | No consistent pattern | Random pairing of scores |

### Key Idea

> Two variables are **positively related** if pairs tend to occupy similar relative positions (high with high, low with low).  
> Two variables are **negatively related** if pairs tend to occupy opposite relative positions (high with low, vice versa).

---

## 6.2 Scatterplots

**A scatterplot is a graph with a cluster of dots representing all pairs of (X, Y) scores.**

### Construction

- **X axis** — One variable (e.g., cards sent)
- **Y axis** — Other variable (e.g., cards received)
- **Each dot** — One pair of scores (X, Y)

### Interpreting the Slope

| Dot cluster slope | Relationship |
|-------------------|--------------|
| **Lower left → upper right** | Positive |
| **Upper left → lower right** | Negative |
| **No clear slope** | Little or no relationship |

### Strength of Relationship

- **Stronger** — Dots cluster more closely around a straight line
- **Weaker** — Dots are more spread out
- **Perfect** — All dots fall exactly on a line (rare in practice)

### Linear vs. Curvilinear

| Type | Description | Example |
|------|-------------|---------|
| **Linear** | Best described by a straight line | Height vs. weight |
| **Curvilinear** | Best described by a curved line | Age vs. physical strength (peaks in adulthood) |

---

## 6.3 A Correlation Coefficient for Quantitative Data: r

**A correlation coefficient is a number between –1 and 1 that describes the relationship between pairs of variables.**

### Pearson r — Key Properties

| Property | Interpretation |
|----------|----------------|
| **Sign** | Positive (+) or negative (–) relationship |
| **Magnitude** | Strength of the linear relationship |

### Scale of r

- **r = +1.00** — Perfect positive linear relationship
- **r = –1.00** — Perfect negative linear relationship  
- **r = 0** — No linear relationship
- **Closer to ±1** — Stronger relationship
- **Closer to 0** — Weaker relationship

### Verbal Descriptions (Cohen's Guidelines)

| r (approx.) | Strength | Example |
|-------------|----------|---------|
| ~.10 or less | Small/weak | r = .03 |
| ~.30 | Medium/moderate | r = .35 |
| ~.50 or more | Large/strong | r = .70 |

*Note: r = .50+ is often considered very strong in behavioral/educational research.*

### Important Cautions

1. **r is not a proportion** — r = .70 does NOT mean "70% of a perfect relationship."
2. **r is unit-free** — Same value regardless of units (inches vs. cm, etc.).
3. **Range restriction** — Limiting the range of X or Y tends to **lower** r (e.g., only tall students → weaker height–weight correlation).
4. **Correlation ≠ causation** — A correlation does not show cause and effect.

### Correlation and Causation

- **Correlation** — Two variables vary together.
- **Cause-effect** — One variable produces a change in the other.
- A correlation can reflect:
  - Simple cause-effect (X causes Y)
  - Reverse causation (Y causes X)
  - Common cause (Z causes both X and Y)
  - Chance
- **Experiments** are needed to establish causation.

---

## 6.4 Details: Computation Formula for r

### Formula

$$r = \frac{SP_{xy}}{\sqrt{SS_x \cdot SS_y}}$$

### Components

**Sum of Products (SPxy):**
$$SP_{xy} = \Sigma XY - \frac{(\Sigma X)(\Sigma Y)}{n}$$

**Sum of Squares for X:**
$$SS_x = \Sigma X^2 - \frac{(\Sigma X)^2}{n}$$

**Sum of Squares for Y:**
$$SS_y = \Sigma Y^2 - \frac{(\Sigma Y)^2}{n}$$

### Computational Steps

1. Find n, ΣX, ΣY
2. Find ΣXY (sum of X×Y for each pair)
3. Find ΣX², ΣY²
4. Compute SPxy, SSx, SSy
5. Substitute into r formula

---

## 6.5 Outliers Again

- **Outliers** in scatterplots are dots that fall far from the main cluster.
- They can **strongly affect** r:
  - An outlier that follows the trend can **increase** r
  - An outlier that contradicts the trend can **decrease** or **reverse** r
- **Strategy:** Report r both **with** and **without** outliers (unless there is a clear reason to exclude them, e.g., data error).

---

## 6.6 Other Types of Correlation Coefficients

The **Pearson r** formula can be adapted for other data types:

| Data Type | Coefficient Name | How |
|-----------|------------------|-----|
| **Ranked (ordinal)** | Spearman's rho | Use ranks in place of raw scores |
| **Quantitative + dichotomous** | Point biserial | Code two categories as 1 and 2 |
| **Two ordered qualitative** | Cramer's phi | Assign ordered codes (1, 2, 3, etc.) |

- Many software packages report all of these as "Pearson r."

---

## 6.7 Computer Output

### Correlation Matrix

- Table of correlations for **all pairs** of variables.
- **Diagonal** = 1.000 (each variable with itself)
- **Off-diagonal** = correlation between two different variables
- Matrix is **symmetric** (rXY = rYX)

### Reading Output

- **Pearson Correlation** — Value of r
- **Sig. (2-tailed)** or **p-value** — Statistical significance (smaller → more likely a real relationship)
- **N** — Number of pairs used

---

## Summary Table: Interpreting r

| r Value | Direction | Strength | Verbal |
|---------|-----------|----------|--------|
| +.80 | Positive | Strong | "Higher X tends to go with higher Y" |
| +.30 | Positive | Moderate | "Slight tendency for high with high" |
| .00 | None | None | "No linear relationship" |
| –.50 | Negative | Moderate–Strong | "Higher X tends to go with lower Y" |
| –.95 | Negative | Very strong | "Very consistent inverse relationship" |

---

## Key Equations

**Correlation Coefficient:**
$$r = \frac{SP_{xy}}{\sqrt{SS_x \cdot SS_y}}$$

**Sum of Products:**
$$SP_{xy} = \Sigma XY - \frac{(\Sigma X)(\Sigma Y)}{n}$$

**Sum of Squares:**
$$SS_x = \Sigma X^2 - \frac{(\Sigma X)^2}{n}$$
$$SS_y = \Sigma Y^2 - \frac{(\Sigma Y)^2}{n}$$

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Positive relationship | High with high, low with low |
| Negative relationship | High with low, low with high |
| Scatterplot | Graph of dots for all (X, Y) pairs |
| Linear relationship | Best described by a straight line |
| Curvilinear relationship | Best described by a curved line |
| Correlation coefficient | Number from –1 to 1 describing relationship |
| Pearson correlation coefficient (r) | Correlation for quantitative data |
| Correlation matrix | Table of correlations for all variable pairs |

---

## Quick Reference: Scatterplot → r

```
Slope: lower-left to upper-right  →  r > 0 (positive)
Slope: upper-left to lower-right  →  r < 0 (negative)
No slope                         →  r ≈ 0

Tight cluster around line        →  |r| close to 1
Spread-out dots                  →  |r| close to 0
```

---

## Next Chapter

**Chapter 7: Regression** — Using correlation for prediction, regression line, least squares, standard error of estimate, and r².

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
