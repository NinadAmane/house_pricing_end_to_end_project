# house_pricing_end_to_end_project

# 📊 Boston House Price Prediction — End-to-End ML Deployment

> A full-stack Machine Learning project that predicts house prices using regression, served via a Flask web app, containerized with Docker, and deployed publicly on Render.

🔗 **Live Demo:**  
https://house-pricing-prediction-end2end.onrender.com/

---

## 🚀 Project Overview

This project demonstrates an **end-to-end Machine Learning workflow**, starting from model training to real-world deployment.

### Key Highlights

- Trained a regression model on the **Boston Housing Dataset**
- Built a **Flask web application** for predictions
- Designed a **modern, dark-themed UI**
- Containerized the app using **Docker**
- Deployed the app **without Heroku or credit card** using **Render**

---

## 🧠 Dataset Information

- **Dataset:** Boston Housing Dataset
- **Target Variable:** `MEDV`
- **Unit of Price:**  
  👉 **Thousands of US Dollars ($1000s)**

### Example:

| Model Output | Meaning   |
| ------------ | --------- |
| `11.99`      | ≈ $11,990 |
| `25.0`       | ≈ $25,000 |

> ⚠️ Note: The dataset is from the 1970s, so prices are historically low.

---

## 🏗️ Tech Stack

- **Language:** Python
- **ML:** Scikit-Learn
- **Backend:** Flask
- **Frontend:** HTML + CSS (Glassmorphism Dark UI)
- **Containerization:** Docker
- **Server:** Gunicorn
- **Deployment:** Render (Free Tier)

---

## 🧪 Model Training (Summary)

- Features were standardized using **StandardScaler**
- Model trained using **Linear Regression**
- Model and scaler saved using `pickle`
- Predictions are made after scaling inputs using the **same scaler**

---

## 🌐 Flask Application

### Routes

- `/` → Home page (UI form)
- `/predict` → Handles form input and displays prediction
- `/predict_api` → JSON-based API endpoint

---

## 🎨 User Interface

- High-end **dark theme**
- Glassmorphism input fields
- Neon orange CTA
- Bento-grid layout (minimal scrolling)
- Fully responsive (desktop + mobile)

No JavaScript frameworks used — clean, fast, and stable.

---

## 🐳 Dockerization

Docker packages the **entire environment** (Python + dependencies + app) so it runs the same everywhere.

### 📄 Dockerfile

Build the Docker image:

```bash
docker build -t boston-house-price .
```

Run the Docker container:

```bash
docker run -p 5000:5000 boston-house-price
```
