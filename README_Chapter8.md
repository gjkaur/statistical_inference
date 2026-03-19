# Chapter 8: Populations, Samples, and Probability — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 8 begins **Part 2: Inferential Statistics**—generalizing beyond observed data. It covers **populations vs. samples**, **random sampling** (surveys), **random assignment** (experiments), **tables of random numbers**, and **probability** (definition, addition rule, multiplication rule). These concepts are the basis for hypothesis testing and confidence intervals in later chapters.

---

## Part 1: Populations and Samples

### 8.1 Populations

**A population is any complete set of observations (or potential observations).**

#### Real Populations

- All potential observations are **accessible** at the time of sampling.
- Examples: attitudes of students at a university, ages of Disneyland visitors on a given day, presidential preferences of registered U.S. voters.
- Pollsters (e.g., Gallup) typically work with real populations.

#### Hypothetical Populations

- Not all potential observations are accessible.
- Examples: "all lab rats that could undergo this experiment," "all student volunteers who could participate."
- Common in experiments where subjects come from small, convenient pools.
- **Generalizations to hypothetical populations are provisional**—based on researcher judgment, not strict statistical necessity.

---

### 8.2 Samples

**A sample is any subset of observations from a population.**

- Sample size is usually small relative to the population.
- Example: Bureau of Labor Statistics surveys <1% of U.S. worksites to estimate unemployment.
- **Optimal sample size** depends on variability, acceptable error, and other factors (discussed in Section 11.11).

---

### 8.3 Random Sampling

**Random sampling occurs when, at each stage of sampling, every remaining member of the population has an equal chance of being selected.**

- **Randomness** describes the **selection process**, not the pattern of observations in the sample.
- Random sampling does **not guarantee** that the sample will be representative; it only makes it more likely.
- **Casual or haphazard sampling is NOT random**—e.g., interviewing only students who enter the student union excludes others and can introduce bias.

---

### 8.4 Tables of Random Numbers

**Tables of random numbers** (e.g., Table H in Appendix C) provide digits 0–9 with equal likelihood.

#### How Many Digits?

- Use enough digits to cover the population size.
- Population of 679 → use 3-digit numbers 001–679 (ignore 680–999).
- Population of 3041 pages × 480 lines → use 6-digit numbers (e.g., first 4 digits = page, last 3 = line).

#### Procedure

1. Enter the table at an arbitrary point (e.g., blind pencil stab).
2. Read in a consistent direction (e.g., left to right, row by row).
3. Include a person/number when its ID appears; skip numbers outside the range and repeats.
4. Continue until the desired sample size is reached.

#### When No Directory Exists

- **Random digit dialing** — Randomly select area code + exchange + last 4 digits. (Limitations: wireless numbers, high nonresponse.)
- **Multi-stage sampling** — Randomly select regions → precincts → households (e.g., Gallup).

#### Hypothetical Populations

- **Cannot** take true random samples from hypothetical populations (some observations are not accessible).
- Researchers often treat convenience samples as if they were random and use inferential statistics—**random assignment** in experiments partly compensates for this.

---

### 8.5 Random Assignment of Subjects

**Random assignment ensures that each subject has an equal chance of being assigned to any group in an experiment.**

#### Why It Matters

- **Chance determines group membership** → basis for calculating probabilities of observed differences.
- **Groups are initially similar** (except for random variation) on uncontrolled variables (IQ, motivation, etc.).
- **Clearer cause-effect conclusions** — Observed differences (after accounting for chance) can be attributed to the independent variable.

#### How to Assign

- **Coin flip** — Heads = treatment, tails = control.
- **Random numbers** — Odd = treatment, even = control (or similar rule).
- **Equal group sizes** — Assign in pairs: first random number → group A or B; second subject automatically goes to the other group.

---

### 8.6 Surveys or Experiments?

| Context | Goal | Use |
|---------|------|-----|
| **Survey** | Random sample from a real population | Random **sampling** — all population members have equal chance of being selected |
| **Experiment** | Equivalent groups at the outset | Random **assignment** — all subjects have equal chance of being in each group |

- Use random numbers in a way that matches the goal (sampling vs. assignment).
- For equal group sizes in experiments, add restrictions (e.g., alternate assignment) while keeping the process random.

---

## Part 2: Probability

### 8.7 Definition

**Probability = the proportion or fraction of times that a particular event is likely to occur.**

- **Range:** 0 (impossible) to 1 (certain).
- **Sum of probabilities** for all outcomes = 1.
- **Ways to determine probability:**
  - **Speculation** — e.g., fair coin → P(heads) = .50.
  - **Observation** — e.g., long-run frequency of an event.
  - **Mixture** — e.g., normal curve superimposed on observed data.

---

### 8.8 Addition Rule

