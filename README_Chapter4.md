# Chapter 4: Describing Variability — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 4 introduces **measures of variability**—how spread out or scattered scores are in a distribution. Averages (Chapter 3) describe the center; variability describes the spread. The main measures are the **range**, **variance**, **standard deviation**, and **interquartile range**. The standard deviation is the most important and is central to inferential statistics.

---

## 4.1 Intuitive Approach

### Why Variability Matters

- Two distributions can have the **same mean** but **different variability**.
- **Less variability** → mean difference between groups is **more conspicuous** and **more statistically stable**.
- **More variability** → mean difference is **less conspicuous** and **less statistically stable** (could be due to chance).

*Analogy:* It's easier to hear a phone message when static (variability) is reduced.

---

## 4.2 Range

**The range is the difference between the largest and smallest scores.**

- **Formula:** Range = Largest score − Smallest score
- **Pros:** Easy to calculate and understand.
- **Cons:**
  - Uses only two scores (ignores the rest).
  - Tends to increase with sample size (larger groups more likely to include extremes).

---

## 4.3 Variance

**The variance is the mean of all squared deviation scores.**

### Steps to Understand Variance

1. **Deviation scores** — Subtract the mean from each score: (X − mean).
2. **Problem:** Sum of deviations from the mean always equals **zero** (positive and negative cancel).
3. **Solution:** Square each deviation to eliminate negative signs.
4. **Variance** — Add all squared deviations and divide by N (population) or n − 1 (sample).

### Mean Absolute Deviation (m.a.d.) — Alternative Not Preferred

- **Mean absolute deviation** = mean of |X − X̄| (sum absolute deviations, ignore signs, then divide by n).
- Can be used as a measure of variability, but is **not preferred** because ignoring negative signs has undesirable mathematical and statistical repercussions (e.g., less useful in advanced inference).
- The standard deviation (which squares deviations) is preferred.

### Weakness of Variance

- Units are **squared** (e.g., "squared pounds")—hard to interpret.
- Variance is mainly a stepping stone to the **standard deviation**.

---

## 4.4 Standard Deviation

**The standard deviation is the square root of the variance.**

- **Formula:** s = √variance (or σ = √variance for population)
- **Units:** Same as original data (e.g., pounds, points).

### Interpretation

> **The standard deviation is a rough measure of the average (or standard) amount by which scores deviate on either side of their mean.**

### Key Generalizations (Most Distributions)

| Rule | Description |
|------|-------------|
| **Majority within 1 SD** | A majority (often ~68%) of scores fall within one standard deviation on either side of the mean. |
| **Small minority beyond 2 SD** | A small minority (often ~5%) of scores deviate more than two standard deviations from the mean. |

**Examples:**
- IQ: mean = 105, s = 15 → majority between 90 and 120; few below 75 or above 135.
- Study hours: mean = 27, s = 10 → majority between 17 and 37; few below 7 or above 47.

### Standard Deviation vs. Mean

| Measure | Type | Description |
|---------|------|-------------|
| **Mean** | Position | A single location on the scale |
| **Standard deviation** | Distance | No fixed location; used to measure distance from the mean (e.g., X + 2s, X − ½s) |

### Properties

- **Never negative** — Squaring eliminates negative signs.
- **Usually exceeds mean absolute deviation** — But "average deviation" is a reasonable approximation.

---

## 4.5 Details: Standard Deviation

### Sum of Squares (SS)

**SS** = sum of all squared deviation scores. Required before calculating variance and standard deviation.

#### Definition Formula (easier to understand)

**Population:** SS = Σ(X − μ)²  
**Sample:** SS = Σ(X − X̄)²

#### Computation Formula (more efficient for calculation)

**Population:** SS = ΣX² − (ΣX)²/N  
**Sample:** SS = ΣX² − (ΣX)²/n

### Population vs. Sample Formulas

| Measure | Population | Sample |
|---------|------------|--------|
| **Variance** | σ² = SS/N | s² = SS/(n − 1) |
| **Standard deviation** | σ = √(SS/N) | s = √(SS/(n − 1)) |

**Critical difference:** Sample formulas divide by **n − 1**, not n.

### Computational Check

- Standard deviation should typically be **less than half** the range (often ⅓ to ⅙ of the range).
- Use this to spot large calculation errors.

---

## 4.6 Degrees of Freedom (df)

