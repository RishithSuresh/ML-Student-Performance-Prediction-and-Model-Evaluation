# ML Student Performance Prediction and Model Evaluation

## 📌 Project Overview

This project implements a complete **Machine Learning workflow for Student Performance Prediction and Model Evaluation** using a Student Performance dataset.

The project begins with **Exploratory Data Analysis (EDA)** to understand the factors associated with students' exam performance. It then applies **Linear Regression** to predict students' exam scores and **Logistic Regression** to classify students as **Pass or Fail** based on a 50-mark threshold.

The project also compares training and testing performance to identify possible **overfitting or underfitting** and concludes with meaningful insights about student performance.

---

## 🎯 Objectives

The main objectives of this project are:

* Perform Exploratory Data Analysis on student performance data.
* Identify numerical and categorical variables.
* Analyze distributions and relationships between variables.
* Identify missing values and potential outliers.
* Study factors associated with `exam_score`.
* Build a Linear Regression model to predict exam scores.
* Evaluate regression performance using standard evaluation metrics.
* Convert exam scores into a Pass/Fail classification problem.
* Build a Logistic Regression classification model.
* Evaluate classification performance using a confusion matrix, accuracy, precision, recall, and F1-score.
* Compare training and testing performance.
* Identify potential overfitting or underfitting.
* Derive five meaningful insights about student performance.

---

## 📊 Dataset

The dataset contains information about students' demographics, study habits, lifestyle, academic behavior, and exam performance.

### Features

| Feature                         | Description                                 |
| ------------------------------- | ------------------------------------------- |
| `student_id`                    | Unique identifier for each student          |
| `age`                           | Age of the student                          |
| `gender`                        | Gender of the student                       |
| `study_hours_per_day`           | Average daily study hours                   |
| `social_media_hours`            | Daily social media usage                    |
| `netflix_hours`                 | Daily Netflix/entertainment usage           |
| `part_time_job`                 | Whether the student has a part-time job     |
| `attendance_percentage`         | Percentage of classes attended              |
| `sleep_hours`                   | Average daily sleep duration                |
| `diet_quality`                  | Quality of the student's diet               |
| `exercise_frequency`            | Frequency of exercise                       |
| `parental_education_level`      | Education level of the student's parents    |
| `internet_quality`              | Quality of internet access                  |
| `mental_health_rating`          | Student's mental health rating              |
| `extracurricular_participation` | Participation in extracurricular activities |
| `exam_score`                    | Final exam score                            |

---

## 🤖 Machine Learning Problems

### 1. Regression

The first machine learning task is to predict the continuous variable:

```text
exam_score
```

A **Linear Regression** model is used.

### Regression Metrics

The model is evaluated using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

---

### 2. Classification

The second task converts `exam_score` into a binary Pass/Fail target.

The passing threshold is:

```text
Exam Score >= 50 → Pass
Exam Score < 50  → Fail
```

A **Logistic Regression** model is used for classification.

### Classification Metrics

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## 🔍 Exploratory Data Analysis

The notebook performs several EDA operations, including:

### Dataset Exploration

* Dataset dimensions
* Data types
* Statistical summary
* Duplicate records
* Numerical and categorical feature identification

### Missing Value Analysis

Missing values are identified and analyzed before model training.

### Distribution Analysis

The project examines the distributions of numerical variables such as:

* Study hours
* Attendance
* Sleep hours
* Social media usage
* Netflix usage
* Exercise frequency
* Mental health rating
* Exam score

### Relationship Analysis

Relationships between important student characteristics and exam scores are visualized using scatter plots and regression lines.

### Correlation Analysis

A correlation matrix is generated to identify numerical variables that have stronger positive or negative relationships with `exam_score`.

### Outlier Analysis

Boxplots and the IQR method are used to identify potential outliers in numerical variables.

---

## ⚙️ Data Preprocessing

Before training the models, the data is prepared using a preprocessing pipeline.

### Numerical Features

Numerical features are standardized using:

```text
StandardScaler
```

### Categorical Features

Categorical features are converted into numerical representations using:

```text
OneHotEncoder
```

The preprocessing is implemented using a Scikit-learn `ColumnTransformer` and `Pipeline`.

This ensures that preprocessing is applied consistently to both training and testing data.

