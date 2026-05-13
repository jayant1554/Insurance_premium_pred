# 🏥 Insurance Premium Prediction — End-to-End MLOps Pipeline

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.x-green.svg)
![AWS](https://img.shields.io/badge/AWS-Elastic%20Beanstalk-orange.svg)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-black.svg)
![Accuracy](https://img.shields.io/badge/Accuracy-88%25+-brightgreen.svg)

A production-ready, end-to-end machine learning pipeline for predicting insurance premium charges based on user demographics and health data. Built with a modular MLOps architecture, deployed on AWS Elastic Beanstalk with an automated CI/CD pipeline.

🔗 **Live Demo:** [insurance-premium-pred.vercel.app](https://insurance-premium-pred.vercel.app)

---

## 📌 Problem Statement

Insurance companies need to accurately estimate premium charges for customers based on factors like age, BMI, smoking habits, and region. Manual estimation is slow and inconsistent. This project automates that prediction using a machine learning model, providing real-time estimates via a web interface.

---

## 🏗️ Architecture

```
User Input (Web Form)
        ↓
Flask Web App (application.py)
        ↓
Prediction Pipeline (src/pipelines/)
        ↓
Data Transformation → Model Inference
        ↓
Predicted Premium (₹) returned to UI
```

**CI/CD Flow:**
```
GitHub Push → GitHub Actions → Build & Test → Deploy to AWS Elastic Beanstalk
```

---

## ✨ Features

- **Real-time prediction** of insurance premium from user inputs
- **Modular pipeline** — separate components for ingestion, transformation, training, and prediction
- **88%+ model accuracy** achieved through systematic feature engineering and hyperparameter tuning
- **CI/CD pipeline** with GitHub Actions for automated testing and deployment
- **Production deployment** on AWS Elastic Beanstalk
- **Clean web UI** with multiple pages (Home, About, Features, Contact, Predict)

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.8+ |
| ML Libraries | Scikit-learn, Pandas, NumPy |
| Web Framework | Flask |
| Deployment | AWS Elastic Beanstalk, Vercel |
| CI/CD | GitHub Actions |
| Model Storage | Artifacts folder (pickle files) |
| Packaging | setup.py |

---

## 📊 Input Features

| Feature | Type | Description |
|---|---|---|
| Age | Integer | Age of the insured person |
| BMI | Float | Body Mass Index |
| Children | Integer | Number of dependents |
| Sex | Categorical | Male / Female |
| Smoker | Categorical | Yes / No |
| Region | Categorical | Northeast / Northwest / Southeast / Southwest |

---

## 📁 Project Structure

```
Insurance_premium_pred/
├── src/
│   ├── components/          # Data ingestion, transformation, model trainer
│   ├── pipelines/           # Training & prediction pipelines
│   └── utils.py             # Helper functions
├── artifacts/               # Saved model & preprocessor
├── templates/               # HTML templates (Jinja2)
├── static/                  # CSS styles
├── notebook/                # EDA & experimentation
├── .ebextensions/           # AWS Elastic Beanstalk config
├── application.py           # Flask app entry point
├── setup.py                 # Package configuration
├── requirements.txt         # Dependencies
└── .github/workflows/       # CI/CD pipeline
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- pip

### Installation

```bash
# Clone the repository
git clone https://github.com/jayant1554/Insurance_premium_pred.git
cd Insurance_premium_pred

# Install dependencies
pip install -r requirements.txt

# Run the application
python application.py
```

App will be running at `http://localhost:5000`

---

## 🤖 Model Details

- **Algorithm:** Regression (with GridSearchCV + RandomizedSearchCV tuning)
- **Accuracy:** 88%+
- **Key techniques:** Outlier handling, feature encoding, cross-validation, hyperparameter tuning
- **Pipeline:** Modular, production-ready code with separate training and prediction pipelines

---

## 📈 Results

| Metric | Value |
|---|---|
| Model Accuracy | 88%+ |
| Deployment | AWS Elastic Beanstalk |
| Response Time | Real-time |

---

## 👤 Author

**Jayant Bisht**
- 📧 jk913600@gmail.com
- 🔗 [LinkedIn](https://linkedin.com/in/jayant-bisht)
- 🐙 [GitHub](https://github.com/jayant1554)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
