# 🧬 On Model Stability as a Function of Random Seed

Original Paper: *[On Model Stability as a Function of Random Seed](#)*

---

## 🆕 What's New
- Investigates how random seed initialization affects model output variability.
- Proposes two novel methods for improving robustness against randomness:
  - **ASWA (Aggressive Stochastic Weight Averaging)**
  - **NASWA (Norm-filtered Aggressive SWA)**
## 🆕 What's New
- Investigates how random seed initialization affects model output variability.
- Proposes two novel methods for improving robustness against randomness:
  - **ASWA (Aggressive Stochastic Weight Averaging)**
  - **NASWA (Norm-filtered Aggressive SWA)**

<p align="center">
  <img src="./aswa_algorithm.png" alt="ASWA Algorithm" width="320" style="display:inline-block; margin-right:10px;">
  <img src="./naswa_algorithm.png" alt="NASWA Algorithm" width="320" style="display:inline-block;">
  <br>
  <em>Left: ASWA Algorithm &nbsp;&nbsp;|&nbsp;&nbsp; Right: NASWA Algorithm</em>
</p>
## 🎯 Why It Matters
- Shows that interpretation and evaluation of models can be unreliable due to randomness from initialization.
- The proposed methods reduce output variation and improve the stability of interpretation metrics across different seeds.

## 📚 Literature Gap
- Many NLP interpretation methods exist, but their reliability is questionable due to inherent model randomness.
- Prior work rarely quantified or addressed this instability in interpretation.

<p align="center">
  <img src="./attention distribution.png" alt="Attention distribution variability across random seeds" width="500">
  <br>
  <em>Figure: Example of attention distribution variability across random seeds.</em>
</p>

## 🛠️ How the Gap is Filled
- Modifies the Stochastic Weight Averaging (SWA) technique to average weights around local minima, pushing models closer to global minima.
- Quantifies and improves the stability of model interpretations across different seeds.
- Demonstrates that the new methods reduce standard deviation and entropy of interpretation results.

## 🏆 Key Findings
- Improved output stability (lower standard deviation in accuracy) without sacrificing performance.
- Reveals that interpretation results can vary significantly with different random seeds.
- The proposed methods also reduce entropy in interpretation results across seeds.

## 📂 Data Used
- IMDB
- Diabetes (MIMIC)
- Anemia (MIMIC)
- AG News
- ...and more

## ⚠️ Limitations
- The methods use only first-order signals (e.g., gradients) for weight averaging, focusing on robustness to random seeds.
- Authors suggest future work could leverage second-order signals for broader robustness, including adversarial or counter samples.

---

*For more details, see the original paper.*