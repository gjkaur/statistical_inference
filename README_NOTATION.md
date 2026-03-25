# Notation and Formula Conventions

*These chapter READMEs use consistent mathematical notation aligned with *Statistics*, 11th Ed., Witte & Witte (Wiley, 2017).*

---

## Hypotheses

| Symbol | Meaning |
|--------|---------|
| $H_0$ | Null hypothesis |
| $H_1$ | Alternative hypothesis |

Chapter READMEs use **$H_0$** and **$H_1$** in Markdown; Unicode **H₀** / **H₁** may still appear in copied textbook phrases or tables in a few places.

---

## Population and sample

| Symbol | Meaning |
|--------|---------|
| $\mu$, $N$, $\sigma$, $\sigma^2$ | Population mean, size, standard deviation, variance |
| $\bar{X}$, $n$, $s$, $s^2$ | Sample mean, size, standard deviation, variance |
| $\mu_{\text{hyp}}$ | Hypothesized population mean (in hypothesis tests) |

---

## Standard errors and sampling distributions

| Symbol | Meaning |
|--------|---------|
| $\sigma_{\bar{X}} = \sigma/\sqrt{n}$ | Standard error of the mean (σ known) |
| $s_{\bar{X}} = s/\sqrt{n}$ | Estimated standard error of the mean (σ unknown) |
| $s_{\bar{X}_1 - \bar{X}_2}$ | Estimated standard error of the difference between two sample means |

---

## Test statistics and confidence

| Symbol | Meaning |
|--------|---------|
| $z_{\text{conf}}$, $t_{\text{conf}}$ | Critical $z$ or $t$ for a stated confidence level (from tables) |
| $\alpha$ | Level of significance; probability of Type I error |
| $\beta$ | Probability of Type II error |
| df | Degrees of freedom |

---

## Greek letters (common)

| Letter | Typical use |
|--------|-------------|
| $\mu$ (mu) | Population mean |
| $\sigma$ (sigma) | Population standard deviation |
| $\chi^2$ (chi-square) | Chi-square test statistic |
| $\eta^2$, $\eta^2_p$ | Eta-squared; partial eta-squared (effect size in ANOVA) |
| $\phi_c^2$ | Squared Cramer's phi (effect size for χ²) |
| $\rho$ (rho) | Population correlation coefficient |

---

## Display formulas

- **Block math** uses `$$ ... $$` on their own lines (fractions and big expressions).
- **Inline math** uses `$ ... $` where a renderer supports it.
- Subscripts and superscripts follow standard LaTeX (e.g., $\bar{X}_1$, $s_p^2$, $\mu_{\text{hyp}}$).

### Readability (with or without a math renderer)

Many Markdown previews **do not** render `$...$`. For that reason, chapter READMEs use:

- **Unicode in prose:** μ, σ, α, X̄, H₀, H₁, ≤, ≥, ±, √ — so the text stays readable everywhere.
- **Plain “readable form” lines** before or after important `$$` blocks (e.g. *z = (X̄ − μ_hyp) / σ_X̄*).
- **μ_hyp** in plain text means the hypothesized μ from H₀ (same idea as $\mu_{\text{hyp}}$ in LaTeX).
- **σ_X̄** means standard error of the mean, σ/√n.

---

## Where math renders

- **GitHub** renders `$...$` and `$$...$$` in Markdown (native math support).
- **VS Code** with a Markdown math extension (e.g. “Markdown+Math”) can preview the same syntax.
- **Default Markdown preview** often shows **raw** `$...$` — use the Unicode + plain lines above, or enable a math-capable preview.

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
