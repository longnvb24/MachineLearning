# Fake News Detection using Bi-Directional LSTM

## 📌 Project Overview
This project aims to build a Deep Learning model capable of detecting fake news with high accuracy. In an era of misinformation, automating the classification of news articles as "Real" or "Fake" is crucial.

The project utilizes **Natural Language Processing (NLP)** techniques for data cleaning and implements a **Bi-Directional LSTM (Long Short-Term Memory)** neural network using TensorFlow/Keras.

## 📊 Dataset
The dataset consists of two CSV files containing news articles:
- **True.csv**: Articles from legitimate sources (e.g., Reuters).
- **Fake.csv**: Articles collected from unreliable sources.

*Data processing steps include combining title, text, and subject columns to create a comprehensive input feature.*

## 🛠 Tech Stack
- **Language:** Python 3.x
- **Deep Learning:** TensorFlow, Keras
- **NLP:** NLTK, Gensim
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, WordCloud

## ⚙️ Methodology

### 1. Data Preprocessing
- **Text Cleaning:** Removed special characters, converted to lowercase, and filtered out short words using `gensim`.
- **Stopwords Removal:** Utilized NLTK stopwords and custom domain-specific stopwords (e.g., 're', 'edu', 'subject') to reduce noise.
- **Tokenization:** Converted text to sequences of integers.
- **Padding:** Standardized input length to **40 tokens** to focus on the most informative parts of the articles (Title & Lead paragraph).

### 2. Model Architecture
The model is built using the Keras Sequential API:
1.  **Embedding Layer:** Converts integer sequences into dense vectors of size 128.
2.  **Bi-Directional LSTM:** (128 units) Captures context from both past and future words, essential for understanding sentence structure.
3.  **Dense Layer:** (128 units, ReLU activation) Extracts high-level features.
4.  **Output Layer:** (1 unit, Sigmoid activation) Outputs a probability score (0 for True, 1 for Fake).

### 3. Training Configuration
- **Optimizer:** Adam
- **Loss Function:** Binary Crossentropy
- **Metrics:** Accuracy
- **Epochs:** 2 (Due to fast convergence)
- **Batch Size:** 64

## 📈 Results
The model achieves exceptional performance on the test set:

- **Accuracy:** ~99%
- **Precision / Recall:** High scores across both classes.

*(Refer to the Confusion Matrix and Classification Report in the notebook for detailed metrics)*

## 🚀 How to Run
1. Clone the repository.
2. Install the required dependencies:
   ```bash
   pip install pandas numpy tensorflow nltk gensim sklearn matplotlib seaborn

## Author
