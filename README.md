❤️ Heart Stroke Prediction — Streamlit App
Streamlit AppPythonscikit-learnLicense: MIT

A machine learning web application that predicts the risk of heart disease based on clinical features. Built with Python, scikit-learn, and deployed via Streamlit.

🔗 Live App: https://sarthak939-heart-stroke-streamlit-app-wg4d9b.streamlit.app/

📌 Overview
This project covers the full lifecycle of a machine learning solution:

📥 Data Loading & Cleaning
🔍 Exploratory Data Analysis (EDA)
⚙️ Feature Engineering & Preprocessing
🤖 Model Building & Evaluation
🚀 Web App Deployment via Streamlit
The final deployed app lets users enter their clinical details and instantly get a prediction on their heart disease risk using a K-Nearest Neighbors (KNN) classifier.

🚀 Live Demo
👉 Try the app here: heart-stroke-streamlit on Streamlit Cloud

Enter patient details (age, chest pain type, cholesterol, etc.) and the model will predict whether the patient is at High Risk or Low Risk of heart disease.

🧠 Features
Interactive UI — Input patient data via sliders and dropdowns
Real-time Prediction — KNN model inference on the fly
One-hot Encoding Handling — Categorical inputs are automatically encoded to match model training format
Feature Scaling — Inputs are normalized using the saved StandardScaler
Clear Output — Visual ✅ / ⚠️ result messages
📊 Dataset
The project uses the Heart Failure Prediction Dataset (commonly sourced from Kaggle / UCI).

Feature	Description
Age	Age of the patient (years)
Sex	Biological sex (M / F)
ChestPainType	ATA, NAP, TA, ASY
RestingBP	Resting blood pressure (mm Hg)
Cholesterol	Serum cholesterol (mg/dL)
FastingBS	Fasting blood sugar > 120 mg/dL (1 = True, 0 = False)
RestingECG	Resting ECG results (Normal, ST, LVH)
MaxHR	Maximum heart rate achieved
ExerciseAngina	Exercise-induced angina (Y / N)
Oldpeak	ST depression induced by exercise
ST_Slope	Slope of peak exercise ST segment (Up, Flat, Down)
HeartDisease	Target — 1: Heart Disease, 0: Normal
🔬 ML Pipeline (EDA_HEART.ipynb)
The Jupyter notebook walks through the complete data science pipeline:

Data Loading — Import and inspect the dataset
Data Cleaning — Handle missing values, outliers, and zero-valued cholesterol
EDA — Visualize distributions, correlations, and feature relationships
Feature Engineering — One-hot encode categorical variables
Train/Test Split — Stratified split to preserve class balance
Scaling — StandardScaler applied to numeric features
Model Training — KNN Classifier with hyperparameter tuning
Evaluation — Accuracy, Confusion Matrix, Classification Report
Model Export — Save model, scaler, and column list as .pkl files
🗂️ Repository Structure
heart-stroke-streamlit/
│
├── EDA_HEART.ipynb          # Full EDA, preprocessing & model training notebook
├── app.py                   # Streamlit web application
├── requirements.txt         # Python dependencies
│
├── knn_heart_model.pkl      # Trained KNN classification model
├── heart_scaler.pkl         # Fitted StandardScaler
├── heart_columns.pkl        # Expected feature columns (post one-hot encoding)
│
├── fetch.env                # Environment configuration
└── .devcontainer/           # Dev container configuration (GitHub Codespaces)
🛠️ Tech Stack
Layer	Technology
Language	Python 3.8+
ML Library	scikit-learn
Data Processing	pandas, numpy
Model Serialization	joblib
Web Framework	Streamlit
Deployment	Streamlit Cloud
⚙️ Run Locally
1. Clone the repository
bash
git clone https://github.com/sarthak939/heart-stroke-streamlit.git
cd heart-stroke-streamlit
2. Install dependencies
bash
pip install -r requirements.txt
3. Run the Streamlit app
bash
streamlit run app.py
The app will open at http://localhost:8501 in your browser.

🤖 Model Details
Property	Value
Algorithm	K-Nearest Neighbors (KNN)
Preprocessing	StandardScaler (z-score normalization)
Encoding	One-hot encoding for categorical features
Output	Binary classification — Heart Disease (1) or Normal (0)
📈 How the App Works
User inputs clinical parameters via the sidebar/form
Inputs are mapped into a one-hot encoded DataFrame matching the training schema
Missing encoded columns are filled with 0
The input is scaled using the saved StandardScaler
The KNN model predicts the class
Result is displayed:
✅ Low Risk of Heart Disease
⚠️ High Risk of Heart Disease
👤 Author
Sarthak Verma

GitHub: @sarthak939
📄 License
This project is licensed under the MIT License.

⭐ If you found this project useful, please consider giving it a star!