---

## 🧠 Models Used

### Linear Regression

Used for predicting the continuous exam score.

```text
Input Features
      ↓
Data Preprocessing
      ↓
Linear Regression
      ↓
Predicted Exam Score
```

### Logistic Regression

Used for predicting whether a student passes or fails.

```text
Input Features
      ↓
Data Preprocessing
      ↓
Logistic Regression
      ↓
Pass / Fail
```

---

## 📈 Model Evaluation

### Regression

The predicted exam scores are compared with actual scores using:

```text
MAE
MSE
RMSE
R² Score
```

An **Actual vs Predicted** plot and residual analysis are also performed.

### Classification

Classification performance is evaluated using:

```text
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
```

---

## 🔄 Training vs Testing Comparison

Training and testing performance is compared to determine how well the models generalize to unseen data.

### Overfitting

Overfitting may be indicated when:

```text
Training Performance >> Testing Performance
```

This means the model performs very well on the training data but significantly worse on unseen data.

### Underfitting

Underfitting may be indicated when:

```text
Training Performance ≈ Poor
Testing Performance ≈ Poor
```

### Good Generalization

A model is considered to generalize reasonably well when training and testing performance are relatively close and both show acceptable performance.

---

## 🛠️ Technologies Used

* **Python**
* **Jupyter Notebook / Google Colab**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**

---

## 📁 Project Structure

```text
ML-Student-Performance-Prediction/
│
├── student_performance.csv
│
├── ML_Student_Performance_Prediction.ipynb
│
├── README.md
│
└── requirements.txt
```

---

## 📦 Installation

Clone the repository:

```bash
git clone <your-github-repository-url>
```

Navigate to the project directory:

```bash
cd ML-Student-Performance-Prediction
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## 📋 Requirements

The project requires the following Python libraries:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

You can install them using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

---

## ▶️ How to Run

### Option 1: Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
ML_Student_Performance_Prediction.ipynb
```

Run the notebook cells sequentially.

### Option 2: Google Colab

1. Open Google Colab.
2. Upload the `.ipynb` notebook.
3. Upload `student_performance.csv`.
4. Run all cells.

---

## 📌 Key Findings

The analysis focuses on identifying how different student-related factors are associated with exam performance.

Important factors investigated include:

* Study time
* Attendance
* Sleep duration
* Social media usage
* Netflix usage
* Exercise
* Mental health
* Diet quality
* Parental education
* Internet quality
* Extracurricular participation
* Part-time employment

The final insights should be based on the actual relationships and model results observed in the dataset.

---

## 💡 Five Key Insights

The project concludes with five meaningful insights supported by the analysis.

Examples of areas investigated include:

1. **Study habits:** Whether increased study time is associated with higher exam scores.
2. **Attendance:** Whether students with higher attendance tend to perform better.
3. **Screen time:** Whether social media and entertainment usage show any relationship with academic performance.
4. **Well-being:** Whether sleep, exercise, and mental health are associated with exam scores.
5. **Predictive performance:** How effectively student characteristics can be used to predict exam scores and identify students likely to pass.

> **Note:** The final conclusions should be updated according to the actual results obtained from the dataset rather than assuming a relationship beforehand.

---

## 📊 Expected Outcomes

By completing this project, the following outcomes are produced:

* Comprehensive EDA of student performance.
* Identification of important numerical and categorical variables.
* Correlation analysis with exam scores.
* Identification of potential outliers.
* Linear Regression model for exam-score prediction.
* Regression performance metrics.
* Logistic Regression model for Pass/Fail prediction.
* Confusion matrix.
* Classification performance metrics.
* Training vs testing comparison.
* Overfitting/underfitting analysis.
* Five data-supported insights.

---

## 🚀 Future Improvements

The project can be extended by:

* Testing additional regression algorithms such as Random Forest and Gradient Boosting.
* Testing additional classification algorithms such as Decision Trees and Random Forest.
* Performing feature selection.
* Applying hyperparameter tuning.
* Using cross-validation.
* Comparing multiple machine learning models.
* Building an interactive student performance prediction application.
* Deploying the final model using Streamlit or Flask.
* Adding explainable AI techniques to understand individual predictions.

---

## 📜 License

This project is intended for **educational and academic purposes**.
