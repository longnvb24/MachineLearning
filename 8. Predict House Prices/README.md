# 🏠 House Price Prediction App (India)

This project is a Machine Learning application designed to predict house prices in India based on key property characteristics. It demonstrates an end-to-end workflow from data selection and model comparison to deploying a user-friendly interface using **Streamlit**.

## 📌 Project Overview
The goal of this project is to build a predictive model that estimates housing prices. While the original dataset contains numerous attributes, this project focuses on a curated subset of **5 key features** identified as the most significant drivers of property value.

## 📊 Dataset
**Source:** Kaggle - House Price India Dataset.

**Selected Features:**
To improve model efficiency and focus on high-impact variables, the following features were selected:
1.  **Number of bedrooms**: Count of bedrooms.
2.  **Number of bathrooms**: Count of bathrooms.
3.  **Living area**: The size of the living area (in discrete units/sqft).
4.  **Condition of the house**: A rating indicating the condition of the property.
5.  **Number of schools nearby**: The proximity to educational institutions (an important factor for families).

## 🤖 Model Development
I experimented with several regression algorithms to determine the best approach for this specific dataset:

* **Linear Regression**: Used as a baseline model to establish linear relationships.
* **Decision Tree Regressor**: Implemented to capture non-linear patterns.
* **Random Forest Regressor**: Used an ensemble method to improve accuracy and reduce overfitting.

### 🏆 Results
After evaluating the models using **Mean Absolute Error (MAE)**, the **Random Forest Regressor** demonstrated the best performance, yielding the lowest error rate. This optimized model was saved using `joblib` for the deployment phase.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-learn
* **Model Persistence:** Joblib
* **Web Framework:** Streamlit

## 🚀 How to Run the App

### 1. Clone the repository (or download files)
Ensure `app.py`, `model.pkl`, and your dataset are in the same directory.

### 2. Install dependencies
Open your terminal and run:

```bash
pip install pandas numpy scikit-learn streamlit joblib
```
### 3. Run the Streamlit app
In the terminal, execute:

```bash
streamlit run app.py
```
### 4. Usage
Input the house details in the sidebar/main menu.

Click the "Predict" button.

The app will display the estimated price based on the Random Forest model.

👤 Author
longnvb24
