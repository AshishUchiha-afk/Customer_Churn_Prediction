# Customer_Churn_Prediction
A machine learning project to predict customer churn using classification algorithms and data analysis techniques. Helps businesses identify customers likely to leave and take proactive retention actions.
## ⚙️ How to Run the Code Without Hassle

Follow the steps below to get started easily:

1. 📥 **Run the following cell in the notebook:**

   ```python
   from google.colab import files
   files.upload()
2.🔐 Upload your Kaggle token (kaggle.json) when prompted.

3.✅ Now the code is ready to run — all necessary permissions and access will be set up!

## ⚙️ How to Set Up the Project Locally (Kaggle API Method)

Follow these steps if you want to use the Kaggle API to download the dataset directly:

1. 🔑 **Get Your Kaggle API Credentials**  
   - Go to your [Kaggle Account Settings](https://www.kaggle.com/account)
   - Click on **"Create New API Token"**
   - This will download a file called `kaggle.json`

2. 📁 **Place the Token File**  
   - Move `kaggle.json` to the `.kaggle` folder:
     - On Windows: `C:\Users\<YourUsername>\.kaggle\kaggle.json`
     - On macOS/Linux: `~/.kaggle/kaggle.json`

3. 🧠 **Use the Following Code to Programmatically Download the Dataset**

   ```python
   import os
   import kaggle

   # Set Kaggle credentials (optional if kaggle.json is correctly placed)
   os.environ['KAGGLE_USERNAME'] = 'your_username'
   os.environ['KAGGLE_KEY'] = 'your_key'

   # Download and unzip the dataset
   kaggle.api.dataset_download_files('dataset', path='.', unzip=True)

   ## 📌 Project Highlights

- 💡 Predicts customer churn using decision tree, random forest, and XGBoost classifiers
- 🧼 Handles missing values and performs label encoding
- ⚖️ Uses SMOTE to balance imbalanced classes
- 📈 Includes EDA, data preprocessing, model evaluation, and final prediction system
- 🧠 Model saved with Pickle for future predictions

---

## 🧠 Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Pickle

customer_churn_prediction/
├── customer_churn_prediction.py   → Main Python script
├── WA_Fn-UseC_-Telco-Customer-Churn.csv  → Dataset (after download)
├── customer_churn_model.pkl       → Trained model (generated)
├── encoders.pkl                   → Saved label encoders
└── README.md                      → Project documentation

🧪 Model Evaluation

✅ Random Forest achieved the highest accuracy with cross-validation

📊 Evaluation metrics include accuracy score, confusion matrix, and classification report

📌 Future Improvements

Add a Streamlit or Flask web app for live prediction

Use hyperparameter tuning with GridSearchCV
