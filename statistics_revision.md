# 📊 Statistics One-Shot Revision: Central Tendency & Dispersion

> **Purpose:** Quick but complete revision before exams/interviews. Everything you need, nothing you don't.

---

## PART 1 — MEASURES OF CENTRAL TENDENCY

> A single value that represents the **"center"** or **"typical value"** of a dataset.

---

### 1.1 — MEAN (Arithmetic Mean)

The **sum of all values divided by the number of values**.

**Formula:**

$$\bar{x} = \frac{\sum_{i=1}^{n} x_i}{n}$$

**Example:**
Data: 4, 8, 6, 5, 3, 2, 8, 9, 2, 5
Sum = 52, n = 10
**Mean = 52 / 10 = 5.2**

**Key Properties:**
- Uses **every value** in the dataset.
- Affected heavily by **outliers/extreme values**.
- The sum of deviations from the mean is always **zero**: `Σ(xᵢ - x̄) = 0`
- Best used for **normally distributed, symmetric data**.

**Types of Mean:**

| Type | Formula | When to Use |
|------|---------|-------------|
| Arithmetic Mean | Σx / n | General average |
| Weighted Mean | Σ(wᵢxᵢ) / Σwᵢ | When values have different importance |
| Geometric Mean | (x₁ · x₂ · ... · xₙ)^(1/n) | Growth rates, ratios |
| Harmonic Mean | n / Σ(1/xᵢ) | Speeds, rates |

**Weighted Mean Example:**
Marks: 80 (weight 3), 70 (weight 2), 90 (weight 5)
Weighted Mean = (80×3 + 70×2 + 90×5) / (3+2+5) = (240+140+450)/10 = **83**

---

### 1.2 — MEDIAN

The **middle value** when data is sorted in ascending or descending order.

**Formula:**
- If n is **odd**: Median = value at position `(n+1)/2`
- If n is **even**: Median = average of values at positions `n/2` and `(n/2)+1`

**Example (Odd n):**
Data (sorted): 2, 3, 5, **7**, 8, 9, 11 → n=7
Position = (7+1)/2 = 4th value → **Median = 7**

**Example (Even n):**
Data (sorted): 2, 4, **6, 8**, 10, 12 → n=6
Average of 3rd and 4th = (6+8)/2 = **Median = 7**

**Key Properties:**
- **Not affected by outliers** — this is its biggest advantage.
- Divides the distribution into **two equal halves**.
- Best used for **skewed data** or data with outliers (e.g., income distribution).
- For grouped data, use the formula:

$$\text{Median} = L + \left(\frac{\frac{n}{2} - CF}{f}\right) \times h$$

Where:
- L = lower boundary of median class
- CF = cumulative frequency before median class
- f = frequency of median class
- h = class width

---

### 1.3 — MODE

The value that **appears most frequently** in the dataset.

**Example:**
Data: 2, 3, 4, **4**, 5, **4**, 6, 7, **4**
**Mode = 4** (appears 3 times)

**Types:**
- **Unimodal** — one mode: {1, 2, **3**, 3, 4}
- **Bimodal** — two modes: {1, **2**, 2, 3, **4**, 4, 5}
- **Multimodal** — more than two modes
- **No Mode** — all values appear equally: {1, 2, 3, 4, 5}

**Key Properties:**
- The **only measure** that can be used for **nominal/categorical data** (e.g., most common eye color).
- Not affected by extreme values.
- A dataset can have **no mode or multiple modes**.

**For Grouped Data (Modal Class Formula):**

$$\text{Mode} = L + \left(\frac{f_1 - f_0}{2f_1 - f_0 - f_2}\right) \times h$$

Where:
- L = lower boundary of modal class
- f₁ = frequency of modal class
- f₀ = frequency of class before modal class
- f₂ = frequency of class after modal class
- h = class width

---

### 1.4 — RELATIONSHIP BETWEEN MEAN, MEDIAN & MODE

**Karl Pearson's Empirical Relationship** (for moderately skewed distributions):

```
Mode = 3(Median) - 2(Mean)
```

**Symmetrical Distribution:**
```
Mean = Median = Mode
```

**Positively Skewed (Right Skewed):**
```
Mode < Median < Mean
```
(Long tail on the right; mean gets pulled up by high values)

**Negatively Skewed (Left Skewed):**
```
Mean < Median < Mode
```
(Long tail on the left; mean gets pulled down by low values)

---

### 1.5 — WHEN TO USE WHICH MEASURE?

| Situation | Best Measure |
|-----------|-------------|
| Symmetric, no outliers | Mean |
| Skewed data, outliers present | Median |
| Categorical/nominal data | Mode |
| Income, house prices | Median |
| Average temperature | Mean |
| Most popular shoe size | Mode |
| Open-ended distributions | Median |

---

## PART 2 — MEASURES OF DISPERSION

> Dispersion tells us **how spread out** the data is around the central value. Two datasets can have the same mean but very different spreads.

**Example:** Dataset A: {5, 5, 5, 5, 5} and Dataset B: {1, 3, 5, 7, 9} — both have Mean = 5, but B is far more spread out.

