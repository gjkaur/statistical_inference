# Comparing Chapters 16, 17, and 18: Which ANOVA?

*Statistics, 11th Ed., Witte & Witte (Wiley, 2017)*

---

## At a glance

| | **Chapter 16** | **Chapter 17** | **Chapter 18** |
|---|----------------|----------------|----------------|
| **Name** | One-factor ANOVA (**one-way**) | One-factor ANOVA (**repeated measures**) | **Two-factor** ANOVA |
| **Factors (IVs)** | **One** independent variable | **One** independent variable | **Two** independent variables |
| **Subjects** | **Different** people in each group | **Same** people in every condition | Typically **different** people per **cell** (independent groups factorial) |
| **Core *F* ratio(s)** | $F = MS_{\text{between}} / MS_{\text{within}}$ | $F = MS_{\text{between}} / MS_{\text{error}}$ | **Three** *F* tests: main A, main B, **interaction** (each vs. $MS_{\text{within}}$) |
| **Error term** | Variability **within** groups | Variability after removing **subject** differences (**$MS_{\text{error}}$**) | Variability **within** cells |

All three extend the logic of comparing means beyond two-group *t* tests: they use **mean squares**, the **F** distribution, and (often) **multiple comparisons** (e.g., Tukey’s HSD). The design—not the number of means alone—determines which chapter applies.

---

## Key formulas

**Mean square** (all chapters):

$$MS = \frac{SS}{df}$$

**Notation:** $N$ = total number of scores; $k$ = number of groups (Ch. 16–17) or levels of the repeated-measures factor (Ch. 17); in Ch. 17, $n$ = number of subjects (rows).

---

### Chapter 16 — one factor, independent groups

**Partition:**

$$SS_{\text{total}} = SS_{\text{between}} + SS_{\text{within}}$$

**Degrees of freedom:**

| Source | $df$ |
|--------|------|
| Between | $k - 1$ |
| Within | $N - k$ |

**Check:** $(N - 1) = (k - 1) + (N - k)$

***F* ratio:**

$$F = \frac{MS_{\text{between}}}{MS_{\text{within}}}$$

---

### Chapter 17 — one factor, repeated measures

**Partition:**

$$SS_{\text{total}} = SS_{\text{between}} + SS_{\text{subject}} + SS_{\text{error}}$$

with $SS_{\text{within}} = SS_{\text{subject}} + SS_{\text{error}}$ (same $SS_{\text{within}}$ as in Ch. 16).

**Degrees of freedom:**

| Source | $df$ |
|--------|------|
| Between | $k - 1$ |
| Subject | $n - 1$ |
| Error | $df_{\text{within}} - df_{\text{subject}}$ |

**Check:** $df_{\text{total}} = df_{\text{between}} + df_{\text{subject}} + df_{\text{error}}$

***F* ratio:**

$$F = \frac{MS_{\text{between}}}{MS_{\text{error}}}$$

---

### Chapter 18 — two factors (independent groups factorial)

**Partition:**

$$SS_{\text{total}} = SS_{\text{column}} + SS_{\text{row}} + SS_{\text{interaction}} + SS_{\text{within}}$$

**Degrees of freedom** ($c$ = columns, $r$ = rows):

| Source | $df$ |
|--------|------|
| Column (Factor A) | $c - 1$ |
| Row (Factor B) | $r - 1$ |
| Interaction | $(c - 1)(r - 1)$ |
| Within | $N - cr$ |

**Three *F* ratios** (each uses the same error mean square):

$$F_{\text{column}} = \frac{MS_{\text{column}}}{MS_{\text{within}}}, \qquad F_{\text{row}} = \frac{MS_{\text{row}}}{MS_{\text{within}}}, \qquad F_{\text{interaction}} = \frac{MS_{\text{interaction}}}{MS_{\text{within}}}$$

---

## Chapter 16: One factor, independent groups

**Use when** you have **one** categorical independent variable with **two or more levels**, and **different participants** are assigned to each level (between-subjects design).

- **$H_0$:** All level means are equal ($\mu_1 = \mu_2 = \ldots$). **$H_1$:** Not all are equal.
- Variability is split into **between groups** (treatment + error) and **within groups** (error only).
- **$F = MS_{\text{between}} / MS_{\text{within}}$** compares these two sources.
- This is the standard “one-way ANOVA” with **unrelated** groups.

---

## Chapter 17: One factor, repeated measures

**Use when** the **same subjects** are measured under **every** level of that **one** factor (or you have matched blocks analyzed equivalently).

- Hypotheses match Chapter 16 (equality of level means).
- **Within-subject** variability is partitioned: **$SS_{\text{within}} = SS_{\text{subject}} + SS_{\text{error}}$**. Individual differences are removed from the error term.
- **$F = MS_{\text{between}} / MS_{\text{error}}$** with **$MS_{\text{error}} < MS_{\text{within}}$** in the comparable design, so the test is often **more powerful** than Chapter 16.
- Practical constraints: **carryover** and **order** effects; **counterbalancing** and spacing conditions matter.

---

## Chapter 18: Two factors

**Use when** you cross **two** independent variables and want to test **main effects** (each factor, ignoring the other) and **interaction** (whether one factor’s effect **depends** on the level of the other).

- **Three *F* tests:** typically **Factor A**, **Factor B**, and **A × B interaction**, each with **$MS_{\text{within}}$** (error) in the denominator for the independent-groups factorial in the text.
- **Interaction** is often the key story: nonparallel profiles of cell means, or simple effects that differ across levels of the other factor.
- Not the same question as Chapters 16–17: you add a **second** way to classify conditions, not only “more levels of one thing.”

---

## Chapter 16 vs. Chapter 17

| Question | Chapter **16** | Chapter **17** |
|----------|----------------|----------------|
| Who is in each condition? | **Different** subjects per level | **Same** subjects at **all** levels |
| Error in the *F* ratio | **Within** groups | **Residual** after subjects (**error**) |
| Main tradeoff | Simpler logistics; individual differences stay in error | More power when pairing is valid; order/carryover risks |

Same **one** factor and the same omnibus hypotheses can justify **either** design; the **data layout** and **partitioning of sums of squares** decide between 16 and 17.

---

## Chapters 16–17 vs. Chapter 18

- **One factor (Ch. 16 or 17):** levels of a **single** IV (e.g., dosage 0 / 24 / 48 hours).
- **Two factors (Ch. 18):** a **grid** of conditions (e.g., crowd size × danger). You estimate **row** and **column** effects plus **interaction**, not just “which means differ” along one dimension.

---

## Quick decision guide

1. **One IV, different people in each group?** → Chapter **16**.
2. **One IV, same people in every group?** → Chapter **17**.
3. **Two IVs, factorial layout, testing mains and interaction?** → Chapter **18**.

---

## Full chapter READMEs

- [README_Chapter16.md](README_Chapter16.md) — Analysis of Variance (One Factor)  
- [README_Chapter17.md](README_Chapter17.md) — Analysis of Variance (Repeated Measures)  
- [README_Chapter18.md](README_Chapter18.md) — Analysis of Variance (Two Factors)  

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
