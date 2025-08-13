# 🧪 Comparative Study on Neural Spoofing Countermeasures for Synthetic Speech Detection

Original Paper: *[A Comparative Study on Recent Neural Spoofing Countermeasures for Synthetic Speech Detection](https://arxiv.org/abs/2103.11326)

---

## 🆕 What's New
- Demonstrates that results of anti-spoofing models can significantly vary depending on random seed initialization.
- Provides a thorough statistical analysis of this variability across different models.

## 🎯 Why It Matters
- Highlights the importance of reproducibility and reliability in anti-spoofing research.
- Establishes statistical measures and best practices for evaluating model stability, helping set a standard for future work.

## 📚 Literature Gap
- Previous research focused on improving fake audio detection, but often overlooked the instability caused by random seed initialization.
- This work is among the first to systematically analyze and quantify this issue.

## 🛠️ How the Gap is Filled
- The study compares models with various back-ends, front-ends, network structures, and loss functions.
- It employs a pair-wise statistical analysis to determine if the performance difference between any two systems (A and B) is statistically significant by computing a *z*-value.

  <p align="center">
    <img src="./z value.png" alt="Formula for z-value calculation" width="450">
    <br>
    <em>Statistical test formula to compare two systems.</em>
  </p>

- **Statistical Test Steps:**
  1. The *z*-value is calculated, where *N* is the number of bonafide and spoof trials.
  2. The calculated *z* is compared against a significance level threshold ($Z_{\alpha/2}$ where $\alpha = 0.05$).
  3. The Holm-Bonferroni correction is applied to account for multiple comparisons.
  4. If $z > Z_{\alpha/2}$, the performance difference between systems A and B is considered statistically significant.

## 🏆 Key Findings
- Identifies model configurations that achieve both high performance and low variance (i.e., stable results across random seeds).
- Provides guidance for selecting robust anti-spoofing models.

## 📂 Data Used
- Experiments conducted on the ASVspoof 2019 LA database.

## ⚠️ Limitations
- While the study exposes instability and proposes analysis methods, it does **not** offer concrete solutions to improve inherent model instability.
- Results depend on six independent training-evaluation runs, so findings may not be fully generalizable.

---

*For more details, see the original paper*