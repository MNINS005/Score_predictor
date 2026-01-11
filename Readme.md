
🎓 Student Performance Prediction – ML Web Application

An end-to-end Machine Learning web application that predicts student math scores based on demographic and academic attributes.
The project demonstrates industry-style ML engineering, from data preprocessing to model deployment using Flask.

📌 Project Objective

To build a reproducible and deployable ML system that:

preprocesses raw input data,

applies a trained ML model,

and serves predictions through a web interface.

This project focuses on correct ML pipeline design, not just model accuracy.

🧠 Machine Learning Approach
Key Concepts Used

Feature preprocessing using Pipeline & ColumnTransformer

Handling categorical and numerical data separately

Model comparison and hyperparameter tuning

Artifact-based inference (no retraining during prediction)

Models Evaluated

Linear Regression

Decision Tree Regressor

Random Forest Regressor

Gradient Boosting Regressor

AdaBoost Regressor

XGBoost Regressor

CatBoost Regressor

The final model is selected based on performance metrics and generalization ability.

🏗️ Project Structure
ML-project/
│
├── app.py                  # Flask application (entry point)
├── templates/              # HTML templates (UI)
│   ├── index.html
│   └── home.html
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   ├── train_pipeline.py
│   │   └── predict_pipeline.py
│   │
│   ├── utils.py
│   ├── logger.py
│   └── exceptions.py
│
├── artifacts/              # Trained model & preprocessor (ignored in Git)
├── requirements.txt
└── README.md

🔄 Application Workflow
User Input (Browser)
        ↓
Flask Backend
        ↓
Load preprocessor.pkl
        ↓
Transform input features
        ↓
Load model.pkl
        ↓
Predict math score
        ↓
Display result

⚙️ Setup & Installation
1️⃣ Clone Repository
git clone <repository-url>
cd ML-project

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows

3️⃣ Install Dependencies
pip install -r requirements.txt

▶️ Run the Application
python app.py


Open browser:

http://127.0.0.1:5000/

🧪 API Testing (Optional)

The backend can be tested independently using Postman:

Endpoint: /predictdata

Method: POST

Body Type: form-data

This helps verify backend and ML logic without relying on the frontend.

📦 Artifacts

Generated during training:

model.pkl – trained ML model

preprocessor.pkl – fitted preprocessing pipeline


📌 These files are stored in artifacts/ and excluded from version control
