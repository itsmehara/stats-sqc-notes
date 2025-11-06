
In Statistical Quality Control (SQC), the **control chart constants** such as **A₁, A₂, A₃, D₃, D₄, B₃, B₄, c₄, d₂**, etc., are standard factors derived from statistical theory (mainly based on the sampling distribution of the range or standard deviation).

Below is a **clear, short, exam-oriented note** with **formulas, interpretation, and reference values** — so you can **remember and use them directly** when solving control chart problems.

---

# 📘 Control Chart Constants — Notes and Formulas

---

## 🔹 1. Purpose of Control Chart Constants

These constants are used to:

* Simplify the computation of control limits (UCL, LCL) for variable control charts.
* Replace theoretical σ (population standard deviation) by estimators based on sample range (R) or standard deviation (S).
* Adjust for **sample size (n)** — because variation of range/SD depends on subgroup size.

---

## 🔹 2. Common Constants & Where They Are Used

| Constant   | Used In                      | Formula/Relation                                                       | Purpose                                                    |
| ---------- | ---------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------- |
| **A₂**     | X̄–R Chart                   | $( A_2 = \frac{3}{d_2\sqrt{n}} )$                                        | Multiplies (\bar{R}) to estimate mean chart limits         |
| **A₃**     | X̄–S Chart                   | $( A_3 = \frac{3}{c_4\sqrt{n-1}} )$                                      | Multiplies (\bar{S}) to estimate mean chart limits         |
| **A₁**     | Less common (special charts) | Derived from $(3 / (d_2\sqrt{n}))$ for small n                           | Similar role to A₂ in older texts                          |
| **B₃, B₄** | S-Chart                      | $( B_3 = 1 - \frac{3(1-c_4)}{c_4} ), ( B_4 = 1 + \frac{3(1-c_4)}{c_4} )$ | For control limits on S chart                              |
| **D₃, D₄** | R-Chart                      | $( D_3 = 1 - \frac{3d_3}{d_2} ), ( D_4 = 1 + \frac{3d_3}{d_2} )$         | For control limits on R chart                              |
| **d₂**     | Range factor                 | From tables                                                            | Mean of distribution of R/dσ; used in estimating σ from R̄ |
| **d₃**     | Range SD factor              | From tables                                                            | Standard deviation of distribution of R/dσ                 |
| **c₄**     | SD bias correction           | $( E(S) = c_4σ )$                                                        | Corrects bias in S-based σ estimates                       |

---

## 🔹 3. Typical Reference Table (for small subgroup sizes n ≤ 25)

| n  | A₂    | A₃    | d₂    | d₃    | D₃    | D₄    | B₃    | B₄    | c₄     |
| -- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ------ |
| 2  | 1.880 | 2.659 | 1.128 | 0.853 | 0     | 3.267 | 0     | 2.266 | 0.7979 |
| 3  | 1.023 | 1.954 | 1.693 | 0.888 | 0     | 2.574 | 0     | 2.568 | 0.8862 |
| 4  | 0.729 | 1.628 | 2.059 | 0.880 | 0     | 2.282 | 0     | 2.266 | 0.9213 |
| 5  | 0.577 | 1.427 | 2.326 | 0.864 | 0     | 2.114 | 0     | 2.089 | 0.9400 |
| 6  | 0.483 | 1.287 | 2.534 | 0.848 | 0     | 2.004 | 0.030 | 1.970 | 0.9515 |
| 7  | 0.419 | 1.182 | 2.704 | 0.833 | 0.118 | 1.924 | 0.118 | 1.882 | 0.9594 |
| 8  | 0.373 | 1.099 | 2.847 | 0.820 | 0.185 | 1.864 | 0.185 | 1.815 | 0.9650 |
| 9  | 0.337 | 1.032 | 2.970 | 0.808 | 0.239 | 1.816 | 0.239 | 1.761 | 0.9693 |
| 10 | 0.308 | 0.975 | 3.078 | 0.797 | 0.284 | 1.777 | 0.284 | 1.716 | 0.9727 |

*(Values beyond n=10 can be included if needed — typically up to n=25 in most SQC references.)*

---

## 🔹 4. Key Relationships Between Constants

