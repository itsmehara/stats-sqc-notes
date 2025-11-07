That's a great question, and understanding the tools is the perfect first step to differentiate their applications!

Before we dive into how control charts distinguish between process and product control, let's make sure we have a solid foundation on the charts themselves.

The sources define control charts as key tools in Statistical Quality Control (SQC) used to detect quickly if a manufacturing process is stable or unstable.

Here is a simple breakdown of the main types of control charts, their uses, and formulas, presented in the table format you requested:

### I. Control Charts for Variables (Measurable Data)
These charts monitor characteristics that can be numerically measured, such as weight or length. You must monitor both the average and the consistency (variability) of the product.

| Chart Name | Purpose (Use) | Center Line (CL) | Upper Control Limit (UCL) | Lower Control Limit (LCL) |
| :--- | :--- | :--- | :--- | :--- |
| **$\mathbf{\bar{X}}$ -Chart** | Monitors the **average level** or central tendency of the characteristic over time . | $CL = \bar{\bar{X}}$  | $UCL = \bar{\bar{X}} + A_2 \bar{R}$  | $LCL = \bar{\bar{X}} - A_2 \bar{R}$  |
| **R-Chart** | Monitors **process variability (spread)**, best for small sample sizes ($n < 10$) . | $CL = \bar{R}$  | $UCL = D_4 \bar{R}$  | $LCL = D_3 \bar{R}$ (or 0)  |
| **S-Chart** | Monitors **process variability (spread)**, best for large sample sizes ($n \ge 10$) . | $CL = \bar{S}$  | $UCL = B_4 \bar{S}$  | $LCL = B_3 \bar{S}$ (or 0)  |

*Note: $A_2$, $D_3, D_4, B_3, B_4$ are constants determined by the sample size ($n$) .*

***

### II. Control Charts for Attributes (Count Data)
These charts are used when classification is simple (good/bad) or when counting flaws .

#### A. Charts for Defectives (The Whole Item is Rejected)
These monitor the count or proportion of items that are completely unusable .

| Chart Name | Purpose (Use) | Center Line (CL) | Upper Control Limit (UCL) | Lower Control Limit (LCL) |
| :--- | :--- | :--- | :--- | :--- |
| **p-Chart** | Monitors the **proportion** of items found to be defective. Can handle variable sample sizes . | $CL = \bar{p}$  | $UCL = \bar{p} + 3\sqrt{\frac{\bar{p}(1-\bar{p})}{n}}$  | $LCL = \bar{p} - 3\sqrt{\frac{\bar{p}(1-\bar{p})}{n}}$ (or 0)  |
| **np-Chart** | Monitors the **absolute number** of defective items. Requires constant sample size ($n$) . | $CL = n\bar{p}$  | $UCL = n\bar{p} + 3\sqrt{n\bar{p}(1-\bar{p})}$  | $LCL = n\bar{p} - 3\sqrt{n\bar{p}(1-\bar{p})}$ (or 0)  |

#### B. Charts for Defects (Counting Flaws on a Single Item)
These charts are used when a single item may have multiple nonconformities/flaws .

| Chart Name | Purpose (Use) | Center Line (CL) | Upper Control Limit (UCL) | Lower Control Limit (LCL) |
| :--- | :--- | :--- | :--- | :--- |
| **c-Chart** | Monitors the **total number of defects** (flaws) found in a sample unit. Assumes constant sample size . | $CL = \bar{c}$  | $UCL = \bar{c} + 3\sqrt{\bar{c}}$  | $LCL = \bar{c} - 3\sqrt{\bar{c}}$ (or 0)  |
| **u-Chart** | Monitors the **average number of defects per unit**. Used when the sample size is variable (e.g., varying lengths of fabric) . | $CL = \bar{u}$  | $UCL_i = \bar{u} + 3\sqrt{\frac{\bar{u}}{n_i}}$  | $LCL_i = \bar{u} - 3\sqrt{\frac{\bar{u}}{n_i}}$ (or 0)  |

***

Now that we have reviewed the specific charts, let's return to your original question: How do these tools differentiate between process control and product control?

Based on the descriptions provided, which of these charts (Variables or Attributes) seems most focused on checking the characteristics *of the finished item* versus checking the consistency *of the manufacturing activity itself*?
