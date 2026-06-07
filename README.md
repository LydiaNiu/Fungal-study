# Environmental Constraints on Grapevine Pathogens: A Statistical Approach

## 1. Project Overview

This repository contains a comprehensive statistical analysis of the growth dynamics of a destructive fungal pathogen closely associated with grapevine decline. By modeling fungal response to Temperature and pH levels across duplicated experimental trials, this study identifies the precise environmental "peak" and "kill zones" necessary for developing effective sanitation and vineyard management strategies.

## 2. Key Biological Findings

* **Thermal Dominance:** Temperature is the primary determinant of fungal development, explaining **95.6%** of growth variance.
* **Growth Optima:** Peak colony diameter occurs at approximately **25°C** and a **pH range of 4.0–6.0**.
* **Inhibition Thresholds:** Growth is completely inhibited at extreme thermal limits (**0°C** and **31.1°C**) and extreme pH levels (**3.0** and **9.0**).

## 3. Statistical Methodology

The project employs a dual-modeling approach to account for differing levels of experimental variance and biological complexity.

### Temperature Modeling (Cubic Regression)

* Utilizes a third-degree polynomial to capture the rapid acceleration, plateau, and sharp decline characteristic of thermal metabolism.
* **Model Selection:** The Cubic fit was selected over Linear and Quadratic alternatives for its superior ability to model the upper thermal inhibition boundary.

### pH Level Modeling (Quadratic Regression)

* **I like this saying:** *"The pH model represents a successful trade-off between statistical beauty and scientific integrity."*
* **Data Refinement:** Observations with zero fungal growth were excluded to satisfy homoscedasticity requirements and focus on active growth zones.
* **Constraints:** Due to the reduction of unique pH levels post-filtering, a Quadratic model was employed to avoid overfitting and maintain degrees of freedom.

### Interaction Analysis (Two-Way ANOVA Framework)

* Experimental trials were analyzed for reproducibility.
* **Finding:** Temperature results were highly reproducible across trials, whereas pH response showed significant interaction with the "Trial" factor, necessitating its inclusion in the final predictive model.

## 4. Diagnostics & Validation

The models were validated against standard OLS assumptions:

* **Normality:** Confirmed via Q-Q plots and Shapiro-Wilk testing.
* **Independence:** Analyzed via Durbin-Watson testing. While pH demonstrated strong independence ($p=0.954$), the Temperature model showed moderate positive autocorrelation ($p=0.018$), a common trait in high-precision biological replicates.
* **Homoscedasticity:** Verified through Scale-Location and Residuals vs. Fitted plots.

## 5. Conclusion

This analysis transitions from simple observation to predictive modeling, providing a robust framework for understanding fungal ecology. The results confirm that while temperature acts as the "master switch" for growth, pH provides a significant secondary constraint, particularly in high-acid environments.

---

**Author:** Lydia Niu

**Field:** Statistical Data Analysis / Plant Pathology