---

### 2.1 — RANGE

The **simplest** measure of dispersion.

**Formula:**
```
Range = Maximum Value - Minimum Value
```

**Example:**
Data: 3, 7, 2, 9, 4, 11, 1
Range = 11 - 1 = **10**

**Key Properties:**
- Extremely **easy to compute**.
- Only uses **two values** (max and min), ignores everything in between.
- Highly **sensitive to outliers**.
- Not suitable for open-ended frequency distributions.

---

### 2.2 — INTERQUARTILE RANGE (IQR)

The range of the **middle 50%** of data. Removes the effect of outliers.

**Formula:**
```
IQR = Q3 - Q1
```

**Quartiles:**
- Q1 (25th percentile) = median of the lower half
- Q2 (50th percentile) = median (middle value)
- Q3 (75th percentile) = median of the upper half

**Example:**
Data (sorted): 1, 3, 5, 7, 9, 11, 13, 15, 17
Q1 = 5, Q2 = 9, Q3 = 13
**IQR = 13 - 5 = 8**

**Key Properties:**
- **Robust to outliers** — that's the whole point.
- Used in **box plots**.
- **Outlier Rule:** Any value below `Q1 - 1.5×IQR` or above `Q3 + 1.5×IQR` is considered an outlier.

---

### 2.3 — MEAN DEVIATION (Average Absolute Deviation)

The **average of absolute deviations** from the mean (or median).

**Formula (from Mean):**

$$MD = \frac{\sum |x_i - \bar{x}|}{n}$$

**Example:**
Data: 2, 4, 6, 8, 10 → Mean = 6
Deviations: |2-6|, |4-6|, |6-6|, |8-6|, |10-6| = 4, 2, 0, 2, 4
Sum = 12
**MD = 12 / 5 = 2.4**

**Key Properties:**
- Takes all values into account.
- Uses absolute values (no negatives cancel out).
- Less mathematically convenient than variance (absolute value is hard to work with algebraically).
- Mean deviation from **median** is minimum compared to any other point.

---

### 2.4 — VARIANCE

The **average of squared deviations** from the mean.

**Population Variance:**

$$\sigma^2 = \frac{\sum_{i=1}^{N}(x_i - \mu)^2}{N}$$

