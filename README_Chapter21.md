# Chapter 21: Postscript: Which Test? — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 21 is a **postscript**—a concise summary and decision guide for selecting the appropriate statistical test. It synthesizes the main themes of the book and provides a flowchart (Figure 21.1) to help you choose the right test for any given research situation. This chapter serves as a practical reference for simple statistical analyses and a point of departure for more complex analyses.

---

## 21.1 Descriptive or Inferential Statistics?

### Descriptive Statistics

- **Intent:** Summarize existing data only (no generalization)
- **When:** You wish to describe or communicate information about current observations
- **Tools:** Tables, graphs, means, medians, standard deviations, correlations
- **Example:** A marriage counselor reports the mean (or median, if outliers exist) number of years of marital relationships for current clients in a group

### Inferential Statistics

- **Intent:** Generalize beyond existing data
- **When:** You wish to estimate or test hypotheses about a broader population
- **Tools:** Confidence intervals, hypothesis tests
- **Example:** Using the same mean to estimate—with a confidence interval—the mean years of marital relationships among all couples who seek professional help

---

## 21.2 Hypothesis Tests or Confidence Intervals?

- **Traditional preference:** Hypothesis tests are often preferred in the behavioral sciences
- **Best practice:** If the null hypothesis is rejected, **always** estimate effect size using:
  - Confidence intervals
  - Other effect size estimates: **d**, **η²**, or **$\phi_c^2$** (Cramer's phi squared)
- **Figure 21.1** reflects a preference for hypothesis tests but emphasizes the importance of effect size estimation

---

## 21.3 Quantitative or Qualitative Data?

The **first decision** when selecting a hypothesis test: Are observations **quantitative** or **qualitative**?

### Quantitative Data

- **Definition:** Numbers that reflect an **amount** or a **count**
- **Measurement level:** Interval/ratio
- **Appropriate tests:** t tests, F tests, or their **nonparametric counterparts** (U, T, H)

### Qualitative Data

- **Definition:** Words or codes that reflect **classes** or **categories**
- **Measurement level:** Nominal or ordinal
- **Appropriate tests:** **One-variable χ²** or **two-variable χ²**

### One- or Two-Variable χ²?

| Situation | Test |
|-----------|------|
| One variable only (e.g., gender: female vs. male) | **One-variable χ²** |
| Two variables cross-classified (e.g., gender × marital status of parents) | **Two-variable χ²** |

---

## 21.4 Distinguishing Between the Two Types of Data

When unsure whether data are quantitative or qualitative, use these guidelines:

### 1. Focusing on a Single Observation

- **Quantitative:** An observation represents an **amount** or **count**, expressed numerically
- **Qualitative:** An observation represents a **class** or **category**, described by a word or code

### 2. Focusing on Numerical Summaries

- **Quantitative:** Means and standard deviations are specified
- **Qualitative:** Only **frequencies** are specified

### 3. Focusing on Key Words

- **Quantitative:** Look for words like *scores*, *means*, *amounts*
- **Qualitative:** Absence of such terms often indicates qualitative data

### 4. If All Else Fails

- Visualize a single observation: Is it a meaningful number (quantitative) or a word/code (qualitative)?

---

## 21.5 One, Two, or More Groups?

Given **quantitative** data and no serious assumption violations, the key issue is the **number of groups**.

### One Group

- **Test:** t test for a **single population mean** (Ch. 13)
- **Example:** Does the mean years of marital relationships among clients differ from 7 years?

### Two Groups — Independent Samples

- **Test:** t test for **two population means** (independent samples) (Ch. 14)
- **Example:** Do clients have significantly fewer mean years of marriage than nonclients? (No pairing)

### Two Groups — Related Samples

- **Mean difference?** → t test for **two population means** (related samples) (Ch. 15)
- **Correlation?** → t test for **population correlation coefficient** (Ch. 15)
- **Example (mean difference):** Each client paired with a nonclient; test mean difference in marital years
- **Example (correlation):** Test correlation between years of courtship and years of marriage

### More Than Two Groups — Repeated Measures

- **Test:** **F test for repeated-measures ANOVA** (Ch. 17)
- **Example:** Same clients measured at three times (initial meeting, final meeting, six months later)

### More Than Two Groups — One Factor

- **Test:** **F test for one-factor ANOVA** (Ch. 16)
- **Example:** Mean years of marriage compared across three ethnic groups (African-American, Asian-American, Hispanic)

### More Than Two Groups — Two Factors

- **Test:** **F test for two-factor ANOVA** (Ch. 18)
- **Example:** Mean years of marriage evaluated by ethnic background **and** gender

---

## 21.6 Concluding Comments

### Nonparametric Tests (U, T, H)

- **Use only when:** An assumption is **seriously violated** or original observations are **ranked**
- **Caveat:** Less powerful than t and F tests—less likely to detect an effect when one exists

### Figure 21.1

- Serves as the primary guide for selecting the appropriate hypothesis test
- Also appears inside the back cover of the textbook for quick reference

---

## Flow Chart: Guidelines for Selecting the Appropriate Hypothesis Test

```
TYPE OF DATA
[Are observations numbers?]
    │
    ├── YES (QUANTITATIVE) ──────────────────────────────────────────────┐
    │         │                                                          │
    │         └── NUMBER OF GROUPS                                        │
    │                   │                                                │
    │                   ├── ONE ──────────────► t for one sample (Ch. 13)│
    │                   │                                                │
    │                   ├── TWO ──────────────► [Are quantitative        │
    │                   │       observations paired?]                    │
    │                   │            │                                    │
    │                   │            ├── NO ──► INDEPENDENT SAMPLES       │
    │                   │            │           t for two independent    │
    │                   │            │           samples (Ch. 14)          │
    │                   │            │           [If violated: Mann-      │
    │                   │            │            Whitney U (Ch. 20)]      │
    │                   │            │                                    │
    │                   │            └── YES ──► [Mean difference or     │
    │                   │                         relationship?]           │
    │                   │                          │                      │
    │                   │                          ├── DIFFERENCE ──►    │
    │                   │                          │   t for two related   │
    │                   │                          │   samples (Ch. 15)    │
    │                   │                          │   [If violated:       │
    │                   │                          │   Wilcoxon T (Ch. 20)]│
    │                   │                          │                      │
    │                   │                          └── RELATIONSHIP ──►   │
    │                   │                              t for correlation  │
    │                   │                              coefficient (Ch.15)│
    │                   │                                                │
    │                   └── THREE+ ──────────────► [Multiple observations  │
    │                             for same subject?]                      │
    │                                    │                                │
    │                                    ├── NO ──► [Two factors?]        │
    │                                    │            │                  │
    │                                    │            ├── NO ──► One-     │
    │                                    │            │         Factor F  │
    │                                    │            │         (Ch. 16)  │
    │                                    │            │         [If viol: │
    │                                    │            │         Kruskal-  │
    │                                    │            │         Wallis H] │
    │                                    │            │                  │
    │                                    │            └── YES ──► Two-    │
    │                                    │                      Factor F  │
    │                                    │                      (Ch. 18)  │
    │                                    │                                │
    │                                    └── YES ──► Repeated-measures    │
    │                                               F Test (Ch. 17)        │
    │                                                                     │
    └── NO (QUALITATIVE) ────────────────────────────────────────────────┘
              │
              └── [Are observations cross-classified?]
                        │
                        ├── NO ──► One-Variable χ² Test (Ch. 19)
                        │
                        └── YES ──► Two-Variable χ² Test (Ch. 19)
```

---

## Summary: Test Selection by Design

| Design | Parametric Test | Nonparametric Alternative |
|--------|-----------------|---------------------------|
| One sample (mean) | t (Ch. 13) | — |
| Two independent samples | t (Ch. 14) | Mann-Whitney U (Ch. 20) |
| Two related samples (mean diff.) | t (Ch. 15) | Wilcoxon T (Ch. 20) |
| Correlation (ρ) | t (Ch. 15) | — |
| One factor, 3+ groups | F (Ch. 16) | Kruskal-Wallis H (Ch. 20) |
| Repeated measures | F (Ch. 17) | — |
| Two factors | F (Ch. 18) | — |
| One qualitative variable | — | One-variable χ² (Ch. 19) |
| Two qualitative variables | — | Two-variable χ² (Ch. 19) |

---

## Important Terms

| Term | Definition |
|------|------------|
| **Descriptive statistics** | Summarizing existing data; no generalization |
| **Inferential statistics** | Generalizing beyond existing data |
| **Quantitative data** | Numbers reflecting amount or count (interval/ratio) |
| **Qualitative data** | Words or codes reflecting classes (nominal/ordinal) |
| **Figure 21.1** | Flowchart for selecting the appropriate hypothesis test |

---

## Quick Reference: Decision Checklist

1. **Descriptive or inferential?** → Descriptive: tables, graphs, means, etc. | Inferential: CI or hypothesis test
2. **Hypothesis test or CI?** → If test, also report effect size ($d$, $\eta^2$, $\phi_c^2$)
3. **Quantitative or qualitative?** → Quantitative: t/F (or U/T/H) | Qualitative: χ²
4. **Number of groups?** → One: t | Two: t (independent/related/correlation) | Three+: F
5. **Assumptions violated or ranked data?** → Use nonparametric: U, T, or H

---

## Sample Review Question Answers (from text)

| Question | Appropriate Test |
|----------|------------------|
| 21.1 | Two-variable χ² (attitudes: increased/same/decreased × gender) |
| 21.2 | t for two independent samples (spending estimates: quantitative) |
| 21.3 | t for two related samples (before/after speed reading) |
| 21.5 | One-variable χ² (district distribution: N/E/S/W) |
| 21.6 | One-factor F (dosage: 0, 4, 8 g) |
| 21.9 | Two-factor F (group size × structure) |
| 21.10 | t for two independent samples (bilingual vs. traditional program) |
| 21.11 | t for correlation coefficient (comprehension × months of education) |

---

## Next Steps

Chapter 21 concludes the main text. For further study:

- **Appendices:** Math review (A), answers to selected questions (B), tables (C), glossary (D)
- **More advanced topics:** Consult a more advanced statistics text or a statistician
- **Online resources:** Many statistics websites offer additional decision aids and tutorials

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
