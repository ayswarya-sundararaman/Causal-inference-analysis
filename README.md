
# Police Shooting Causal Inference Analysis

## 📌 Project Overview
This project investigates the **causal impact of police body cameras** on use-of-force decisions in law enforcement. By leveraging **causal inference techniques**, we estimate whether officers wearing body cameras exhibit different behavior compared to those who do not. The study applies **propensity score matching, inverse probability weighting (IPW), S-Learner, T-Learner, and backdoor adjustment** to derive unbiased causal estimates.

## 📊 Dataset
The dataset consists of **5,000+ police shooting incidents**, capturing key variables such as:
- **Use of Force Indicators** – Firearm discharge, taser use, etc.
- **Body Camera Presence** – (Treatment variable)
- **Suspect Attributes** – Race, armed status, threat level
- **Officer Characteristics** – Years of experience, jurisdiction
- **Manner of Death** – Outcome of the police encounter

## 🔬 Methodology
To estimate the **causal effect** of body cameras on use-of-force decisions, the project implements:

1. **Naïve ATE Calculation** – Compares raw mean differences between treated (body camera) and control (no body camera) groups.
2. **Propensity Score Matching (PSM)** – Matches cases with similar characteristics to balance treatment and control groups.
3. **Inverse Probability Weighting (IPW)** – Uses a **Random Forest classifier** to estimate treatment probabilities.
4. **S-Learner & T-Learner Models** – Applies **Random Forest & Decision Tree classifiers** to estimate **counterfactual outcomes**.
5. **Matching Estimation** – Uses **K-Nearest Neighbors (KNN) with Hamming distance** for causal effect estimation.
6. **Backdoor Adjustment** – Controls for confounders like **‘arms_category’** to refine causal estimates.

## 📈 Results
- **Naïve ATE** estimate: **0.0132** (biased due to confounders)
- **Backdoor-adjusted ATE**: **0.0012**, indicating minimal causal impact of body cameras
- **S-Learner and T-Learner models** using **Random Forest and Decision Tree classifiers** produced stable ATE estimates, ensuring robustness.

## ⚙️ Technologies Used
- **Programming:** Python
- **Data Handling:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn` (`RandomForestClassifier`, `DecisionTreeClassifier`, `KNeighborsClassifier`)
- **Visualization:** `matplotlib`
- **Statistical Analysis:** `scipy`
- **Causal Inference:** Custom implementation (no external causal libraries used)

## 🚀 How to Run
1. Clone the repository:
   ```git clone https://github.com/ayswarya-sundararaman/Causal-inference-analysis.git
cd Causal-inference-analysis```