These are useful if the table is not given in exam (and the question provides only partial constants):

* $( A_2 = \dfrac{3}{d_2 \sqrt{n}} )$
* $( D_3 = 1 - \dfrac{3d_3}{d_2} )$
* $( D_4 = 1 + \dfrac{3d_3}{d_2} )$
* $( A_3 = \dfrac{3}{c_4 \sqrt{n - 1}} )$
* $( B_3 = 1 - \dfrac{3(1 - c_4)}{c_4} )$
* $( B_4 = 1 + \dfrac{3(1 - c_4)}{c_4} )$

These formulas connect constants with theoretical distributions.

---

## 🔹 5. How to Remember Quickly (Exam Tip)

| Chart           | Constants Used | Memory Tip              |
| --------------- | -------------- | ----------------------- |
| **X̄–R**        | A₂, D₃, D₄     | *R → Range → D’s + A₂*  |
| **X̄–S**        | A₃, B₃, B₄     | *S → SD → B’s + A₃*     |
| **R or S to σ** | d₂, d₃, c₄     | *Used for σ estimation* |

> 🧠 Quick Recall Trick:
>
> * **A → Average (X̄ chart)**
> * **B → Based on S chart**
> * **D → Derived from Range (R chart)**
> * **c₄, d₂, d₃ → correction constants from distribution properties**

---

## 🔹 6. Example of Using Constants

Suppose n = 5, and data are:

* $(\bar{R} = 4.5)$
* $(\bar{\bar{X}} = 52.3)$

From table: A₂ = 0.577, D₃ = 0, D₄ = 2.114.

Then:

* X̄ chart:
  $(UCL = 52.3 + (0.577)(4.5) = 54.9)$
  $(LCL = 52.3 - (0.577)(4.5) = 49.7)$
* R chart:
  $(UCL_R = (2.114)(4.5) = 9.5)$
  $(LCL_R = (0)(4.5) = 0)$

---

## 🔹 7. Key Concept: Why constants differ by n

As subgroup size (n) increases:

* Range variability decreases relative to σ.
* Therefore, **A₂, A₃ decrease** with larger n.
* **B₄, D₄** approach 1 (narrower relative limits).
  This is because larger samples give more stable estimates of process variation.

---

## 🔹 8. When Constants Are Not Given (Derivation Summary)

If exam gives only **d₂**, you can compute:

* $( \sigma = \dfrac{\bar{R}}{d_2} )$
* Then $( A_2 = \dfrac{3}{d_2\sqrt{n}} )$
* $( D_3 = 1 - \dfrac{3d_3}{d_2} )$
* $( D_4 = 1 + \dfrac{3d_3}{d_2} )$

If **c₄** given (for S chart):

* $( A_3 = \dfrac{3}{c_4\sqrt{n-1}} )$
* $( B_3 = 1 - \dfrac{3(1-c_4)}{c_4} )$
* $( B_4 = 1 + \dfrac{3(1-c_4)}{c_4} )$

---

## 🔹 9. Exam Quick Sheet Summary

| Chart | Constants | UCL                          | CL              | LCL                          |
| ----- | --------- | ---------------------------- | --------------- | ---------------------------- |
| X̄–R  | A₂        | $(\bar{\bar{X}} + A_2\bar{R})$ | $(\bar{\bar{X}})$ | $(\bar{\bar{X}} - A_2\bar{R})$ |
| R     | D₃, D₄    | $(D_4\bar{R})$                 | $(\bar{R})$       | $(D_3\bar{R})$                 |
| X̄–S  | A₃        | $(\bar{\bar{X}} + A_3\bar{S})$ | $(\bar{\bar{X}})$ | $(\bar{\bar{X}} - A_3\bar{S})$ |
| S     | B₃, B₄    | $(B_4\bar{S})$                 | $(\bar{S})$       | $(B_3\bar{S})$                 |

---

## 🔹 10. Key takeaway for your exam memory

* Use **A₂, D₃, D₄ → R chart family (n ≤ 10)**
* Use **A₃, B₃, B₄ → S chart family (n > 10)**
* Constants depend **only on n**, not on data values.
* Tables are standard — write "from standard table" if not given.

---
