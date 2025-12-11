# 🎗️ Breast Cancer Prediction using Deep Learning

## 📌 Project Overview
This project applies **Deep Learning (Artificial Neural Networks - ANN)** to classify breast cancer tumors as **Malignant (M)** or **Benign (B)**.

Early diagnosis of breast cancer can significantly improve survival rates. This project utilizes the Wisconsin Breast Cancer Diagnostic dataset to train a binary classification model that predicts the diagnosis based on cell nuclei characteristics extracted from digitized images of Fine Needle Aspirate (FNA).

## 📊 Dataset
- **Source:** Wisconsin Breast Cancer Diagnostic Dataset.
- **Input File:** `breast_cancer_prediction.csv`
- **Instances:** 569 patients.
- **Features:** 30 numerical features describing the characteristics of cell nuclei (Radius, Texture, Perimeter, Area, Smoothness, etc.).
- **Target:** `diagnosis` (M = Malignant, B = Benign).

## 🛠 Tech Stack
- **Language:** Python 3.x
- **Deep Learning:** TensorFlow / Keras
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Preprocessing:** Scikit-Learn (LabelEncoder, StandardScaler)

## ⚙️ Methodology

### 1. Data Preprocessing & EDA
- **Data Cleaning:** Removed unnecessary columns (e.g., `id`, `Unnamed: 32`).
- **Label Encoding:** Converted the target variable `diagnosis` into numerical format (M = 1, B = 0).
- **Correlation Analysis:** Used Heatmaps to identify highly correlated features and multicollinearity.
- **Feature Scaling:** Applied **StandardScaler** to normalize the data. *This is a crucial step for Neural Networks to ensure faster convergence and prevent features with larger magnitudes (like Area) from dominating the model.*

### 2. Model Architecture
The model is built using a Feed-Forward Neural Network (ANN) with the Keras Sequential API:
- **Input Layer:** Matches the number of features.
- **Hidden Layers:** Dense layers with **ReLU** activation function to capture non-linear patterns.
- **Dropout Layers:** (Optional) Added to prevent overfitting.
- **Output Layer:** 1 unit with **Sigmoid** activation (standard for binary classification).

### 3. Training
- **Optimizer:** Adam
- **Loss Function:** Binary Crossentropy
- **Metrics:** Accuracy

## 📈 Results
The model was evaluated on the test set with the following performance metrics:

- **Accuracy:** ~96%
- **Confusion Matrix:** Shows a low number of False Negatives (Critical for medical diagnosis).

*(Please refer to the notebook for the detailed classification report and loss/accuracy graphs).*

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/longnvb24/MachineLearning.git](https://github.com/longnvb24/MachineLearning.git)

## Author
longnvb24 