**Degrees of freedom = the number of values that are free to vary, given one or more mathematical restrictions.**

### Why n − 1 for Sample Variance?

- When using the **sample mean** (X̄) to compute deviations, the sum of deviations **must equal zero**.
- Given n deviations, once you know n − 1 of them, the last one is **fixed** by this restriction.
- So only **n − 1** deviations provide independent information about variability.
- Dividing by n would **underestimate** population variability; dividing by n − 1 gives a better estimate.

### Formula

**df = n − 1** (when estimating variance/standard deviation from a sample)

### Alternative Formulas Using df

$$s^2 = \frac{SS}{df} \quad \text{and} \quad s = \sqrt{\frac{SS}{df}}$$

where df = n − 1.

---

## 4.7 Interquartile Range (IQR)

**The IQR is the range for the middle 50% of the scores.**

- **Formula:** IQR = Third quartile (Q3) − First quartile (Q1)
- **Q3** = 75th percentile (top quarter removed)
- **Q1** = 25th percentile (bottom quarter removed)

### Finding the IQR

1. Order scores from least to most.
2. **Steps to penetrate:** (n + 1) ÷ 4 (round if needed).
3. From the **largest** score, count that many steps in → value at that position = Q3.
4. From the **smallest** score, count that many steps in → value at that position = Q1.
5. IQR = Q3 − Q1.

### Key Property: Resistant to Outliers

- IQR **ignores** the top 25% and bottom 25%.
- Extreme scores (outliers) do **not** affect the IQR.
- **Use with:** Median (both resist outliers).

---

## 4.8 Measures of Variability for Qualitative and Ranked Data

### Qualitative (Nominal) Data

- No standard numeric measure of variability.
- Describe informally:
  - **Maximum variability** — Scores evenly divided among classes (heterogeneous).
  - **Minimum variability** — Scores concentrated in one class (homogeneous).
  - **Intermediate** — Uneven division among several classes.

### Ordered Qualitative and Ranked Data

- Describe variability by identifying **extreme scores or ranks** (e.g., "ranks range from lieutenant to general").

---

## Summary Table: Measures of Variability

| Measure | Definition | Pros | Cons |
|---------|-------------|------|------|
| **Range** | Largest − smallest | Simple | Uses only 2 scores; increases with n |
| **Mean absolute deviation (m.a.d.)** | Mean of absolute deviations from mean | Intuitive "average deviation" | Not preferred; limited use in inference |
| **Variance** | Mean of squared deviations | Foundation for SD | Squared units; hard to interpret |
| **Standard deviation** | √Variance | Same units as data; key for inference | Sensitive to outliers |
| **IQR** | Q3 − Q1 | Resistant to outliers | Ignores half the data |

---

## Key Equations

### Sum of Squares
**Definition:** SS = Σ(X − X̄)²  
**Computation:** SS = ΣX² − (ΣX)²/n

### Variance
**Population:** σ² = SS/N  
**Sample:** s² = SS/(n − 1) = SS/df

### Standard Deviation
**Population:** σ = √(SS/N)  
**Sample:** s = √(SS/(n − 1)) = √(SS/df)

### Degrees of Freedom
**df = n − 1** (for sample variance and standard deviation)

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Measures of variability | Descriptions of how dispersed or scattered scores are |
| Range | Difference between largest and smallest scores |
| Variance | Mean of all squared deviation scores |
| Sum of squares (SS) | Sum of all squared deviation scores |
| Standard deviation | Rough average amount scores deviate from the mean |
| Population standard deviation (σ) | SD for a population |
| Sample standard deviation (s) | SD for a sample; uses n − 1 |
| Degrees of freedom (df) | Number of values free to vary given restrictions |
| Interquartile range (IQR) | Range for middle 50% of scores |

---

## Quick Reference: Calculation Steps

```
1. Find the mean (X̄ or μ)
2. Find deviation scores: (X − mean)
3. Square each deviation: (X − mean)²
4. Sum squared deviations → SS
   (Or use computation formula: SS = ΣX² − (ΣX)²/n)
5. Variance: σ² = SS/N  OR  s² = SS/(n−1)
6. Standard deviation: σ = √σ²  OR  s = √s²
```

---

## Next Chapter

**Chapter 5: Normal Distributions and Standard (z) Scores** — The normal curve, z scores, and solving normal curve problems.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
