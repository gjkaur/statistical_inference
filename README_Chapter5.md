# Chapter 5: Normal Distributions and Standard (z) Scores — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 5 introduces the **normal curve** and **z scores**—tools for answering questions about any normal distribution. The normal curve describes many real-world distributions (IQ, heights, measurement errors, etc.) and is central to inferential statistics. Using the **standard normal table**, we can find proportions (areas) for any score or find scores for any proportion.

---

## 5.1 The Normal Curve

**The normal curve is a theoretical, symmetrical, bell-shaped curve defined for continuous variables.**

### Properties

- **Symmetrical** — Lower half is the mirror image of the upper half.
- **Bell-shaped** — Peaks at the midpoint, tapers gradually in both directions.
- **Tails extend infinitely** — Never actually touch the horizontal axis.
- **Mean = Median = Mode** — All three coincide at the center.

### Why Use the Normal Curve?

- Observed distributions (e.g., heights of 3091 men) have chance irregularities.
- The normal curve **smooths** these irregularities for more accurate generalizations.
- Many real distributions approximate the normal curve (IQ, heights, gestation periods, etc.).

### Key Facts

- **68%** of the area is within ±1 standard deviation of the mean.
- **95%** of the area is within ±2 standard deviations (more precisely, ±1.96).
- **5%** of the area is beyond ±2 standard deviations.

### Different Normal Curves

- Changing **μ** (mean) → shifts the curve left or right.
- Changing **σ** (standard deviation) → changes spread (taller/narrower vs. shorter/wider).
- All normal curves share the same mathematical structure; distances in **standard deviation units** have the same meaning.

---

## 5.2 z Scores

**A z score is a unit-free, standardized score that indicates how many standard deviations a score is above or below the mean.**

### Formula

$$z = \frac{X - \mu}{\sigma}$$

- **X** = original score  
- **μ** = population mean  
- **σ** = population standard deviation  

*For samples:* use X̄ and s instead of μ and σ.

### Interpretation

- **z = 0** → score equals the mean
- **z = 2.00** → score is 2 standard deviations **above** the mean
- **z = –1.27** → score is 1.27 standard deviations **below** the mean

### Properties

- **Unit-free** — Original units (inches, IQ points, etc.) cancel out.
- **Comparable across distributions** — A z of 1.5 means the same relative position in any normal distribution.

---

## 5.3 Standard Normal Curve

**The standard normal curve is the normal curve with mean = 0 and standard deviation = 1.**

- There are infinitely many normal curves (different μ and σ).
- There is **only one** standard normal curve.
- **Table A** (Appendix C) gives proportions for the standard normal curve.

### Converting to the Standard Normal Curve

- Converting any normal distribution to z scores produces the standard normal curve.
- Example: 66 inches (μ=69, σ=3) → z = (66−69)/3 = **–1.00**
- Same z = –1.00 for 1080 hours (bulbs), 90 IQ points, etc.—all one SD below their means.

### Using Table A

| Legend | Refers to | Columns |
|--------|-----------|---------|
| **Top** | Upper half (z ≥ 0) | A (z), B (between mean and z), C (beyond z) |
| **Bottom** | Lower half (z ≤ 0) | A′ (negative z), B′ (between mean and z), C′ (beyond z) |

**Key facts:**
- B + C (or B′ + C′) = .5000 for any z
- Total area under curve = 1.0000
- Areas are never negative

---

## 5.4 Solving Normal Curve Problems

Two main types:

| Type | Given | Find |
|------|-------|------|
| **Finding proportions** | Score(s) | Proportion (area) |
| **Finding scores** | Proportion (area) | Score(s) |

### General Approach

1. **Sketch** the normal curve and shade the target area.
2. **Plan** which table column(s) to use.
3. **Convert** (X → z or z → X).
4. **Look up** or compute the answer.

---

## 5.5 Finding Proportions

*Given a score (or scores), find the proportion of the distribution.*

### Step-by-Step

1. Sketch the curve; shade the target area.
2. Decide which column (B, C, B′, C′) gives the target area.
3. Convert X to z: \( z = \frac{X - \mu}{\sigma} \)
4. Look up z in Table A; read the proportion.

### Common Situations

