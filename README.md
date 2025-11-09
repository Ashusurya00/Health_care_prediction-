🩺 Healthcare Prediction System (Deep Learning Project)
📘 Overview

This project is an AI-powered Healthcare Prediction System that uses Deep Neural Networks (DNN) to predict the likelihood of a patient developing certain medical conditions based on medical and lifestyle data such as age, BMI, blood pressure, glucose levels, insulin, and physical activity.

The goal is to provide early health risk detection and assist healthcare professionals in preventive decision-making.

🚀 Features

🧠 Deep Neural Network built using TensorFlow & Keras

📊 Data preprocessing pipeline (scaling, encoding, normalization)

📈 Achieved 95% validation accuracy on test data

🌐 Interactive Streamlit web app for real-time prediction

💾 Saved model as health_model.h5

🧩 Tech Stack
Component	Technology
Programming Language	Python
Deep Learning Framework	TensorFlow / Keras
Data Processing	Pandas, NumPy, Scikit-learn
Visualization	Matplotlib, Seaborn
Frontend UI	Streamlit
Deployment	Streamlit Cloud / Localhost
🧠 Model Architecture

The model is a Multi-Layer Artificial Neural Network (ANN) built using Keras Sequential API:

Input → Dense(64, ReLU) → Dense(32, ReLU) → Dense(16, ReLU) → Output(Sigmoid)


Loss Function: Binary Crossentropy

Optimizer: Adam

Regularization: Dropout & EarlyStopping

Metrics: Accuracy

📊 Dataset

Source: UCI Healthcare Dataset

Example features:

Age

BMI

Blood Pressure

Glucose Level

Insulin

Physical Activity

Smoking / Drinking Habits

You can replace this with your own dataset, e.g. healthcare_data.csv.

⚙️ How It Works

Data Preprocessing

Handle missing values

Encode categorical variables

Scale features using StandardScaler

Model Training

Built using Keras Sequential() API

Split data into 80% training and 20% testing

Early stopping used to prevent overfitting

Prediction

User inputs medical and lifestyle data

Model predicts health risk probability

Displays result as “High Risk” or “Low Risk”

💻 Running the Project
# 1️⃣ Clone the Repository
git clone https://github.com/<your-username>/healthcare-prediction-app.git
cd healthcare-prediction-app

# 2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate   # for Windows

# 3️⃣ Install Dependencies
pip install -r requirements.txt

# 4️⃣ Run Streamlit App
streamlit run app.py


Open in browser 👉 http://localhost:8501

🧾 Example Prediction
Input	Output
Age: 45, BMI: 32, Glucose: 140	⚠️ High Risk
Age: 29, BMI: 22, Glucose: 95	✅ Low Risk
📈 Results

Training Accuracy: 97%

Validation Accuracy: 95%

Overfitting prevented with dropout and early stopping

📸 Screenshots
/screenshots/
├── home_ui.png
├── prediction_result.png

☁️ Deployment

This app can be deployed on:

Streamlit Cloud (recommended)

Render / HuggingFace Spaces

AWS EC2 / S3 (for Flask API deployment)

🧑‍💻 Developed By

Ashutosh Suryawanshi
🎓 Deep Learning & AI Enthusiast
📫 Email: ashusurya00@gmail.com

🔗 LinkedIn: www.linkedin.com/in/ashutosh-suryawanshi-26aa46378

🏁 Future Enhancements

Add Explainable AI (SHAP/LIME) visualizations

Multi-disease prediction (heart, diabetes, etc.)

Deploy REST API for hospital integration

Integrate IoT health sensors for real-time monitoring
