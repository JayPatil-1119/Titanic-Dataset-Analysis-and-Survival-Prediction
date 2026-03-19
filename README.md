# 🚢 Titanic Dataset Analysis & Survival Prediction using Machine Learning

## 📌 Project Overview

This project analyzes the Titanic dataset and builds a machine learning model to predict whether a passenger survived or not. The project focuses on understanding key factors influencing survival and building an optimized classification model.

---

## 🎯 Objective

* Analyze passenger data and identify survival patterns
* Perform data cleaning and preprocessing
* Build a classification model for survival prediction
* Evaluate model performance using multiple metrics

---

## 📊 Dataset Information

* Total Records: 891

* Features include passenger details such as:

  * Pclass (Passenger Class)
  * Sex
  * Age
  * Fare
  * Embarked
  * SibSp & Parch (combined later)

* Target Variable:

  * `Survived` → (0 = No, 1 = Yes)

---

## 🔍 Data Preprocessing

* Missing Values Handling:

  * Dropped `Cabin` (77% missing values)
  * Filled `Age` using median
  * Removed rows with missing `Embarked`

* Feature Engineering:

  * Created **FamilySize = SibSp + Parch**
  * Dropped unnecessary columns (PassengerId, Name, Ticket)

* Encoding:

  * Converted categorical features using **Ordinal Encoding**

* Feature Scaling:

  * Applied **MinMaxScaler** due to skewed data

---

## 📈 Exploratory Data Analysis (EDA)

* Dataset is imbalanced (more non-survivors than survivors)
* Key insights:

  * Females had higher survival rate
  * First-class passengers survived more
  * Passengers traveling alone had lower survival chances
  * Higher fare increased survival probability

---

## ⚙️ Model Building

### 🔹 Logistic Regression

* Accuracy: **~81%**
* ROC-AUC Score: **~0.80**

---

### 🔹 K-Nearest Neighbors (KNN)

* Initial model showed slight overfitting
* Optimized using hyperparameter tuning (best k ≈ 21)
* Final performance aligned with Logistic Regression

---

## 📊 Model Evaluation Metrics

* Accuracy Score
* Precision, Recall, F1-score
* Confusion Matrix
* ROC-AUC Curve

---

## 🔥 Threshold Optimization

* Default threshold (0.5) was adjusted to **0.43**
* Improved recall and overall model performance

---

## 🧠 Feature Selection

* Applied **Chi-Square Test**
* Selected important features:

  * Pclass
  * Sex
  * Fare
  * Embarked

---

## 🏆 Final Conclusion

* Logistic Regression performed well with balanced results
* Threshold tuning improved recall significantly
* Key survival factors:

  * Gender
  * Passenger class
  * Fare

---

## 📂 Project Structure

```bash id="f9bqv3"
Titanic-ML-Project/
│── titanic_analysis.ipynb
│── titanic.csv
│── README.md
│── requirements.txt
```

---

## ▶️ How to Run the Project

```bash id="c9q9zo"
pip install -r requirements.txt
jupyter notebook
```

---

## 🚀 Future Improvements

* Try advanced models (Random Forest, XGBoost)
* Deploy model using Streamlit
* Perform cross-validation for better generalization

---

## 🙌 Acknowledgements

* Kaggle Titanic Dataset
* Scikit-learn Documentation

---

## 📬 Contact

* GitHub: https://github.com/JayPatil-1119
* LinkedIn: www.linkedin.com/in/jay-patil-5b10422a7

---

⭐ If you like this project, give it a star!

