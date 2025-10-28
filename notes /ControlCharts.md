Here are quick reference notes on the different types of Control Charts, structured simply for your quick revision as a Statistics student focusing on SQC.

***

### Notes on Different Types of Control Charts

Control charts are the primary tools used in Statistical Process Control (SPC). They are broadly divided into two main categories based on the type of data being monitored: **Control Charts for Variables** and **Control Charts for Attributes**.

#### I. Phase I Control Charts (Shewhart Control Charts)

These charts are used initially (Phase I) to bring a process into a state of statistical control by identifying and eliminating large sources of variation (Assignable Causes). They primarily detect **large variations/shifts**.

---

### A. Control Charts for Variables

These charts are used when the quality characteristic being monitored is **measurable** (like length, weight, diameter, or temperature). They typically require a separate chart for each quality characteristic. Since variability and average must both be controlled, they usually come in pairs.

| Chart Type | Purpose (What it Controls) | Key Characteristic / Use Case |
| :--- | :--- | :--- |
| **$\overline{X}$-chart** (X-bar chart) | **Process Central Tendency (Mean)**. | Monitors the average quality level of the process. It is preferred over individual measurement plots for detecting changes in the process mean. |
| **R-chart** (Range chart) | **Process Variability/Dispersion.** | Monitors the spread of the data. Widely used when sample sizes ($n$) are **small** (usually less than 10), as calculating the range is simple. |
| **S-chart** (Standard Deviation chart) | **Process Variability/Dispersion.** | Monitors the spread of the data. Preferred when sample sizes ($n$) are **large** (usually 10 or more), as standard deviation uses all data points for a better picture of variability. |

---

### B. Control Charts for Attributes

These charts are used when the quality characteristic is **not measurable**, or when it is impractical or uneconomical to measure it. Items are simply classified as "good/bad" or the number of "defects" is counted. A single chart can be used to control several quality characteristics simultaneously.

#### B1. Charts for Defectives (Deals with items classified as defective)

| Chart Type | Purpose (What it Controls) | Key Characteristic / Formula Basis |
| :--- | :--- | :--- |
| **p-chart** (Fraction Defective) | **Proportion of defective units** (defective items divided by total items inspected). | Applicable for both **constant and variable sample sizes**. Based on the **Binomial Distribution**. |
| **np-chart** (Number of Defectives) | **Actual number of defective units** per sample. | Used primarily when the **sample size ($n$) is constant/equal**. Plots the actual count ($d = np$). |

#### B2. Charts for Defects (Deals with number of nonconformities)

| Chart Type | Purpose (What it Controls) | Key Characteristic / Formula Basis |
| :--- | :--- | :--- |
| **c-chart** (Number of Defects) | **Total number of defects/nonconformities** found in a unit/sample. | Used when the inspection unit size is **constant** (e.g., defects in one piece of furniture). Based on the **Poisson Distribution**. |
| **u-chart** (Defects per Unit) | **Average number of defects per inspection unit** ($u = c/n$). | Essential when the inspection unit/sample size **varies**. Plots the defect density. |

***

#### II. Phase II Control Charts (For Small Shifts)

These charts are implemented **after** the process has achieved statistical control using Phase I charts. They are much **more sensitive** and are designed specifically to detect **small shifts** in the process mean (generally less than $1.5\sigma$) which Shewhart charts often miss.

| Chart Type | Key Feature | Primary Use Case |
| :--- | :--- | :--- |
| **CUSUM Chart** (Cumulative Sum Chart) | Plots the **cumulative sum of deviations** from the target value, integrating information from past samples. | Highly effective for detecting shifts, particularly those around **$\pm 1.5\sigma$**. |
| **EWMA Chart** (Exponentially Weighted Moving Average Chart) | Calculates a weighted average where **recent data points are weighted highest**. Incorporates past data exponentially. | Highly effective for detecting **very small shifts**, typically better than CUSUM for shifts around **$\pm 1\sigma$**. |
