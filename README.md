Placement Prediction using Logistic Regression

GDSC AI/ML Inductions - Beginner Task 1

📌 Problem Statement

The objective of this project is to predict whether a student will be Placed or NotPlaced based on academic performance, skills, and training-related attributes. This is formulated as a binary classification problem.

📂 Dataset Description

The dataset contains student-level information with 10,000 rows and 12 columns, where each row represents an individual student.

Key feature groups include:
Academic performance (CGPA, SSC Marks, HSC Marks)
Experience and skills (Internships, Projects, Workshops/Certifications)
Aptitude and soft skills (Aptitude Test Score, Soft Skills Rating)
Other factors (Extracurricular Activities, Placement Training)
The target variable is PlacementStatus (Placed / NotPlaced).

🔍 Exploratory Data Analysis (EDA)
EDA was performed to understand the structure, validity, and trends in the dataset.

Key Observations:
The dataset contains 10,000 rows and 12 columns, with no missing values and appropriate data types.
There are more NotPlaced students than Placed students, indicating a slight class imbalance.
Placed students generally have a higher median CGPA compared to NotPlaced students.
However, the Placed group also contains notable low-CGPA outliers (~6.5), suggesting that factors beyond CGPA influence placement outcomes.

🧠 Model Selection

Logistic Regression was used as it is well-suited for binary classification problems and offers interpretability at a beginner level.

⚙️ Data Preprocessing

Removed non-informative columns such as StudentID
Converted categorical Yes/No features into numerical format using one-hot encoding

Split the dataset into:
80% training data
20% testing data

A fixed random_state = 1 was used to ensure reproducibility.

🧪 Model Training and Interpretation

The Logistic Regression model was trained on the training dataset.
After training, the model coefficients and intercept were examined to understand feature influence:
Features related to aptitude, placement training, extracurricular activities, and academic performance showed stronger positive influence on placement likelihood.
Some features contributed minimally, indicating weaker predictive power.
The intercept represents the baseline likelihood of placement when all feature values are zero.
This analysis helped confirm that placement outcomes are influenced by multiple factors, not a single metric.

📊 Model Evaluation

The trained model was evaluated on unseen test data using accuracy as the metric.

Accuracy achieved: 0.808

This comfortably exceeds the required 60% accuracy threshold.

🎯 Sample Prediction

A random student from the test set was selected to:
Observe the model’s prediction
Compare it with the actual placement outcome

This step helped verify the model’s behavior on individual unseen examples.

📌 Conclusion

The model demonstrates that student placement can be predicted with reasonable accuracy using academic, skill-based, and training-related features. While CGPA is an important factor, the presence of low-CGPA placed students highlights the role of aptitude, training, and extracurricular involvement.

🛠️ Technologies Used

Python,
Pandas,
Matplotlib, Seaborn,
Scikit-learn

