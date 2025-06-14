# 🛡️ Fraud Detection Using Machine Learning

## 📌 Problem Statement

Financial fraud is a critical challenge in today's digital economy, where online transactions are increasing rapidly. Detecting fraudulent transactions in real-time can help mitigate massive financial losses and safeguard both institutions and consumers. 

The objective of this project is to build a **machine learning model** capable of predicting fraudulent transactions with high accuracy and deploy it through an interactive **Streamlit** application.

---

## 📊 Dataset

- **Source:** [Kaggle - Credit Card Fraud Detection]([https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download&select=AIML+Dataset.csv))
- **Description:**  
  The dataset contains transactions made by European cardholders in September 2013. It includes 284,807 transactions, of which only 492 are fraud cases. Each transaction is described by 30 features:
  - `Time` and `Amount`
  - 28 anonymized principal components (`V1` to `V28`)
  - `Class` (Target variable: 0 for non-fraud, 1 for fraud)

---

## ⚙️ Project Workflow

### 1. Data Preprocessing
- Loaded and explored the dataset using `pandas` and `seaborn`
- Checked for missing values and understood the distribution
- Visualized feature correlation using a heatmap
- Dropped highly correlated features and unnecessary columns

### 2. Feature Engineering
- Scaled the `Amount` feature using `StandardScaler`
- Split data into features (X) and target variable (y)
- Converted categorical variables (if any) using `OneHotEncoder` via `ColumnTransformer`

### 3. Handling Class Imbalance
- Used **RandomUnderSampler** from the `imblearn` library to address class imbalance
- Reduced the number of majority class examples to balance the dataset for fair training

### 4. Model Building
- Built a **Logistic Regression** model using `scikit-learn`
- Evaluated model using:
  - Accuracy Score
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)
- Trained model was serialized using `joblib` and saved as `model.pkl`

### 5. Deployment
- Built a **Streamlit** app that:
  - Accepts user input through an interactive web interface
  - Loads the trained model (`model.pkl`)
  - Outputs whether the transaction is fraudulent or not
- Streamlit app provides an intuitive way to test the model without writing code

---

## 🛠️ How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/fraud-detection-streamlit.git
cd fraud-detection-streamlit