**Use when events are connected by "or" and are mutually exclusive.**

**Mutually exclusive** — Events cannot occur together (e.g., a person cannot be both 73 and 74 inches tall).

**Formula:**
$$\text{Pr}(A \text{ or } B) = \text{Pr}(A) + \text{Pr}(B)$$

**Example:** P(height ≥ 73") = P(73) + P(74) + P(75) + P(76+) = .05 + .03 + .02 + .02 = .12

#### When Events Are NOT Mutually Exclusive

- They can occur together.
- **Adjust for overlap:** Pr(A or B) = Pr(A) + Pr(B) − Pr(A and B).
- Example: P(senior or psych major) = P(senior) + P(psych) − P(senior and psych).

---

### 8.9 Multiplication Rule

**Use when events are connected by "and" and are independent.**

**Independent** — The occurrence of one event does not affect the probability of the other (e.g., two coin tosses, two randomly selected men).

**Formula:**
$$\text{Pr}(A \text{ and } B) = \text{Pr}(A) \times \text{Pr}(B)$$

**Example:** P(both men ≥ 73") = P(first ≥ 73) × P(second ≥ 73) = (.12)(.12) = .0144

#### When Events Are Dependent

- The occurrence of one affects the probability of the other.
- **Use conditional probability:** Pr(A and B) = Pr(A) × Pr(B | A).
- **Pr(B | A)** = probability of B given that A has occurred.

**Example:** P(senior and psych) = P(senior) × P(psych | senior) = (.20)(.50) = .10  
(not P(senior) × P(psych) = .14, which ignores dependency)

#### Conditional Probability

- **Pr(B | A)** = proportion of times B occurs when A has occurred.
- **Frequency approach:** Convert to frequencies (e.g., 100 people), solve, then convert back to probability.

---

### 8.10 Probability and Statistics

**Probability is central to inferential statistics.**

- Observed results (e.g., mean difference) are evaluated in the context of **all possible results** that could occur by chance.
- **Null hypothesis** — Provisional assumption that chance alone can account for the result.
- **Probabilities** are assigned to the observed result using theoretical distributions (e.g., normal curve).

#### Common vs. Rare Outcomes

| Outcome | Probability | Interpretation |
|---------|-------------|----------------|
| **Common** | ~95% of area (e.g., between z = ±1.96) | Nothing special; result could be due to chance → **not statistically significant** |
| **Rare** | ~5% of area (e.g., beyond z = ±1.96) | Something special; result unlikely due to chance alone → **statistically significant** |

- **z = ±1.96** → 2.5% in each tail; 5% total in the "rare" region.
- **z = ±2.58** → 0.5% in each tail; 1% total in the "rare" region.

---

## Summary Table: Surveys vs. Experiments

| Aspect | Survey | Experiment |
|--------|--------|------------|
| **Randomization** | Random sampling | Random assignment |
| **Goal** | Representative sample | Equivalent groups |
| **Generalization** | From sample to population | Whether group difference is real |
| **Population** | Usually real | Often hypothetical |

---

## Key Equations

**Addition Rule (mutually exclusive events):**
$$\text{Pr}(A \text{ or } B) = \text{Pr}(A) + \text{Pr}(B)$$

**Multiplication Rule (independent events):**
$$\text{Pr}(A \text{ and } B) = \text{Pr}(A) \times \text{Pr}(B)$$

**Multiplication Rule (dependent events):**
$$\text{Pr}(A \text{ and } B) = \text{Pr}(A) \times \text{Pr}(B|A)$$

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Population | Complete set of observations or potential observations |
| Sample | Subset of observations from a population |
| Random sampling | Process where all population members have equal chance of selection |
| Random assignment | Process where all subjects have equal chance of being in any group |
| Probability | Proportion of times an event is likely to occur |
| Mutually exclusive events | Events that cannot occur together |
| Addition rule | Add probabilities for "or" with mutually exclusive events |
| Independent events | One event does not affect the probability of the other |
| Multiplication rule | Multiply probabilities for "and" with independent events |
| Conditional probability | Probability of one event given that another has occurred |

---

## Quick Reference: Probability Rules

```
"OR" → Addition Rule
  - Mutually exclusive: Pr(A or B) = Pr(A) + Pr(B)
  - Not mutually exclusive: Pr(A or B) = Pr(A) + Pr(B) − Pr(A and B)

"AND" → Multiplication Rule
  - Independent: Pr(A and B) = Pr(A) × Pr(B)
  - Dependent: Pr(A and B) = Pr(A) × Pr(B|A)
```

---

## Next Chapter

**Chapter 9: Sampling Distribution of the Mean** — What happens when we take many samples; mean and standard error of the sampling distribution; Central Limit Theorem.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
