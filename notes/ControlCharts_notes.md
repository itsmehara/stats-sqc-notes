These notes cover the definitions, key features, and formulas for the three main control charts used for variables. 
We are keeping the context easy for a quick read, perfect for your stats revision.

***

### Control Charts for Variables (Measurable Characteristics)

These charts are used when the quality characteristic (like weight, diameter, or length) can be **measured**. Since we need to control both the level and the spread of the process, these charts are typically used in pairs ($\overline{X}$ and R, or $\overline{X}$ and S charts).

#### 1. $\overline{X}$-Chart (X-bar Chart) – For Process Mean

| Quick Reference Points | Details & Definition |
| :--- | :--- |
| **Purpose** | To control the **Process Central Tendency (Average)**. |
| **What is Plotted?** | The **Sample Mean** ($\overline{X}$) for each sample is plotted along the Y-axis against the sample number or time. |
| **Sensitivity** | This chart is highly sensitive to detecting changes or shifts in the process mean. |
| **Typical Use** | Always used along with a variability chart (R-chart or S-chart) to ensure complete control. |

**Key Formulas (When Process Mean ($\mu$) and SD ($\sigma$) are Unknown):**

| Line | Formula (Using Sample Range, $\overline{R}$) | Note |
| :--- | :--- | :--- |
| **Centre Line (CL)** | $CL = \mathbf{\overline{\overline{X}}}$ | $\overline{\overline{X}}$ is the Grand Mean (Average of all Sample Means). |
| **Upper Control Limit (UCL)** | $UCL = \mathbf{\overline{\overline{X}} + A_{2}\overline{R}}$ | $A_{2}$ is a control chart constant dependent on sample size ($n$). |
| **Lower Control Limit (LCL)** | $LCL = \mathbf{\overline{\overline{X}} - A_{2}\overline{R}}$ | |

***

#### 2. R-Chart (Range Chart) – For Process Variability

| Quick Reference Points | Details & Definition |
| :--- | :--- |
| **Purpose** | To control the **Process Variability or Dispersion** (the spread of the data). |
| **What is Plotted?** | The **Sample Range** ($R$) for each sample is plotted. |
| **When to Use?** | **Most widely used** for variability control, especially when the **sample size ($n$) is small (typically $n < 10$)**. The range is considered easier to calculate and interpret than the standard deviation. |
| **Order of Analysis** | The R-chart must be analyzed **first**. If variability is out-of-control, the $\overline{X}$-chart cannot be accurately interpreted. |
| **Range Calculation** | $R_{i}=X_{max}-X_{min}$ (Maximum minus Minimum value in the sample). |

**Key Formulas (When Process Standard Deviation ($\sigma$) is Unknown):**

| Line | Formula | Note |
| :--- | :--- | :--- |
| **Centre Line (CL)** | $CL = \mathbf{\overline{R}}$ | $\overline{R}$ is the mean of all sample ranges. |
| **Upper Control Limit (UCL)** | $UCL = \mathbf{D_{4}\overline{R}}$ | $D_{4}$ is a control chart constant dependent on sample size ($n$). |
| **Lower Control Limit (LCL)** | $LCL = \mathbf{D_{3}\overline{R}}$ | $D_{3}$ is a control chart constant dependent on sample size ($n$). |

***

#### 3. S-Chart (Standard Deviation Chart) – For Process Variability

| Quick Reference Points | Details & Definition |
| :--- | :--- |
| **Purpose** | Also controls **Process Variability or Dispersion**. |
| **What is Plotted?** | The **Sample Standard Deviation** ($S$) for each sample is plotted. |
| **When to Use?** | Used when the **sample size ($n$) is large (typically $n \ge 10$)**. For large samples, the Standard Deviation gives a more accurate measure of process spread compared to the Range, as it uses *all* observations, not just the two extreme values. |
| **Alternate Names** | Some authors refer to this as the $\sigma$-chart or $\sum$-chart. |

**Key Formulas (When Process Standard Deviation ($\sigma$) is Unknown):**

| Line | Formula | Note |
| :--- | :--- | :--- |
| **Centre Line (CL)** | $CL = \mathbf{\overline{S}}$ | $\overline{S}$ is the mean of all sample standard deviations. |
| **Upper Control Limit (UCL)** | $UCL = \mathbf{B_{4}\overline{S}}$ | $B_{4}$ is a control chart constant dependent on sample size ($n$). |
| **Lower Control Limit (LCL)** | $LCL = \mathbf{B_{3}\overline{S}}$ | $B_{3}$ is a control chart constant dependent on sample size ($n$). |

***
**Note on Control Limit Factors:**
The constants $A_2$, $D_3$, $D_4$, $B_3$, and $B_4$ incorporate the $3\sigma$ distance needed for control charts. They are based on the assumption that the underlying process is normally distributed. When $\mu$ and $\sigma$ are unknown (which is often the case in practice), these empirical constants are used to estimate the control limits.
