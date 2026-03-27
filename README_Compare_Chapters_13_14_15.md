# Comparing Chapters 13, 14, and 15: Which *t* Test?

*Statistics, 11th Ed., Witte & Witte (Wiley, 2017)*

---

## At a glance

| | **Chapter 13** | **Chapter 14** | **Chapter 15** |
|---|----------------|----------------|----------------|
| **Name** | *t* test for **one sample** | *t* test for **two independent samples** | *t* test for **two related samples** |
| **Question** | Is one population mean equal to a value? | Do **two different groups** differ in mean? | Do **paired** measurements differ on average? |
| **Typical design** | One random sample from one population | Two separate groups (e.g., treatment vs. control) | Same people twice, or matched pairs |
| **Parameter** | Single mean $\mu$ | Difference $\mu_1 - \mu_2$ | Mean of differences $\mu_D$ |
| **Degrees of freedom** | $df = n - 1$ | $df = n_1 + n_2 - 2$ | $df = n - 1$ ( $n$ = number of **pairs** ) |

All three use Student’s *t* because the population standard deviation $\sigma$ is unknown and estimated from the data. The **sampling distribution**, **hypotheses**, and **formula for the standard error** change with the design.

---

## Chapter 13: One sample

**Use when** you have **one** sample and want to test a claim about **one** population mean—for example, whether the mean mileage of new cars meets a legal standard.

- You compare the sample mean $\bar{X}$ to a **hypothesized** value $\mu_{\text{hyp}}$.
- The *t* ratio uses the standard error of **one** mean: $s_{\bar{X}} = s/\sqrt{n}$.
- This is the direct replacement for the *z* test when $\sigma$ is unknown.

---

## Chapter 14: Two independent samples

**Use when** you have **two unrelated groups**—different people in each group, with no systematic pairing between a person in group 1 and a person in group 2.

- You test whether **$\mu_1 - \mu_2$** differs from a hypothesized difference (usually 0).
- Variability comes from **two** samples; the standard error is for **$\bar{X}_1 - \bar{X}_2$**, often using a **pooled variance** when equal variances are assumed.
- With random assignment, this design supports **cause–effect** language about a treatment versus a control.

---

## Chapter 15: Two related samples (repeated measures / matched pairs)

**Use when** each score in one condition is **linked** to a score in the other—most often the **same subjects** measured twice (before/after), or two subjects **matched** on a relevant variable.

- You work with **difference scores** $D = X_1 - X_2$ and test **$\mu_D$** (usually against 0).
- After differencing, the problem becomes a **one-sample *t* test on $D$**, so the structure mirrors Chapter 13, but the meaning is “change” or “pairwise difference” rather than a single raw mean.
- **Individual differences** are controlled because each pair contributes one difference; the test is often **more powerful** than the independent-samples *t* on the same kind of question, when pairing is justified.

---

## Chapter 14 vs. Chapter 15 (the usual confusion)

- **Independent (Ch. 14):** two separate groups; order of subjects does not pair across groups.
- **Related (Ch. 15):** each observation has a **partner** in the other condition; analysis is on **differences within pairs**.

If the data are **naturally paired** (same person, or matched pairs), Chapter 15 is appropriate. If the groups are **unrelated**, Chapter 14 is appropriate. Using the wrong chapter breaks the assumptions of the test and can misstate precision and conclusions.

---

## Quick decision guide

1. **One group, one mean vs. a standard?** → Chapter **13**.
2. **Two unrelated groups?** → Chapter **14**.
3. **Same subjects twice (or matched pairs)?** → Chapter **15**.

---

## Full chapter READMEs

- [README_Chapter13.md](README_Chapter13.md) — *t* Test for One Sample  
- [README_Chapter14.md](README_Chapter14.md) — *t* Test for Two Independent Samples  
- [README_Chapter15.md](README_Chapter15.md) — *t* Test for Two Related Samples  

---

*Source: Statistics, 11th Ed., Witte & Witte, Wiley 2017*
