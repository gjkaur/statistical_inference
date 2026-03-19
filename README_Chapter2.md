# Chapter 2: Describing Data with Tables and Graphs — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 2 introduces the core tools of **descriptive statistics**: tables (frequency distributions) and graphs. These tools help you organize data, detect patterns, and communicate information clearly. The chapter covers how to construct, interpret, and avoid common pitfalls when creating tables and graphs.

---

## Part 1: Tables (Frequency Distributions)

### 2.1 Frequency Distributions for Quantitative Data

A **frequency distribution** organizes observations by sorting them into classes and showing the **frequency (f)** of occurrence in each class.

#### Ungrouped Data
- Observations sorted into **classes of single values** (e.g., each weight value gets its own class).
- **Use when:** Fewer than ~20 possible values between the smallest and largest observations.
- **Example:** Film ratings on a 1–10 scale.

#### Grouped Data
- Observations sorted into **classes of more than one value** (e.g., 130–139, 140–149).
- **Use when:** 20 or more possible values—ungrouped would be too long and uninformative.
- **Example:** Weights ranging from 133 to 245 lbs grouped into 10-lb intervals.

---

### 2.2 Guidelines for Frequency Distributions

#### Essential Rules (Do Not Violate)

| Rule | Description | Example |
|------|-------------|---------|
| **1. Mutually exclusive** | Each observation in one, and only one, class | Use 130–139, 140–149 (not 130–140, 140–150) |
| **2. List all classes** | Include classes with zero frequency | Don't skip 210–219 just because f = 0 |
| **3. Equal intervals** | All class intervals same width | 130–139, 140–149, 150–159 (not 130–139, 140–159) |

#### Optional Rules

| Rule | Description |
|------|-------------|
| 4. Upper & lower boundaries | Avoid open-ended classes like "240–above" when possible |
| 5. Convenient intervals | Use 1, 2, 5, 10 or multiples (not 13, 17) |
| 6. Lower boundary = multiple of interval | 130, 140, 150 (not 135, 145) |
| 7. ~10 classes | Avoid too many (over-summarizing) or too few (masking patterns) |

#### Key Concepts

- **Unit of measurement** — Smallest possible difference between scores (e.g., 1 lb for weights rounded to nearest pound).
- **Real limits** — Midpoint of the gap between adjacent tabled boundaries. For 140–149, real limits are 139.5 and 149.5. Actual width = 10.
- **Gaps between classes** — Show that each score goes in exactly one class. Gap size = one unit of measurement.

#### Constructing a Frequency Distribution (Grouped Data)

1. Find **range** = largest − smallest.
2. **Class interval** = range ÷ desired number of classes (usually 10).
3. Round to convenient number (5, 10, etc.).
4. Start lowest class at a multiple of the interval (e.g., 130 if smallest is 133).
5. End lowest class: add interval, subtract 1 unit of measurement (e.g., 130 + 10 − 1 = 139).
6. List classes upward to include largest observation.
7. Tally observations into classes.
8. Replace tallies with frequencies (f); add total.

---

### 2.3 Outliers

**Outliers** are very extreme scores (e.g., GPA 0.06, IQ 170, summer wages $62,000).

| Action | When |
|--------|------|
| **Check accuracy** | Verify the value isn't a recording error (e.g., 3.06 → 0.06) |
| **Might exclude from summaries** | Use a footnote; avoid stretching class intervals to include them |
| **Might enhance understanding** | Study special circumstances that produced the outlier |

---

### 2.4 Relative Frequency Distributions

**Relative frequency** = frequency of each class as a fraction (or %) of the total.

- **Formula:** Relative f = f ÷ total f
- **Use when:** Comparing distributions with different total N (e.g., 500 vs. 300 million).
- **Proportions:** 0 to 1. **Percentages:** 0% to 100% (multiply proportion by 100).

---

### 2.5 Cumulative Frequency Distributions

**Cumulative frequency** = total observations in that class and all lower-ranked classes.

- **Construction:** Add each class frequency to the sum of all lower classes, working upward.
- **Cumulative percentage** = cumulative f ÷ total f × 100
- **Percentile rank** — Percentage of scores with equal or smaller values than a given score.
- **Use when:** Relative standing matters (e.g., test scores, aptitude).
- **Note:** Exact percentile ranks require ungrouped data; grouped data give **approximate** percentile ranks.

---

### 2.6 Frequency Distributions for Qualitative (Nominal) Data

- **Construction:** Count how often each category appears; report frequencies.
- **Order:** Arbitrary for nominal data (Yes/No). For **ordinal** data, preserve order (e.g., military ranks: General → Lieutenant).
- **Conversions:** Can create relative frequency and, for ordinal data, cumulative frequency/percentile ranks.

---

### 2.7 Interpreting Distributions Constructed by Others

When reviewing a distribution:

1. **Read the whole table** — Title, column headings, footnotes, source.
2. **Check construction** — Does it follow guidelines? Appropriate number of classes?
3. **Inspect content** — Range reasonable? Any outliers?
4. **Focus on shape** — Single peak or several? Balanced or lopsided?
5. **Stay open-minded** — Pursue questions that arise.

