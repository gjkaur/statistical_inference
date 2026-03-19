# Chapter 7: Regression — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 7 extends **correlation** (Chapter 6) to **prediction**. When two variables are correlated, one can be used to predict the other. The chapter covers the **least squares regression line**, **standard error of estimate**, **r²** (coefficient of determination), **multiple regression**, and **regression toward the mean**.

---

## 7.1 Two Rough Predictions

### Prediction 1: "Relatively Large Number"

- If X and Y are positively related, a high X suggests a high Y.
- Example: Sending many cards → expect to receive many cards.

### Prediction 2: "Between Two Values"

- Use nearby points on the scatterplot.
- Example: If Emma sends 11 cards (between Steve's 9 and Doris's 13), predict she'll receive between 14 and 18 cards (between their Y values).

*Limitation:* These methods use only a few data points.

---

## 7.2 A Regression Line

**The regression line is a straight line used to predict Y from X.**

- **Placement:** Passes through the main cluster of dots (a compromise when dots don't fall on a single line).
- **Predictive errors:** Vertical distances between actual Y and predicted Y′.
- **Goal:** Minimize total predictive error.

*Problem:* Sum of raw errors (Y − Y′) equals zero (positive and negative cancel). So we minimize **squared** errors instead.

---

## 7.3 Least Squares Regression Line

**The least squares regression line minimizes the sum of squared predictive errors.**

### Regression Equation

$$Y' = bX + a$$

- **Y′** = predicted value of Y
- **X** = known value of the predictor
- **b** = slope
- **a** = Y-intercept

### Formulas for b and a

**Slope:**
$$b = r \sqrt{\frac{SS_y}{SS_x}}$$

**Y-intercept:**
$$a = \bar{Y} - b\bar{X}$$

*All values come from the original correlation analysis (r, SSx, SSy, X̄, Ȳ).*

### Interpretation of b and a

- **b** — Change in predicted Y per 1-unit increase in X.
  - b < 1: predicted Y increases less than X
  - b > 1: predicted Y increases more than X
  - b < 0: negative relationship
- **a** — Predicted Y when X = 0.

### Example

For cards sent (X) and received (Y): Y′ = .80X + 6.40

- Each additional card sent → +0.80 cards received.
- Sending 0 cards → predicted 6.40 cards received.

---

## 7.4 Standard Error of Estimate (sy|x)

**The standard error of estimate is a rough measure of the average predictive error.**

### Interpretation

> sy|x is roughly the average amount by which actual Y values differ from their predicted Y′ values.

### Formulas

**Definition:**
$$s_{y|x} = \sqrt{\frac{SS_{y|x}}{n-2}} = \sqrt{\frac{\Sigma(Y - Y')^2}{n-2}}$$

**Computation (preferred):**
$$s_{y|x} = \sqrt{\frac{SS_y(1 - r^2)}{n-2}}$$

### Properties

- **r = 1** → sy|x = 0 (no predictive error)
- **r = 0** → sy|x is largest (no improvement over predicting Ȳ)
- **Stronger |r|** → smaller sy|x → better predictions

### Prediction Statement

Prediction = Y′ ± sy|x (e.g., "15.20 ± 3.10 cards")

---

## 7.5 Assumptions

### 1. Linearity

- The relationship between X and Y should be **linear**.
- Check: scatterplot should not show a clear curvilinear pattern.
- If curvilinear, use methods suited for non-linear relationships.

### 2. Homoscedasticity

- Variability of Y around the regression line should be **similar** at all levels of X.
- Dots should be dispersed similarly about the line along its length.
- If not (e.g., fan shape), use sy|x cautiously.

---

## 7.6 Interpretation of r²

**r² = proportion of total variability in Y that is predictable from X.**

### Formula

$$r^2 = \frac{SS_y - SS_{y|x}}{SS_y} = \frac{\text{SS explained by regression}}{SS_y}$$

### Interpretation

- **r² = .64** → 64% of the variability in Y is predictable from X.
- **1 − r²** → proportion of variability **not** predictable from X.

### Cohen's Guidelines for r²

| r²    | Strength |
|-------|----------|
| ~.01  | Weak     |
| ~.09  | Moderate |
| ~.25  | Strong   |

### Important Cautions

1. **r² applies to variability, not individual scores** — e.g., r² = .64 does not mean 64% of individuals are predicted perfectly.
2. **r² ≠ causation** — "predictable" or "explained" does not imply cause and effect.
3. **Large r² values are uncommon** in behavioral/educational research; r² > .25 is often notable.

---

## 7.7 Multiple Regression Equations

**Multiple regression uses more than one predictor variable** to predict Y.

### Example

$$Y' = .410(X_1) + .005(X_2) + .001(X_3) + 1.03$$

where X1 = high school GPA, X2 = IQ, X3 = SAT score.

### Properties

- Still a **least squares** equation (minimizes sum of squared errors).
- Has a **standard error of estimate**.
- More predictors → more accurate predictions (when predictors add information).
- Same concepts as simple regression, but with multiple X variables.

---

## 7.8 Regression Toward the Mean

**Regression toward the mean is the tendency for extreme scores to move toward the average on a later measurement.**

### Why It Occurs

- Extreme scores often combine:
  - **Stable component** (skill, ability)
  - **Chance component** (luck)
- On retest, the chance component often changes; extreme scores move toward the mean.

### Examples

- Top 5 on exam 1 → often not all in top 5 on exam 2
- Best stocks in one year → often not best the next year
- Very good landings → often followed by less good landings

### The Regression Fallacy

**The regression fallacy is treating regression toward the mean as if it were a real effect.**

- Example: Trainees praised after good landings did worse next time; reprimanded trainees did better. It was concluded that praise hurts and reprimands help. In reality, both groups were regressing toward the mean.
- **Avoiding the fallacy:** Use a **control group** that receives no feedback (or different feedback) so that regression toward the mean can be separated from the treatment effect.

### In Research

- Underachievers or extreme scorers often improve (or regress) without special intervention.
- Always include a control group when evaluating interventions for extreme groups.

---

## Summary Table: Key Formulas

| Component | Formula |
|-----------|---------|
| **Regression equation** | Y′ = bX + a |
| **Slope** | b = r√(SSy/SSx) |
| **Y-intercept** | a = Ȳ − bX̄ |
| **Standard error of estimate** | sy|x = √[SSy(1−r²)/(n−2)] |
| **r²** | Proportion of Y variability predictable from X |

---

## Key Equations

**Least Squares Regression:**
$$Y' = bX + a$$

**Slope:**
$$b = r \sqrt{\frac{SS_y}{SS_x}}$$

**Y-intercept:**
$$a = \bar{Y} - b\bar{X}$$

**Standard Error of Estimate:**
$$s_{y|x} = \sqrt{\frac{SS_y(1 - r^2)}{n-2}}$$

**r² Interpretation:**
$$r^2 = \frac{SS_y - SS_{y|x}}{SS_y}$$

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Least squares regression equation | Equation that minimizes sum of squared prediction errors |
| Standard error of estimate (sy\|x) | Rough average amount of predictive error |
| Squared correlation (r²) | Proportion of Y variability predictable from X |
| Multiple regression equation | Regression with more than one predictor |
| Regression toward the mean | Tendency for extreme scores to move toward the mean |
| Regression fallacy | Misinterpreting regression toward the mean as a real effect |

---

## Quick Reference: Prediction Workflow

```
1. Verify linear relationship (scatterplot)
2. Calculate r, SSx, SSy from correlation analysis
3. Find b = r√(SSy/SSx) and a = Ȳ − bX̄
4. Regression equation: Y′ = bX + a
5. For new X, substitute and solve for Y′
6. Report prediction as Y′ ± sy|x
7. Interpret r² as % of variability predictable from X
```

---

## Next Chapter

**Part 2: Inferential Statistics** begins with **Chapter 8: Populations, Samples, and Probability** — random sampling, random assignment, and probability rules.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