| Target Area | Column to Use |
|-------------|---------------|
| Below a score (left tail) | C′ |
| Above a score (right tail) | C |
| Between mean and score (upper half) | B |
| Between mean and score (lower half) | B′ |
| Between two scores | Subtract two C′ (or C) values |
| Beyond two scores (both tails) | C + C′ (or 2 × C if symmetric) |

### Important Notes

- **Below vs. below or equal** — For continuous variables, the proportion is the same.
- **"More than X"** vs. **"Less than X"** — Check which tail is needed.
- **Between two scores** — Use (area below higher) − (area below lower). Do **not** subtract z scores.

---

## 5.6 Finding Scores

*Given a proportion (area), find the score(s).*

### Step-by-Step

1. Sketch the curve; draw a line for the target score on the correct side of the mean.
2. Plan which column to search (B, C, B′, or C′).
3. Find z by locating the desired proportion in the table; read the z score.
4. Convert z to X: **X = μ + (z)(σ)**

### Placing the Target Score

- **Area to left > .50** → target score is **above** the mean (use top legend, positive z).
- **Area to left < .50** → target score is **below** the mean (use bottom legend, negative z).

### Converting z to X

$$X = \mu + (z)(\sigma)$$

### Common z Values (Inferential Statistics)

- **z = ±1.96** → 2.5% in each tail; 95% in the middle
- **z = ±2.58** → 0.5% in each tail; 99% in the middle

---

## 5.7 More About z Scores

### z Scores for Non-Normal Distributions

- z scores can be computed for **any** distribution.
- The **shape** of the z-score distribution matches the original (e.g., skewed → skewed).
- z scores always have **mean = 0** and **standard deviation = 1**.
- **Table A applies only when the distribution is normal.**

### Interpreting Test Scores

- Raw scores alone are hard to interpret.
- z scores show **relative performance** (e.g., z = 1.80 → almost 2 SD above mean).
- **Reference group** matters—specify whose mean and SD are used.

### Transformed Standard Scores

- **Standard score** — Unit-free score expressed relative to a known mean and SD.
- **Transformed standard score** — Like z but with a different mean and SD (no negatives/decimals).

**Formula:**
$$z' = \text{desired mean} + (z)(\text{desired standard deviation})$$

### Common Transformations

| Scale | Mean | SD | Example |
|-------|------|-----|---------|
| **z** | 0 | 1 | –1.00 |
| **T score** | 50 | 10 | 40 |
| **IQ** | 100 | 15 | 85 |
| **GRE** | 500 | 100 | 400 |

- Transformations **do not change** relative standing or distribution shape.

---

## Summary: Doing Normal Curve Problems

### Finding Proportions

1. Sketch and shade target area.
2. Plan solution (which columns).
3. Convert X to z: \( z = \frac{X - \mu}{\sigma} \)
4. Enter Table A with z; read proportion.

### Finding Scores

1. Sketch; draw target score on correct side of mean.
2. Plan solution (which column to search).
3. Find z by locating proportion in B, C, B′, or C′.
4. Convert z to X: **X = μ + (z)(σ)**

---

## Key Equations

**z Score:**
$$z = \frac{X - \mu}{\sigma}$$

**Convert z to X:**
$$X = \mu + (z)(\sigma)$$

**Transformed Standard Score:**
$$z' = \text{desired mean} + (z)(\text{desired SD})$$

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Normal curve | Theoretical, symmetrical, bell-shaped curve |
| z score | Unit-free score in standard deviation units from the mean |
| Standard normal curve | Normal curve with μ=0, σ=1 |
| Standard score | Unit-free score relative to known mean and SD |
| Transformed standard score | Standard score with different mean/SD (e.g., T, IQ, GRE) |

---

## Quick Reference: Table A Columns

```
UPPER HALF (z ≥ 0)          LOWER HALF (z ≤ 0)
Col A: z score              Col A′: –z score
Col B: between mean and z   Col B′: between mean and –z
Col C: beyond z (right)     Col C′: beyond –z (left)

B + C = .5000    B′ + C′ = .5000
```

---

## Next Chapter

**Chapter 6: Describing Relationships: Correlation** — Scatterplots, correlation coefficient r, and measuring linear relationships.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