**Sample Variance** (uses n-1 to correct for bias — Bessel's correction):

$$s^2 = \frac{\sum_{i=1}^{n}(x_i - \bar{x})^2}{n-1}$$

**Example:**
Data: 2, 4, 4, 4, 5, 5, 7, 9 → Mean = 5
Squared deviations: 9, 1, 1, 1, 0, 0, 4, 16 → Sum = 32
**Population Variance = 32/8 = 4**
**Sample Variance = 32/7 ≈ 4.57**

**Key Properties:**
- Always **non-negative** (squares eliminate negatives).
- **Units are squared** — if data is in kg, variance is in kg². This is a limitation.
- Gives **more weight to outliers** due to squaring.
- Why n-1 for sample? Because using n underestimates the true population variance (degrees of freedom concept).

**Shortcut Formula for Variance:**

$$\sigma^2 = \frac{\sum x_i^2}{n} - \bar{x}^2$$

---

### 2.5 — STANDARD DEVIATION (SD)

The **square root of variance**. Brings units back to the original scale.

**Population SD:**
$$\sigma = \sqrt{\frac{\sum(x_i - \mu)^2}{N}}$$

**Sample SD:**
$$s = \sqrt{\frac{\sum(x_i - \bar{x})^2}{n-1}}$$

**From the previous example:**
Variance = 4 → **SD = √4 = 2**

**Key Properties:**
- Most widely used measure of dispersion.
- **Same units** as original data.
- A **low SD** → data is clustered close to the mean.
- A **high SD** → data is widely spread.
- For a **normal distribution:**
  - Mean ± 1σ covers **~68%** of data
  - Mean ± 2σ covers **~95%** of data
  - Mean ± 3σ covers **~99.7%** of data *(Empirical Rule / 68-95-99.7 Rule)*

---

### 2.6 — COEFFICIENT OF VARIATION (CV)

A **relative measure** of dispersion — used to compare variability between datasets with **different units or means**.

**Formula:**

$$CV = \frac{\sigma}{\bar{x}} \times 100\%$$

**Example:**
- Dataset A: Mean = 50, SD = 10 → CV = (10/50) × 100 = **20%**
- Dataset B: Mean = 200, SD = 30 → CV = (30/200) × 100 = **15%**

Dataset B has a higher SD but **less relative variability**. Dataset A is more variable relative to its mean.

**Key Properties:**
- **Dimensionless** — no units, pure percentage.
- Lower CV = more consistent/stable data.
- Perfect for comparing variability across **different scales** (e.g., comparing weight in kg vs height in cm).

---

### 2.7 — STANDARD ERROR (SE)

Measures how much the **sample mean is expected to vary** from the true population mean.

**Formula:**

$$SE = \frac{\sigma}{\sqrt{n}}$$

**Key Properties:**
- As **n increases**, SE decreases → larger samples give more reliable estimates.
- Used heavily in **hypothesis testing and confidence intervals**.
- Do NOT confuse with Standard Deviation:
  - **SD** = spread of individual data points
  - **SE** = spread of the sampling distribution of the mean

---

## PART 3 — QUICK COMPARISON TABLE

### Central Tendency

| Measure | Formula | Affected by Outliers? | Best For |
|---------|---------|----------------------|----------|
| Mean | Σx/n | Yes, heavily | Symmetric data |
| Median | Middle value | No | Skewed data |
| Mode | Most frequent | No | Categorical data |

### Dispersion

| Measure | Based On | Affected by Outliers? | Units |
|---------|---------|----------------------|-------|
| Range | Max - Min | Yes, heavily | Same as data |
| IQR | Q3 - Q1 | No | Same as data |
| Mean Deviation | Avg of \|deviations\| | Somewhat | Same as data |
| Variance | Avg of squared deviations | Yes | Squared |
| Standard Deviation | √Variance | Yes | Same as data |
| CV | (SD/Mean)×100 | Yes | % (unitless) |

---

## PART 4 — IMPORTANT PROPERTIES & THEOREMS TO REMEMBER

### Properties of Variance & SD

1. **Variance is always ≥ 0** (it's zero only if all values are identical)
2. Adding a **constant** to all values does NOT change variance/SD: `Var(X + c) = Var(X)`
3. **Multiplying** all values by constant k: `Var(kX) = k²·Var(X)` and `SD(kX) = k·SD(X)`
4. For independent variables: `Var(X + Y) = Var(X) + Var(Y)`

### Chebyshev's Theorem (Works for ANY Distribution)

For **any** distribution, at least `1 - 1/k²` of the data lies within k standard deviations of the mean.

- k=2: At least **75%** of data lies within 2 SDs of mean
- k=3: At least **88.9%** of data lies within 3 SDs of mean

Unlike the Empirical Rule, Chebyshev's applies to **non-normal** distributions too.

### Five Number Summary (used in Box Plots)

```
Minimum | Q1 | Median (Q2) | Q3 | Maximum
```

---

## PART 5 — SOLVED EXAMPLE (End-to-End)

**Dataset:** 12, 7, 3, 14, 6, 11, 5, 4, 9, 10

**Step 1 — Sort:** 3, 4, 5, 6, 7, 9, 10, 11, 12, 14

**Step 2 — Mean:**
Sum = 81, n = 10 → **Mean = 8.1**

**Step 3 — Median:**
n=10 (even) → Average of 5th and 6th values = (7+9)/2 = **Median = 8**

**Step 4 — Mode:**
All values appear once → **No Mode**

**Step 5 — Range:**
14 - 3 = **Range = 11**

**Step 6 — Q1, Q3, IQR:**
Lower half: 3,4,5,6,7 → Q1 = 5
Upper half: 9,10,11,12,14 → Q3 = 11
**IQR = 11 - 5 = 6**

**Step 7 — Variance:**
Deviations from mean (8.1): squared deviations:
(12-8.1)²=15.21, (7-8.1)²=1.21, (3-8.1)²=26.01, (14-8.1)²=34.81, (6-8.1)²=4.41
(11-8.1)²=8.41, (5-8.1)²=9.61, (4-8.1)²=16.81, (9-8.1)²=0.81, (10-8.1)²=3.61

Sum of squared deviations = 120.9
**Population Variance = 120.9/10 = 12.09**
**Sample Variance = 120.9/9 ≈ 13.43**

**Step 8 — Standard Deviation:**
**Population SD = √12.09 ≈ 3.48**

**Step 9 — CV:**
CV = (3.48/8.1) × 100 = **42.96%**

---

## PART 6 — COMMON EXAM TRICKS & GOTCHAS

1. **Median is preferred over mean** whenever you see words like "income", "salaries", "house prices", "skewed" — real-world data is almost always skewed.

2. **Variance uses squared units** — if asked for a measure in the same unit as data, use **SD**, not variance.

3. **Sample vs Population:**
   - Population (whole group known): divide by **N**
   - Sample (subset of population): divide by **n-1**

4. **CV is used for comparison** — whenever a question asks "which dataset is more consistent?", compute CV and pick the lower one.

5. **IQR and Outlier Detection:** The 1.5×IQR rule is the standard. Anything outside [Q1 - 1.5·IQR, Q3 + 1.5·IQR] is an outlier.

6. **Range is useless for comparison** — it only captures two points. Always prefer IQR or SD for meaningful comparison.

7. **Zero SD** means every single value in the dataset is the same.

8. **Adding a constant shifts the mean but doesn't change spread** (variance, SD, range all stay the same).

9. **Multiplying all values by k:** Mean gets multiplied by k, SD gets multiplied by k, Variance gets multiplied by k².

10. **Empirical Rule only works for normal distributions.** If the distribution is unknown or skewed, fall back to Chebyshev's theorem.

---

*End of Revision Notes — Good luck! 🎯*
