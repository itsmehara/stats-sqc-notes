Continuing our quick reference notes for your Statistics studies in Statistical Quality Control (SQC), 
here are concise points on the $3\sigma$ limits and the advantages/limitations of SQC, strictly based on your source materials.

***

### Notes on $3\sigma$ Limits

The concept of $3\sigma$ (three-sigma) limits is fundamental to control charts and Statistical Process Control (SPC).

*   **Basis (Normal Distribution):** A quality characteristic is usually assumed to follow a **normal distribution** or can be approximated by one.
*   **Probability Coverage:** For a normally distributed variable (X), the probability that it lies between **$\mu - 3\sigma$ and $\mu + 3\sigma$ is 0.9973**.
    *   This means $\mathbf{99.73\%}$ of observations/products are expected to fall inside these limits.
*   **Out-of-Limits Probability:** The probability that the variable (X) lies outside the $\mu \pm 3\sigma$ limits is very small: $1 - 0.9973 = \mathbf{0.0027}$.
*   **Purpose in Control Charts:** Because this probability is so low, control limits (UCL and LCL) on a control chart are set using $3\sigma$ limits. If a point falls outside these limits, it is logical to **suspect that something has gone wrong** (i.e., an assignable cause is present).
*   **Calculation (General Formula):** If M is a sample statistic (like the mean or range) with mean $\mu_{M}$ and standard error $\sigma_{M}$, the control lines are defined as:
    *   **Centre Line (CL):** $\mathbf{\mu_{M}}$.
    *   **Upper Control Limit (UCL):** $\mathbf{\mu_{M} + 3\sigma_{M}}$.
    *   **Lower Control Limit (LCL):** $\mathbf{\mu_{M} - 3\sigma_{M}}$.
*   **Interpretation:**
    *   If all sample points lie within or on the control limits (UCL and LCL), the process is **under statistical control** (only chance causes are present).
    *   If one or more sample points fall outside the limits, the control chart signals that the process is **out-of-control** (assignable causes are present), requiring investigation and corrective action.

***

### Advantages and Limitations of SQC

#### Advantages of SQC

1.  **Ease of Application:** SQC methods are **easy to apply**, even by persons who have not had extensive specialized training (though skilled persons develop the methods).
2.  **Reduction in Costs:** The cost of inspection is **reduced** since only a fraction or part of a lot is inspected, unlike 100% inspection.
3.  **Greater Efficiency:** Inspectors are generally **more alert** while using SQC compared to the dull routine of inspecting every item (100% inspection).
4.  **Early Detection of Faults:** SQC involves **continuous checking**, providing signals (when points fall outside control limits) that allow for necessary corrective action, resulting in **minimum wastage** of items.
5.  **Helpful in Specification:** SQC signals danger if variation is beyond tolerance limits. As long as statistical control continues, **specifications can be accurately predicted for the future**.
6.  **Ensures Overall Coordination:** SQC helps managers coordinate decisions regarding specifications, production, and inspection, providing a basis to resolve organizational differences.
7.  **Determination of the Effect of Change:** Control charts make it easy to detect whether a change in the production process results in a significant change in quality.
8.  **Equilibrium in Risk:** SQC tools, like acceptance sampling, help maintain balance (equilibrium) between the **consumer's risk and the producer's risk**.
9.  **Wider Applications:** SQC is useful both when items are produced in small numbers and when **bulk production** is carried out.
10. **Unique Method for Destructive Testing:** SQC is essential for items that are destroyed upon examination (e.g., testing the average life of a compact fluorescent lamp (CFL), the strength of glass, or the intensity of match sticks) where 100% inspection would spoil the entire lot and cause huge loss.

#### Limitations of SQC

1.  **Sampling Risk (Main Limitation):** If the sample drawn from a lot is **not a true representative** (lacks the same characteristics as the lot), there is a risk that a good lot may be rejected, or a bad one may be accepted.
2.  **Requires Adequate Knowledge:** SQC cannot be applied mechanically to any production process without **studying the process** and possessing **adequate knowledge** about it.
3.  **No Direct Action:** SQC provides **only information** (whether the process is under control or out of control); it cannot take action for improvement itself.
