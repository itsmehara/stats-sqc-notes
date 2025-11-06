This is an excellent idea! A simple, consolidated article is perfect for quick reference and sharing.

Here is a simplified article format covering the main Control Charts for Statistical Quality Control (SQC), their uses, and fundamental formulas.

***

# Control Charts: A Simple Guide to Monitoring Process Quality

Statistical Quality Control (SQC) uses statistical tools to monitor and maintain the quality of products. The most important tool in this is the **Control Chart**, which is a two-dimensional graph that helps us quickly detect if a manufacturing process is stable (under statistical control) or unstable (out-of-control).

Control charts work by setting three horizontal lines based on the process data:
1.  **Centre Line (CL):** Represents the average or target value of the quality characteristic.
2.  **Upper Control Limit (UCL):** The maximum expected variation, typically set at $CL + 3\sigma_{M}$.
3.  **Lower Control Limit (LCL):** The minimum expected variation, typically set at $CL - 3\sigma_{M}$.

If a plotted point falls outside these limits, it signals the presence of "Assignable Causes" that need investigation.

Control charts are grouped into two main types: Charts for **Variables** (for measurable data) and Charts for **Attributes** (for count data).

***

## I. Control Charts for Variables (Measurable Data)

These charts are used when the quality characteristic can be measured numerically (e.g., diameter, weight, length, volume). When using these, you must monitor both the average (mean) and the consistency (variability) of the product.

| Chart Name | Purpose (When to Use) | Formulas (When $\mu$ and $\sigma$ are Unknown) |
| :--- | :--- | :--- |
| **1. $\mathbf{\bar{X}}$-Chart** (Control for Mean) | Used to monitor the **central tendency** or **average level** of the measurable characteristic over time. | $CL = \bar{\bar{X}}$ |
| | | $UCL = \bar{\bar{X}} + A_2 \bar{R}$ |
| | | $LCL = \bar{\bar{X}} - A_2 \bar{R}$ |
| **2. R-Chart** (Range Chart) | Used alongside the $\bar{X}$-Chart to monitor **process variability (spread)**. Best when sample size ($n$) is small (typically $n<10$). | $CL = \bar{R}$ |
| | | $UCL = D_4 \bar{R}$ |
| | | $LCL = D_3 \bar{R}$ (or 0 if negative) |
| **3. S-Chart** (Standard Deviation) | Used to monitor **process variability (spread)** when the sample size ($n$) is large ($\ge 10$). | $CL = \bar{S}$ |
| | | $UCL = B_4 \bar{S}$ |
| | | $LCL = B_3 \bar{S}$ (or 0 if negative) |

> *Note: $A_2, D_3, D_4, B_3, B_4$ are constants determined by the sample size ($n$).*

**Use Case Example:** A company making cricket balls measures the exact **weight** (a measurable variable). They use the $\bar{X}$-Chart to monitor the average weight over time, and the R-Chart (or S-Chart) to monitor how consistent or spread out the weights are.

***

## II. Control Charts for Attributes (Count Data)

These charts are used when products are classified simply as good/bad, defective/non-defective, or when counting the number of flaws/defects.

### A. Charts for Defectives (The Whole Item is Bad)

These monitor the proportion or count of items that are completely rejected.

| Chart Name | Purpose (When to Use) | Formulas (When $P$ is Unknown) |
| :--- | :--- | :--- |
| **4. p-Chart** (Fraction Defective) | Monitors the **proportion** of items found to be defective. Can handle **variable sample sizes**. | $CL = \bar{p}$ |
| | | $UCL = \bar{p} + 3\sqrt{\frac{\bar{p}(1-\bar{p})}{n}}$ |
| | | $LCL = \bar{p} - 3\sqrt{\frac{\bar{p}(1-\bar{p})}{n}}$ (or 0) |
| **5. np-Chart** (Number of Defectives) | Monitors the **absolute number** of items found to be defective. Must be used only when the **sample size ($n$) is constant**. | $CL = n\bar{p}$ |
| | | $UCL = n\bar{p} + 3\sqrt{n\bar{p}(1-\bar{p})}$ |
| | | $LCL = n\bar{p} - 3\sqrt{n\bar{p}(1-\bar{p})}$ (or 0) |

**Use Case Example:** In a batch of 100 mobile phones, 5 are found to be completely unusable (defective). The p-chart tracks the rate (5/100 = 0.05).

### B. Charts for Defects (Counting Flaws on a Single Item)

These charts are used when one item may have multiple defects (nonconformities) but is not necessarily rejected outright.

| Chart Name | Purpose (When to Use) | Formulas (When $\lambda$ is Unknown) |
| :--- | :--- | :--- |
| **6. c-Chart** (Number of Defects) | Monitors the **total number of defects** (flaws/nonconformities) found in a single inspection unit or sample. Assumes **constant sample size**. | $CL = \bar{c}$ |
| | | $UCL = \bar{c} + 3\sqrt{\bar{c}}$ |
| | | $LCL = \bar{c} - 3\sqrt{\bar{c}}$ (or 0) |
| **7. u-Chart** (Defects per Unit) | Monitors the **average number of defects per unit**. Used when the **sample size is variable** (e.g., inspecting 100 meters of cloth one day and 150 meters the next). | $CL = \bar{u}$ |
| | | $UCL_i = \bar{u} + 3\sqrt{\frac{\bar{u}}{n_i}}$ |
| | | $LCL_i = \bar{u} - 3\sqrt{\frac{\bar{u}}{n_i}}$ (or 0) |

**Use Case Example:** An auditor checks a large roll of fabric. She counts 15 separate snags or blemishes (defects). If all rolls are the same size, use the c-Chart. If the roll lengths vary, use the u-Chart.

***

## III. Advanced Charts for Small Shifts (Phase II)

The standard charts ($\bar{X}$, R, p, etc.) are excellent at catching large shifts. For detecting very small, sustained shifts in the process mean (like $1.5\sigma$ or less), special charts are used:

| Chart Name | Purpose (When to Use) | Primary Feature |
| :--- | :--- | :--- |
| **CUSUM** (Cumulative Sum) | Used to detect **small, sustained shifts** in the mean (around $\pm 1.5\sigma$). | Plots the cumulative sum of deviations from a target value. |
| **EWMA** (Exponentially Weighted Moving Average) | Used to detect even **smaller shifts** in the mean (around $\pm 1\sigma$). | Gives more weight to recent data points than older data points. |

This structure provides a clean overview of the key control charts needed for statistical quality control!

What step would you like to focus on next? Perhaps an explanation of the core difference between **defectives** ($p$, $np$) and **defects** ($c$, $u$)?
