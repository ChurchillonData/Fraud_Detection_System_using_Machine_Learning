# 🛡️ Fraud Detection Using Machine Learning

## 📌 Problem Statement

Financial fraud is a critical challenge in today's digital economy, where online transactions are increasing rapidly. Detecting fraudulent transactions in real-time can help mitigate massive financial losses and safeguard both institutions and consumers.

The objective of this project is to build a **machine learning model** capable of predicting fraudulent transactions with high accuracy and deploy it through an interactive **Streamlit** application.

---
## 🌐 Streamlit App Preview

Below is a preview of the deployed app interface:

![Fraud Detection UI]((https://github.com/ChurchillonData/Fraud_Detection_System_using_Machine_Learning/blob/main/Fraud_Detection_System_UI.png))


## 📊 Dataset

- **Source:** [Kaggle - Fraud Detection Dataset](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset)
resource=download&select=AIML+Dataset.csv)
- **Description:**  
  The dataset contains transactions made by European cardholders in September 2013. It includes 284,807 transactions, of which only 492 are fraud cases. Each transaction is described by 30 features:
  - `Time` and `Amount`
  - 28 anonymized principal components (`V1` to `V28`)
  - `Class` (Target variable: 0 for non-fraud, 1 for fraud)

---

## ⚙️ Project Workflow

### 1. Data Preprocessing

- Loaded and explored the dataset using `pandas` and `seaborn`
- Checked for missing values
- Visualized feature correlation using a heatmap
- Dropped highly correlated features and unnecessary columns

### 2. Feature Engineering

- Scaled the `Amount` feature using `StandardScaler`
- Split data into features (X) and target (y)
- Converted categorical variables using `OneHotEncoder` via `ColumnTransformer` (if applicable)

### 3. Handling Class Imbalance

- Used `RandomUnderSampler` from `imblearn` to address class imbalance
- Balanced the dataset to improve model fairness

### 4. Model Building

- Trained a **Logistic Regression** model using `scikit-learn`
- Evaluated the model using:
  - Accuracy score
  - Confusion matrix
  - Classification report (precision, recall, F1-score)
- Saved the model using `joblib` as `model.pkl`

### 5. Deployment

- Developed a **Streamlit** web application
  - Accepts user input via an intuitive UI
  - Loads the trained model (`model.pkl`)
  - Predicts whether a transaction is fraudulent or not
- Streamlit enables quick access and testing of the model without writing code

---

## 🛠️ How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/fraud-detection-streamlit.git
cd fraud-detection-streamlit
