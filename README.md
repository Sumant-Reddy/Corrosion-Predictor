# 🧪 Machine Learning-Based Corrosion Rate Prediction in High-Entropy Alloys

## 📅 **Project Duration:** Mar - Jun 2024

## 🛠️ **Tech Stack:**

**Languages & Tools:** Python, NumPy, Pandas, Matplotlib, Seaborn
**ML Libraries:** Scikit-learn, XGBoost, SHAP, Ridge Regression, GBDT, SVM
**Optimization Techniques:** Grid Search, Random Search, Bayesian Optimization
**Model Evaluation:** R², MAE, MSE, RMSE
**Visualization:** Matplotlib, SHAP



## 🌍 **Project Overview**

This Project is a machine learning-based research project focused on predicting the **electrochemical corrosion behavior** of **High-Entropy Alloys (HEAs)**. The platform utilizes curated experimental data and data-driven approaches to predict two key corrosion parameters:

* **Corrosion Potential (Ecorr)** – Thermodynamic indicator of corrosion susceptibility
* **Corrosion Current Density (Icorr)** – Kinetic measure of actual corrosion rate

This work bridges materials science and artificial intelligence, enabling **rapid screening of HEA compositions** for corrosion resistance and accelerating the design of next-generation materials for harsh environments.



## 🔬 **Why It Matters**

Corrosion causes massive industrial losses, accounting for approximately **7% of India’s GDP annually**. Traditional trial-and-error methods for corrosion resistance testing are time-consuming and expensive. Our ML-based framework offers a **predictive, scalable, and efficient** alternative to conventional methods.



## 🔧 **Core Features & Methodology**

### 🧹 **1. Data Collection & Preprocessing**

* Extracted electrochemical corrosion data from **peer-reviewed literature** (Web of Science, Google Scholar).
* Focused on **as-cast HEAs** tested under **standardized room-temperature conditions**.
* Standardized corrosion potential values to SCE reference electrode.
* Applied **log-scale transformation** on Icorr to reduce variance.

### 🧪 **2. Feature Engineering**

* Engineered 38 features including:

  * **Environmental parameters**: pH, Cl⁻, SO₄²⁻ concentration, solution type
  * **Material phase descriptors**: ΔHmix, ΔSmix, δ, Ω, χ̄, VEC, e/a, Tm
  * **Compositional vectors** for 21 elements
* Performed feature encoding for categorical environments and normalization for numerical inputs.

### 🔍 **3. Feature Selection (Three-Step Process)**

* **Step 1:** Pearson Correlation Analysis
  Removed highly correlated and redundant features (|r| > 0.8).
* **Step 2:** Random Forest Feature Importance
  Ranked features and removed low-importance inputs.
* **Step 3:** Recursive Feature Elimination (RFE)
  Selected optimal subset of features minimizing MSE and improving model generalization.

### 🤖 **4. Machine Learning Models**

* Applied and compared multiple ML regression algorithms:

  * **XGBoost**
  * **Gradient Boosted Decision Trees (GBDT)**
  * **Random Forest (RF)**
  * **Support Vector Machine (SVM)**
  * **Ridge Regression (RR)**
* Trained using **5-fold cross-validation**, with train-test split of **80:20**.

### 🎯 **5. Hyperparameter Tuning**

* Employed **Grid Search**, **Random Search**, and **Bayesian Optimization** to fine-tune each model.
* Bayesian Optimization enabled faster convergence and efficient exploration.

### 📈 **6. Evaluation Metrics**

* **R² (Coefficient of Determination)**
* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **RMSE (Root Mean Squared Error)**
  Lower values indicate better model accuracy and fit.

### 🧠 **7. Model Interpretability**

* Used **SHAP (SHapley Additive Explanations)** to explain individual predictions.
* Identified top influencing factors:

  * **pH** (acidic environments increase corrosion rate)
  * **\[Cl⁻]** (halide ions accelerate corrosion)
  * **Δχ, δ** (electronegativity difference, lattice distortion)
  * **Cr** (passivation), **Cu** (oxidation tendency)



## 📊 **Results & Findings**

| Parameter | Best Model | R² Score |
| --------- | ---------- | -------- |
| **Icorr** | XGBoost    | 0.81     |
| **Ecorr** | GBDT       | 0.84     |

* **XGBoost** showed best performance for predicting Icorr (corrosion rate).
* **GBDT** excelled in predicting Ecorr (corrosion potential).
* Validation on **new experimental HEA dataset** confirmed high generalization with relative errors within acceptable limits.


## 🧪 **Experimental Validation**

* Constructed a dataset of **3 new HEAs** prepared in-house using **vacuum arc melting**.
* Electrochemical tests performed in **3.5 wt% NaCl** using Tafel extrapolation.
* Model predictions closely matched lab results.


## 🔮 **Future Enhancements**

* Expand dataset with more HEA systems and broader environmental conditions.
* Integrate **Deep Learning (DL)** models for complex pattern recognition.
* Develop a **web-based prediction interface** or API for public usage.
* Extend framework to include **corrosion under stress and fatigue** environments.
