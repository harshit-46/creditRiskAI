# CreditRiskAI

### End-to-End Credit Default Risk Prediction System

CreditRiskAI is an **end-to-end machine learning system** designed to predict the probability of **loan default** using customer financial and demographic data.

The project demonstrates a **complete ML engineering workflow**, including data preprocessing, model training, API development, and containerized deployment using **FastAPI and Docker**.

This project is built using the **Home Credit Default Risk dataset** and aims to simulate how financial institutions assess **credit risk** before approving loans.

---

# 🚀 Features

* End-to-end **Machine Learning pipeline**
* **Feature engineering and preprocessing**
* **LightGBM model** for credit default prediction
* REST API built with **FastAPI**
* **Dockerized deployment**
* Interactive **Swagger API documentation**
* Production-style **project structure**

---

# 🧠 Problem Statement

Financial institutions must determine whether a loan applicant is likely to **repay the loan or default**.

Incorrect decisions can result in significant financial losses.

This project predicts the **probability of loan default** using historical applicant data.

Target variable:

```
TARGET

0 → Loan Repaid
1 → Loan Default
```

---

# 📊 Dataset

Dataset: **Home Credit Default Risk**
Source: Kaggle

The dataset contains information about:

* Applicant income
* Credit amount
* Employment status
* Credit history
* Demographic information
* Previous loan behavior

Main dataset used:

```
application_train.csv
```

---

# 🏗 Project Architecture

```
Client Request
      ↓
FastAPI Endpoint
      ↓
Data Preprocessing
      ↓
LightGBM Model
      ↓
Prediction
      ↓
JSON Response
```

---

# 📂 Project Structure

```
credit-risk-ai/

│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── eda.ipynb
│
├── src/
│   ├── preprocess.py
│   ├── train_model.py
│   ├── predict.py
│
├── models/
│   └── model.pkl
│
├── api/
│   └── main.py
│
├── requirements.txt
├── Dockerfile
├── .dockerignore
└── README.md
```

---

# ⚙️ Machine Learning Pipeline

The ML workflow follows these steps:

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Missing Value Handling
4. Categorical Feature Encoding
5. Feature Engineering
6. Train-Test Split
7. Model Training
8. Model Evaluation
9. Model Serialization
10. API Deployment

---

# 🤖 Model

The primary model used in this project is **LightGBM**.

Why LightGBM?

* Excellent performance on **tabular datasets**
* Handles **missing values**
* Faster training
* Captures **nonlinear feature interactions**

Evaluation metric:

```
ROC-AUC Score
```

---

# 🔌 API Endpoints

Base URL:

```
http://localhost:8000
```

Health check:

```
GET /
```

Prediction endpoint:

```
POST /predict
```

Example request:

```json
[120000, 500000, 35]
```

Example response:

```json
{
  "default_prediction": 1,
  "default_probability": 0.72
}
```

Interactive API documentation:

```
http://localhost:8000/docs
```

---

# 🐳 Docker Deployment

Build the Docker image:

```
docker build -t credit-risk-api .
```

Run the container:

```
docker run -p 8000:8000 credit-risk-api
```

Access the API:

```
http://localhost:8000/docs
```

---

# 💻 Local Development

Clone the repository:

```
git clone https://github.com/yourusername/credit-risk-ai.git
```

Navigate into the project:

```
cd credit-risk-ai
```

Install dependencies:

```
pip install -r requirements.txt
```

Run the API:

```
uvicorn api.main:app --reload
```

---

# 📈 Future Improvements

Possible enhancements:

* Advanced feature engineering
* Hyperparameter tuning
* Model monitoring
* MLflow experiment tracking
* CI/CD pipeline
* Cloud deployment (AWS / GCP)

---

# 🧰 Tech Stack

Machine Learning

* Python
* Scikit-learn
* LightGBM
* Pandas
* NumPy

Backend

* FastAPI
* Uvicorn

Deployment

* Docker

Visualization

* Matplotlib
* Seaborn

---

# 👨‍💻 Author

Harshit Gupta

Final Year B.Tech CSE (AI & Data Science) student building projects in:

* Machine Learning
* AI Engineering
* Full Stack Development

---

# ⭐ If you found this project useful

Please consider **starring the repository**.

Keep Learning