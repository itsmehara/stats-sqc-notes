Here are comprehensive notes containing all the core formulas and summation notations 
related to the mean and variability concepts discussed in Unit 1 (Overview) and Unit 2 (Control Charts for Mean and Variation) of Block 1. 
Keep these handy for your quick reference!

***

### Quick Reference Formulas: Mean, Variation, and Control Limits

#### A. Notations and Fundamental Calculations

These basic formulas define the sample statistics used in control charts.

| Concept | Notation | Formula | Tiny Note | Source |
| :--- | :--- | :--- | :--- | :--- |
| **Individual Measurement** | $X_{i}$ | $X_{1}, X_{2}, \dots, X_{n}$ | Measurements on a random sample of size $n$. | |
| **Summation (Sample)** | $\sum_{i=1}^{n}X_{i}$ | $X_{1}+X_{2}+\dots+X_{n}$ | Sum of all measurements within one sample. | |
| **Sample Mean** | $\overline{X}$ | $\overline{X}=\frac{1}{n}\sum_{i=1}^{n}X_{i}$ | Mean (Average) of a single sample of size $n$. | |
| **Sample Range** | $R$ | $R_{i}=X_{max}-X_{min}$ | Difference between the largest and smallest observation in a sample. | |

#### B. Process Parameters and Estimators ($\mu$ and $\sigma$)

These formulas define the true process parameters and how we estimate them from collected samples ($k$ is the total number of samples/subgroups inspected).

| Concept | Notation | Formula | Tiny Note | Source |
| :--- | :--- | :--- | :--- | :--- |
| **Process Mean (True Value)** | $\mu$ | $CL=E(\overline{X})=\mu$ | Expected value of the sample mean ($\overline{X}$). | |
| **Grand Mean (Estimate of $\mu$)** | $\overline{\overline{X}}$ | $\overline{\overline{X}}=\frac{1}{k}\sum_{i=1}^{k}\overline{X}_{i}$ | Average of all sample means. Used as the best estimate ($\hat{\mu}$) when $\mu$ is unknown. | |
| **Mean of Sample Ranges** | $\overline{R}$ | $\overline{R}=\frac{1}{k}\sum_{i=1}^{k}R_{i}$ | Average of all $k$ sample ranges. | |
| **Mean of Sample SDs** | $\overline{S}$ | $\overline{S}=\frac{1}{k}\sum_{i=1}^{k}S_{i}$ | Average of all $k$ sample standard deviations. | |
| **Estimated SD ($\hat{\sigma}$ via R)** | $\hat{\sigma}$ | $\hat{\sigma}=\overline{R}/d_{2}$ | Estimate of process SD ($\sigma$) using $\overline{R}$. Preferred for small samples ($n<10$). | |
| **Estimated SD ($\hat{\sigma}$ via S)** | $\hat{\sigma}$ | $\hat{\sigma}=\overline{S}/c_{4}$ | Estimate of process SD ($\sigma$) using $\overline{S}$. Preferred for large samples ($n \ge 10$). | |
| **Standard Error of Mean** | $SE(\overline{X})$ | $SE(\overline{X})=\sigma/\sqrt{n}$ | Variability of the sample mean distribution. | |

#### C. General and Specific Control Chart Formulas

The foundation of all control charts is the $3\sigma$ limit principle. The specific formulas below are derived from this principle.

1.  **General $3\sigma$ Control Limits Formula**

    If $M$ is a sample statistic (like $\overline{X}$ or $R$) with mean $\mu_{M}$ and standard error $\sigma_{M}$:

    $$
    \mathbf{CL} = \mu_{M} \quad
    $$
    $$
    \mathbf{UCL} = \mu_{M} + 3\sigma_{M} \quad
    $$
    $$
    \mathbf{LCL} = \mu_{M} - 3\sigma_{M} \quad
    $$
    (Note: If LCL is negative, it is usually taken as zero).

2.  **$\overline{X}$-Chart Formulas (Using $\overline{R}$ as SD estimate)**

    These are used primarily when the true $\mu$ and $\sigma$ are unknown, and $\overline{R}$ is used to estimate $\sigma$ (common for $n<10$).

    | Line | Formula | Constant Definition | Source |
    | :--- | :--- | :--- | :--- |
    | **CL** | $CL = \mathbf{\overline{\overline{X}}}$ | Estimate of the process mean $\mu$. | |
    | **UCL** | $UCL = \mathbf{\overline{\overline{X}} + A_{2}\overline{R}}$ | $A_{2}=\frac{3}{d_{2}\sqrt{n}}$ is a constant factor. | |
    | **LCL** | $LCL = \mathbf{\overline{\overline{X}} - A_{2}\overline{R}}$ | | |

3.  **$\overline{X}$-Chart Formulas (Using $\overline{S}$ as SD estimate)**

    These are used when the true $\mu$ and $\sigma$ are unknown, and $\overline{S}$ is used to estimate $\sigma$ (common for $n \ge 10$).

    | Line | Formula | Constant Definition | Source |
    | :--- | :--- | :--- | :--- |
    | **CL** | $CL = \mathbf{\overline{\overline{X}}}$ | Estimate of the process mean $\mu$. | |
    | **UCL** | $UCL = \mathbf{\overline{\overline{X}} + A_{3}\overline{S}}$ | $A_{3}=\frac{3}{c_{4}\sqrt{n}}$ is a constant factor. | |
    | **LCL** | $LCL = \mathbf{\overline{\overline{X}} - A_{3}\overline{S}}$ | | |

4.  **R-Chart Formulas (For Variability Control, $\sigma$ unknown)**

    The R-chart is typically used when $n<10$.

    | Line | Formula | Constant Definition | Source |
    | :--- | :--- | :--- | :--- |
    | **CL** | $CL = \mathbf{\overline{R}}$ | Estimate of the mean of the range distribution. | |
    | **UCL** | $UCL = \mathbf{D_{4}\overline{R}}$ | $D_{4}=(1+\frac{3d_{3}}{d_{2}})$ is a constant factor. | |
    | **LCL** | $LCL = \mathbf{D_{3}\overline{R}}$ | $D_{3}=(1-\frac{3d_{3}}{d_{2}})$ is a constant factor. | |

5.  **S-Chart Formulas (For Variability Control, $\sigma$ unknown)**

    The S-chart is typically used when $n \ge 10$.

    | Line | Formula | Constant Definition | Source |
    | :--- | :--- | :--- | :--- |
    | **CL** | $CL = \mathbf{\overline{S}}$ | Estimate of the mean of the standard deviation distribution. | |
    | **UCL** | $UCL = \mathbf{B_{4}\overline{S}}$ | $B_{4}=(1+\frac{3}{c_{4}}\sqrt{1-c_{4}^{2}})$ is a constant factor. | |
    | **LCL** | $LCL = \mathbf{B_{3}\overline{S}}$ | $B_{3}=(1-\frac{3}{c_{4}}\sqrt{1-c_{4}^{2}})$ is a constant factor. | |
