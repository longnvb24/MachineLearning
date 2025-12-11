# 🚢 Titanic Survivor Prediction: Logistic Regression vs. Naive Bayes

## 📌 Project Overview
The sinking of the RMS Titanic is one of the most infamous shipwrecks in history. This project aims to build a Machine Learning model to predict which passengers survived the tragedy based on their personal characteristics (age, gender, class, etc.).

This project serves as a comparative study between two fundamental classification algorithms: **Logistic Regression** and **Naive Bayes**, implemented using Python and Scikit-Learn.

## 📊 Dataset
- **Source:** Kaggle Titanic Dataset.
- **Input File:** `titanic.csv`
- **Key Features:**
  - `Pclass`: Ticket class (1st, 2nd, 3rd) - a proxy for socio-economic status.
  - `Sex`: Gender of the passenger.
  - `Age`: Age in years.
  - `SibSp` / `Parch`: Number of siblings/spouses and parents/children aboard.
  - `Fare`: Passenger fare.
  - `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).
- **Target:** `Survived` (0 = No, 1 = Yes).

## 🛠 Tech Stack
- **Language:** Python 3.x
- **Libraries:**
  - **Pandas & NumPy:** For data manipulation and numerical operations.
  - **Matplotlib & Seaborn:** For Exploratory Data Analysis (EDA) and visualization.
  - **Scikit-Learn:** For data preprocessing (LabelEncoding), model building, and evaluation.

## ⚙️ Methodology

### 1. Data Cleaning & Preprocessing
- **Handling Missing Values:** - Filled missing `Age` values using the mean/median.
  - Dropped columns with excessive missing data or low predictive value (e.g., `Cabin`, `Name`, `Ticket`).
- **Encoding Categorical Data:** Converted text data (e.g., `Sex`, `Embarked`) into numerical format suitable for machine learning models.
- **Feature Selection:** Selected the most relevant features to avoid overfitting.

### 2. Modeling
Two classification models were trained and evaluated:
1.  **Logistic Regression:** A statistical model that uses a logistic function to model a binary dependent variable. It serves as a strong baseline.
2.  **Naive Bayes (GaussianNB):** A probabilistic classifier based on Bayes' theorem with an assumption of independence between features.

## 📈 Results & Evaluation
The models were evaluated using the **Accuracy Score** and **Confusion Matrix**.

| Model | Accuracy |
|-------|----------|
| **Logistic Regression** | ~80% |
| **Naive Bayes** | ~78% |

*(Detailed classification reports and confusion matrices can be found in the notebook)*

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/longnvb24/MachineLearning.git](https://github.com/longnvb24/MachineLearning.git)

## Author
longnvb24
