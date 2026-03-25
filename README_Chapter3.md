# Chapter 3: Describing Data with Averages — Statistics (Witte & Witte, 11th Ed.)

## Overview

Chapter 3 introduces **measures of central tendency**—averages that describe the middle or typical value of a distribution. The three main averages are the **mode**, **median**, and **mean**. Each has specific uses; the mean is the most important for both descriptive and inferential statistics.

---

## 3.1 Mode

**The mode is the value of the most frequently occurring score.**

- **Interpretation:** The most prevalent or typical value.
- **Finding it:** With organized data (e.g., frequency distribution), identify the class with the highest frequency. The **mode = the value**, not the frequency.
- **Example:** If 7 presidents served 4-year terms (more than any other term), the mode = **4 years**, not 7.

### Multiple Modes

| Term | Description |
|------|-------------|
| **Bimodal** | Two obvious peaks (e.g., weights of males + females combined) |
| **Multimodal** | More than two peaks |
| **No mode** | All values occur with equal frequency |

Multiple modes can indicate different subgroups in the data.

---

## 3.2 Median

**The median is the middle value when observations are ordered from least to most.**

- **Interpretation:** Splits the distribution into upper and lower halves; has a percentile rank of 50.
- **Requirement:** Scores must be ordered before finding the median.

### Finding the Median

| Step | Action |
|------|--------|
| 1 | Order scores from least to most |
| 2 | Find middle position: (n + 1) ÷ 2 |
| 3a | **If odd n:** Median = value at the middle position |
| 3b | **If even n:** Median = average of the two middlemost values |

**Examples:**
- **5 scores:** 2, 2, 6, 7, 8 → middle position = (5+1)/2 = 3 → median = **6**
- **6 scores:** 1, 3, 3, 8, 8, 9 → middle positions = 3rd and 4th → median = (3+8)/2 = **5.5**

---

## 3.3 Mean

**The mean is found by adding all scores and dividing by the number of scores.**

### Formulas

**Sample mean:**
$$\bar{X} = \frac{\sum X}{n}$$

- **$\bar{X}$** (X-bar) = sample mean  
- **$\sum X$** = sum of all scores  
- **$n$** = sample size  

**Population mean:**
$$\mu = \frac{\sum X}{N}$$

- **$\mu$** (mu) = population mean  
- **$N$** = population size  

*Greek symbols ($\mu$, $\sigma$) = population; English ($\bar{X}$, $s$) = sample.*

### Key Properties

1. **Balance point** — The mean is the point where the distribution would balance if it were a physical object. The sum of all deviations from the mean equals **zero**.
2. **Uses all scores** — Unlike the mode (most frequent) or median (middle), the mean reflects every value.
3. **Sensitive to outliers** — One extreme score can pull the mean substantially.

---

## 3.4 Which Average?

### When the Distribution Is Not Skewed

- Mode, median, and mean are **similar**.
- Any of the three can describe central tendency.

### When the Distribution Is Skewed

- The three averages **differ**.
- The **mean is most affected** by extreme scores.

| Skew Type | Mean vs. Median | Cause |
|-----------|-----------------|-------|
| **Positively skewed** | Mean **>** median | Few large values (e.g., income, infant death rates) |
| **Negatively skewed** | Median **>** mean | Few small values (e.g., retirement ages) |

### Guidelines

| Situation | Preferred Average |
|-----------|-------------------|
| Skewed distribution | Report **both** mean and median |
| Need typical/most common value | Mode |
| Need middle-ranked value | Median |
| Need balance point; later statistics | **Mean** (preferred for quantitative data) |

### Special Status of the Mean

- Used almost exclusively in later chapters.
- Key component of the **standard deviation** (Chapter 4).
- Central to **inferential statistics** (Part 2).

### Using the Word "Average"

- **Conventionally**, "average" usually means **mean** (e.g., grade point average).
- For controversial or unclear contexts, **specify** which average (mode, median, or mean) is being used.

---

## 3.5 Averages for Qualitative and Ranked Data

### Qualitative Data

| Average | Appropriate? | Notes |
|---------|--------------|-------|
| **Mode** | ✅ Always | Most frequent category (e.g., Yes, PG, White) |
| **Median** | ✅ If ordinal | Only when data can be ordered (e.g., military ranks) |
| **Mean** | ❌ Never | Words cannot be added and divided |

### Finding the Median for Ordered Qualitative Data

1. Convert to relative frequencies (percentages).
2. Cumulate from bottom to top.
3. Find the class where cumulative % first reaches or exceeds 50%.
4. That class is the **median class**.

**Caution:** Do not assume classes have equal frequencies. Use cumulative percentages to find the true 50th percentile.

### Ranked Data

- **Median** — Preferred; find the middlemost rank (or average of two middlemost).
- **Mode** — Less informative.
- **Mean** — Less informative; not typically used.

---

## Summary Table: The Three Averages

| Average | Definition | Best For | Sensitive to Outliers? |
|---------|------------|----------|------------------------|
| **Mode** | Most frequent value | Typical value; qualitative data | No |
| **Median** | Middle value (50th percentile) | Skewed distributions; ranked data | No |
| **Mean** | Sum ÷ n (balance point) | Quantitative data; later statistics | Yes |

---

## Important Terms (Glossary)

| Term | Definition |
|------|------------|
| Measures of central tendency | Numbers that describe the middle or typical value |
| Mode | Value of the most frequently occurring score |
| Bimodal | Distribution with two obvious peaks |
| Median | Middle value when observations are ordered |
| Sample | Subset of scores |
| Population | Complete set of scores |
| Sample mean ($\bar{X}$) | Balance point for a sample; $\sum X \div n$ |
| Population mean ($\mu$) | Balance point for a population; $\sum X \div N$ |
| Sample size ($n$) | Number of scores in sample |
| Population size ($N$) | Number of scores in population |

---

## Key Equations

**Sample Mean:**
$$\bar{X} = \frac{\sum X}{n}$$

**Population Mean:**
$$\mu = \frac{\sum X}{N}$$

---

## Quick Reference: Choosing an Average

```
                    DATA TYPE
                         |
        ┌────────────────┼────────────────┐
        |                |                |
   QUALITATIVE       RANKED         QUANTITATIVE
        |                |                |
   Mode only      Median preferred   All three possible
   (Median if     (Mode & mean      Mean preferred
    ordinal)       less useful)      for most analyses
```

---

## Next Chapter

**Chapter 4: Describing Variability** — Range, variance, standard deviation, and degrees of freedom.

---

*Source: Statistics, 11th Edition by Robert S. Witte & John S. Witte (Wiley, 2017)*
