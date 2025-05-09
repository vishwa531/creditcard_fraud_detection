# Credit Card Fraud Detection

### 📜 Overview
This project aims to detect fraudulent credit card transactions using machine learning. The model is trained on a dataset of credit card transactions, using features such as transaction amount, time, and others to classify whether a transaction is fraudulent or not. The project includes data preprocessing, handling class imbalance, model training, evaluation, and hyperparameter tuning.

---

### 🛠️ Tools & Technologies
- **Python**: Core programming language for the project.
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Scikit-learn**: For building and evaluating machine learning models.
- **Matplotlib/Seaborn**: For data visualization.
**imbalanced-learn (SMOTE)**: For handling class imbalance in the dataset.
- **Flask**: For deploying the trained model as an API (optional).

---

### 🚀 Installation

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/vishwa531/creditcard_fraud_detection
    cd credit-card-fraud-detection
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

### 📊 Dataset

This project uses the **Credit Card Fraud Detection Dataset** available on [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). It contains transactions, including features such as transaction time, amount, and a class label (`1` for fraudulent transactions and `0` for non-fraudulent transactions).

- **Features**:
  - `trans_date_trans_time`: Timestamp of the transaction
  - `cc_num`: Credit card number (anonymized)
  - `merchant`: Merchant name
  - `category`: Merchant category
  - `amt`: Transaction amount
  - `city`, `state`, `zip`, `lat`, `long`: Location details
  - `gender`, `job`, `dob`: Demographic info
  - `is_fraud`: Target variable (0 = Not Fraud, 1 = Fraud)

---

### 📝 How to Run the Project

1. **Data Preprocessing**: The dataset undergoes preprocessing, which includes normalizing certain features and handling class imbalance (fraudulent transactions are much rarer than non-fraudulent ones).
  
2. **Model Training**: A Random Forest Classifier is trained on the processed data to distinguish between fraudulent and non-fraudulent transactions.

3. **Model Evaluation**: After training, the model's performance is evaluated using metrics such as **Precision**, **Recall**, **F1-Score**, and a **Confusion Matrix**.

---

### ⚙️ How to Use

1. **Run the Script**: Execute the Python script to preprocess the data, train the model, and evaluate the performance.
   
2. **Deploy the Model** (Optional): If you want to deploy the trained model as an API, you can use Flask. After training and saving the model (`fraud_model.pkl`), the Flask app serves the model as an API. You can send a POST request to `/predict` with transaction data to get predictions.

---

## 🧹 Data Preprocessing

- Converted `trans_date_trans_time` into `hour`, `day`, and `month` features.
- Dropped non-useful columns (`first`, `last`, `dob`, `trans_num`, `street`).
- Encoded categorical variables using Label Encoding.
- Handled class imbalance (optional using SMOTE).

---

## 🔥 Model Training

- Model Used: **Random Forest Classifier**
- Splitting dataset into training and testing sets (80/20 split).
- Trained model on the processed dataset.

---

### 🙌 Acknowledgments

- Special thanks to the creators of the **Credit Card Fraud Detection Dataset** on Kaggle for providing a high-quality dataset for this project.

---

## 📚 Conclusion

Random Forest performed well on the credit card fraud detection task, showing high precision and recall. Fraud detection is a critical area where minimizing false negatives (missing frauds) is as important as minimizing false positives.

---

## ✍️ Author

- **Vishwa Tailor**
- Data Science Learner | Bachelor of Engineering Student 
- Project as part of Data Science Assignment


