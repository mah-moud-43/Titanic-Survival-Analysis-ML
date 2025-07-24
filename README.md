# Titanic Survival Analysis & Prediction

This project focuses on analyzing the Titanic passenger dataset to uncover patterns related to survival rates and building machine learning models to predict the likelihood of survival for new passengers.

The dataset includes demographic and travel information for over 800 passengers aboard the Titanic, allowing for both statistical analysis and predictive modeling.

## 🎯 Objectives

- Understand survival patterns by exploring demographic and ticket-related features.
- Identify key factors that influenced survival.
- Build and evaluate predictive models for survival classification.
- Interpret model outputs to inform data-driven storytelling.

## 📊 Exploratory Data Analysis (EDA)

Through EDA, the following insights were discovered:

- **Gender** played a major role: ~74% of females survived vs. ~19% of males.
- **Class** mattered: First-class passengers had a much higher survival rate.
- **Children** (under age 10) had higher chances of survival.
- **Fare** and **embarkation port** showed some correlation with survival rates.
- **Alone vs. Family**: Passengers traveling with family had better survival odds.

## 🔍 Key Features Considered

- `Pclass` (Ticket class)
- `Sex`
- `Age`
- `SibSp` (Number of siblings/spouses aboard)
- `Parch` (Number of parents/children aboard)
- `Fare`
- `Embarked`
- `Alone` (engineered feature)
- `Title` (extracted from Name)
- `AgeGroup` (binned)

## 🤖 Machine Learning Models Used

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)

Models were evaluated using:

- Accuracy  
- Precision / Recall / F1 Score  
- Confusion Matrix  
- ROC-AUC Curve  

**Best-performing model:** Random Forest (Accuracy ~84%)

## 🧠 Notable Techniques

- Feature engineering (`Alone`, `Title`, `AgeGroup`)
- Handling missing data using imputation strategies
- Label encoding and one-hot encoding
- Hyperparameter tuning with GridSearchCV
- Model evaluation using cross-validation

## 📁 Files Included

- `titanic_analysis.ipynb` – Full EDA and visualizations
- `titanic_modeling.ipynb` – ML models and evaluation
- `data/` – CSV files: train & test datasets
- `submission.csv` – Sample Kaggle submission

## 📌 FAQs

### ❓ What is the purpose of this project?
To analyze the Titanic dataset for patterns in survival and build accurate models that can predict whether a given passenger would survive.

### ❓ Why was Random Forest the best model?
Random Forest performed best due to its ability to capture non-linear relationships, reduce overfitting through ensemble learning, and handle both numerical and categorical features well.

### ❓ How were missing values handled?
- `Age`: Imputed using median grouped by `Title`
- `Embarked`: Filled with mode
- `Fare`: Imputed with median for that `Pclass`

### ❓ Which features were most important?
Feature importance from the Random Forest model highlighted:
- `Sex`
- `Pclass`
- `Fare`
- `Age`
- `Title`

### ❓ What can be improved in the future?
- Use of deep learning models
- More advanced feature extraction (e.g., social status, cabin deck)
- Integration with external datasets

## 🧠 What I Learned

- Translating real-world data into usable ML features
- Performing thorough exploratory data analysis (EDA)
- Building, tuning, and evaluating machine learning models
- Communicating insights clearly through data storytelling

---

## 🚀 Try It Yourself

To run the project:

```bash
git clone https://github.com/your-username/Titanic-Survival-Analysis-ML.git
cd Titanic-Survival-Analysis-ML
open titanic_analysis.ipynb
