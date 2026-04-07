# 🏗️ Richter's Predictor Earthquake Damage Modeling using Machine Learning

## 📌 Overview
This project focuses on predicting the level of structural damage to buildings after an earthquake using supervised machine learning techniques. The goal is to support disaster response planning by identifying buildings that are more likely to suffer severe damage.

The dataset is derived from post-earthquake surveys and includes information about building structure, materials, geographic location, and usage. The problem is framed as a **multiclass classification task** with three damage levels.

---

## 🎯 Objective
- Predict building damage grade (Low, Medium, High)
- Handle class imbalance effectively
- Build a model that generalizes well on unseen data
- Evaluate performance using appropriate metrics (Macro F1)

---

## 📊 Dataset Description
The dataset contains a mix of:
- **Numerical features**: age, area, height, number of floors, etc.
- **Categorical features**: foundation type, roof type, land surface condition
- **Binary features**: presence of structural materials
- **Geographic features**: hierarchical location identifiers

These features capture both **structural vulnerability** and **geographical risk factors**.

---

## 🔍 Approach

### 1. Data Preprocessing
- Handled missing values and duplicates
- Encoded categorical variables
- Created a clean modeling dataset

### 2. Exploratory Data Analysis
- Studied class imbalance in damage grades
- Analyzed feature distributions and relationships
- Identified key risk indicators (age, materials, geo levels)

### 3. Feature Selection
- Used correlation and model-based importance
- Removed redundant and low-impact features

### 4. Handling Class Imbalance
- Experimented with SMOTE for some models
- Used model-based handling (e.g., class weighting) for tree models

### 5. Model Building
Trained and compared multiple models:
- Logistic Regression (baseline)
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

### 6. Hyperparameter Tuning
- Applied RandomizedSearchCV
- Focused on controlling overfitting and improving Macro F1

---

## 📈 Model Performance

| Model | Macro F1 (Test) |
|------|----------------|
| Logistic Regression | Lower baseline |
| Decision Tree | Overfitting observed |
| Random Forest | ~0.61 |
| Gradient Boosting | Improved performance |
| **XGBoost** | **0.6699 (Best)** |

> Macro F1-score was used as the primary metric due to class imbalance.

---

## 🧠 Key Observations
- Building-related features (age, material, floors) strongly influence damage
- Geographic features are critical predictors of risk
- Tree-based models outperform linear models on structured data
- Default parameters often lead to overfitting and require tuning

---

## ⚠️ Challenges Faced
- Handling imbalanced classes without distorting data
- Overfitting in tree-based and boosting models
- Increased computation time during hyperparameter tuning
- Choosing the right evaluation metric (accuracy was misleading)

---

## 📘 Learnings
- Macro F1-score provides a better evaluation than accuracy in imbalanced datasets
- SMOTE is not always beneficial for tree-based models
- Small train-test performance gaps indicate good generalization
- Model selection should balance performance and interpretability

---

## 🧭 Real-World Impact
This model can assist:
- Disaster management teams in prioritizing response
- Urban planners in identifying vulnerable zones
- Policy makers in improving building regulations

---
# 👩‍💻 Author

**Sejal Kumari**
Aspiring Data Scientist transitioning from manufacturing to analytics

---
# ⭐ Final Note

The focus of this project was not just achieving a higher score, but building a robust, interpretable, and generalizable model suitable for real-world scenarios.
