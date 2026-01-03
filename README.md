# Placement Prediction using Logistic Regression  
**GDSC AI/ML Inductions - Beginner Task 1**

![task](https://img.shields.io/badge/Task-Beginner%201-blue)
![type](https://img.shields.io/badge/Type-Binary%20Classification-brightgreen)
![model](https://img.shields.io/badge/Model-Logistic%20Regression-orange)
![metric](https://img.shields.io/badge/Accuracy-0.808-success)

---

## 📌 Problem Statement
The objective of this project is to predict whether a student will be **Placed** or **NotPlaced** based on academic performance, skills, and training-related attributes.  
This is a **binary classification** problem.

---

## 📂 Dataset Description
The dataset contains student-level information with **10,000 rows** and **12 columns**, where each row represents an individual student.

### Key feature groups
- **Academic performance:** CGPA, SSC Marks, HSC Marks  
- **Experience and skills:** Internships, Projects, Workshops/Certifications  
- **Aptitude and soft skills:** Aptitude Test Score, Soft Skills Rating  
- **Other factors:** Extracurricular Activities, Placement Training  

**Target variable:** `PlacementStatus` (Placed / NotPlaced)

---

## 🔍 Exploratory Data Analysis (EDA)
EDA was performed to understand the structure, validity, and trends in the dataset.

### Key observations
- The dataset has **no missing values** and appropriate data types.
- There are more **NotPlaced** students than **Placed** students → slight class imbalance.
- **Placed** students generally have a higher median **CGPA** than **NotPlaced** students.
- Low-CGPA outliers (~6.5) exist in the Placed group, suggesting placement depends on factors beyond CGPA.

---

## 🧠 Model Selection
**Logistic Regression** was used because it is well-suited for binary classification and offers good interpretability at a beginner level.

---

## ⚙️ Data Preprocessing
- Removed non-informative columns such as `StudentID`
- Converted categorical Yes/No features into numerical format using **one-hot encoding**

### Train–test split
- **80%** training data  
- **20%** testing data  
- Used `random_state = 1` for reproducibility

---

## 🧪 Model Training and Interpretation
The Logistic Regression model was trained on the training dataset. After training, coefficients and intercept were examined to understand feature influence.

- Features related to **aptitude**, **placement training**, **extracurricular activities**, and **academic performance** showed stronger positive influence.
- Some features contributed minimally, indicating weaker predictive power.
- The **intercept** represents the baseline likelihood of placement when all feature values are zero.

---

## 📊 Model Evaluation
The trained model was evaluated on unseen test data using **accuracy**.

✅ **Accuracy achieved:** `0.808`  
This exceeds the required **60%** accuracy threshold.

---

## 🎯 Sample Prediction
A random student from the test set was selected to:
- observe the model’s prediction
- compare it with the actual placement outcome

This helped verify the model’s behavior on an individual unseen example.

---

## 📌 Conclusion
The model demonstrates that student placement can be predicted with reasonable accuracy using academic, skill-based, and training-related features.  
While CGPA is important, low-CGPA placed students highlight the role of **aptitude, training, and extracurricular involvement**.

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- Matplotlib, Seaborn  
- Scikit-learn  