---

## Part 2: Graphs

### 2.8 Graphs for Quantitative Data

#### Histogram
- **Bar-type graph** for quantitative data.
- **Adjacent bars share boundaries** — Emphasizes continuity (continuous variables).
- **Axes:** X = class intervals; Y = frequency.
- **Origin** at (0, 0). Use **wiggly lines** for breaks in scale (e.g., between 0 and 130).

#### Frequency Polygon
- **Line graph** — Dots at midpoints of class intervals, connected by lines.
- **Anchored to horizontal axis** — Extend tails to midpoints of first unoccupied classes.
- **Use when:** Overlaying two or more distributions on the same graph.
- **Midpoint** = (lower boundary + upper boundary) ÷ 2

#### Stem and Leaf Display
- **Preserves individual scores** while showing distribution shape.
- **Stems** = leading digits (e.g., 13, 14, 15 for 130s, 140s, 150s).
- **Leaves** = trailing digits (e.g., 0, 3, 5 for 160, 163, 165).
- **Rotate 90°** — Silhouette resembles a histogram.
- **Flexible stems** — Can use 1, 10, 100, 0.1, etc., depending on data scale.

---

### 2.9 Typical Shapes

| Shape | Description | Example |
|-------|-------------|---------|
| **Normal** | Bell-shaped, symmetric | IQ scores, gestation periods |
| **Bimodal** | Two peaks | Ages in a neighborhood of new parents + infants |
| **Positively skewed** | Few extreme values to the **right** (positive direction) | U.S. family incomes; weights in Figure 2.1 |
| **Negatively skewed** | Few extreme values to the **left** (negative direction) | Ages at retirement |

**Tip:** Label skew by where the **few extreme observations** are, not where the majority are.

---

### 2.10 A Graph for Qualitative (Nominal) Data

#### Bar Graph
- **Gaps between bars** — Emphasizes discrete/categorical nature of data.
- **Use for:** Qualitative data; sometimes discrete quantitative data (e.g., number of children).
- **Contrast with histogram:** Histogram has no gaps (continuous data).

---

### 2.11 Misleading Graphs

Common distortions to avoid (and to spot in others' work):

| Trick | Problem |
|-------|---------|
| **Unequal bar widths** | Makes one category look larger than it is |
| **Omitted zero** | Exaggerates differences; use wiggly lines if scale is broken |
| **Exaggerated vertical axis** | Vertical axis much taller than horizontal → overstates differences |
| **Suppressed vertical axis** | Vertical axis too short → understates differences |

**Rule of thumb:** Vertical axis height ≈ horizontal axis width.

**Reference:** *How to Lie with Statistics* by Darrell Huff & Irving Geis.

---

### 2.12 Doing It Yourself

- Follow the **"Constructing Graphs"** step-by-step procedure (see box in text).
- Choose graph type: histogram or frequency polygon for quantitative; bar graph for qualitative.
- Depict data **clearly, concisely, and completely**.
- Avoid distortions described in Section 2.11.

---

## Constructing Graphs — Quick Steps

1. Choose graph type (histogram, frequency polygon, or bar graph).
2. Draw axes — vertical height ≈ horizontal width.
3. Identify class intervals for horizontal axis.
4. Place intervals along horizontal axis; use wiggly lines for scale breaks.
5. Scale vertical axis from 0 to max frequency (or slightly above).
6. Draw bars or dots/lines.
7. Add labels and title.

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Frequency distribution | Observations sorted into classes with frequency (f) shown |
| Frequency distribution for ungrouped data | Classes of single values |
| Frequency distribution for grouped data | Classes of multiple values |
| Unit of measurement | Smallest possible difference between scores |
| Real limits | Boundaries at midpoint of gaps between tabled boundaries |
| Outlier | Very extreme score |
| Relative frequency distribution | Frequency as fraction/percentage of total |
| Cumulative frequency distribution | Total in each class and all lower classes |
| Percentile rank | % of scores with equal or smaller values |
| Histogram | Bar graph for quantitative data; bars touch (continuous) |
| Frequency polygon | Line graph for quantitative data |
| Stem and leaf display | Display preserving individual scores via stems and leaves |
| Positively skewed distribution | Few extreme observations to the right |
| Negatively skewed distribution | Few extreme observations to the left |
| Bar graph | Bar graph for qualitative data; gaps between bars |

---

## Quick Reference: When to Use What

| Data Type | Table | Graph |
|-----------|------|-------|
| **Quantitative, <20 values** | Ungrouped frequency distribution | Histogram or frequency polygon |
| **Quantitative, ≥20 values** | Grouped frequency distribution | Histogram, frequency polygon, or stem and leaf |
| **Qualitative** | Frequency distribution by category | Bar graph |
| **Comparing distributions (different N)** | Relative frequency distribution | Frequency polygons on same graph |

---

## Next Chapter

**Chapter 3: Describing Data with Averages** — Mode, median, mean, and when to use each.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
