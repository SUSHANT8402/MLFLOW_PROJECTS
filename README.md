# 🧠 Machine Learning Experiments with MLflow

This repository showcases practical **end-to-end machine learning experiments** using **MLflow** for experiment tracking, model management, and deployment.
Each project demonstrates how MLflow integrates seamlessly into modern ML workflows — from model training and hyperparameter tuning to evaluation, registration, and inference.

---

## 🚀 Getting Started

### 1. Install Dependencies

Make sure you have Python and the required libraries installed before running any project.
Refer to each project folder for a list of dependencies or install common packages such as:

```bash
pip install -r requirements.txt
```

### 2. Launch the MLflow Tracking Server

Start the MLflow UI locally to monitor experiments and model versions.
By default, the UI runs at:

👉 **[http://127.0.0.1:5000](http://127.0.0.1:5000)**

---

## 🧩 Projects Overview

### **1. Iris Classification (Logistic Regression)**

**Objective:**
Classify iris flowers using sepal and petal dimensions through a Logistic Regression model.

**Key Highlights:**

* Uses the classic **Iris dataset** from scikit-learn.
* Tracks model parameters, metrics, and artifacts in MLflow.
* Demonstrates model versioning and lifecycle management using the **MLflow Model Registry**.
* Covers model loading and serving via the **PyFunc interface**.

**Concepts Demonstrated:**

* Experiment tracking (`mlflow.start_run`, logging metrics and parameters)
* Model registration and deployment
* Run comparison and artifact visualization

**Experiment Name:** `Iris-Classification`
**Registered Model:** `tracking-quickstart`

---

### 🏠 **2. House Price Prediction (Random Forest with Hyperparameter Tuning)**

**Objective:**
Predict house prices using the **California Housing dataset**, leveraging hyperparameter tuning and MLflow tracking.

**Key Highlights:**

* Implements **Random Forest Regressor** for price prediction.
* Performs **hyperparameter tuning** using `GridSearchCV`.
* Logs all hyperparameters, metrics, and model artifacts to **MLflow UI**.
* Enables **comparison across multiple runs** to identify the best model configuration.
* Registers the best-performing model in the **MLflow Model Registry** for version control and deployment.

**Concepts Demonstrated:**

* Hyperparameter tuning & experiment management
* Automated logging of best parameters and performance metrics
* Model registration and tracking for production readiness

**Experiment Name:** `House-Price-Prediction`
**Registered Model:** `Best-RandomForestRegressor-Model`

---

### 🍷 **3. Wine Quality Prediction (Keras ANN with Hyperopt Optimization)**

**Objective:**
Predict wine quality using a **Keras-based Artificial Neural Network (ANN)**, with automated hyperparameter optimization via **Hyperopt** and full MLflow experiment tracking.

**Key Highlights:**

* Utilizes the **Wine Quality (White)** dataset from the UCI Machine Learning Repository.
* Defines a neural network with input normalization, hidden dense layers, and ReLU activation.
* Performs **hyperparameter optimization** using `fmin()` from Hyperopt (parameters: learning rate & momentum).
* Logs all metrics (RMSE), hyperparameters, and model artifacts to MLflow automatically.
* Tracks multiple nested runs for each hyperparameter combination.
* Uses MLflow’s **model signature** to record input-output schema for reproducible inference.
* Demonstrates model validation and inference via MLflow’s **PyFunc interface**.

**Concepts Demonstrated:**

* Nested MLflow runs and parameter sweeps
* Automatic schema inference using `infer_signature()`
* Model comparison and best-run selection
* Model deployment and REST API validation
* Input validation with `validate_serving_input()` and `convert_input_example_to_serving_input()`

---

## ⚙️ MLflow Components in Use

* **Tracking Server:** Records parameters, metrics, and artifacts for every run.
* **Model Registry:** Organizes model versions, stages, and metadata.
* **MLflow UI:** Provides a visual dashboard for comparing experiments.
* **MLflow PyFunc Interface:** Enables loading models for inference in any environment.

---

## 📊 How to View Your Experiments

1. Run the MLflow UI and open **[http://127.0.0.1:5000](http://127.0.0.1:5000)**.
2. Navigate to the **Experiments** section to explore:

   * Run metrics (accuracy, RMSE, etc.)
   * Parameter comparisons across runs
   * Model artifacts and logs
3. Switch to the **Models** tab to inspect registered models, their versions, and lifecycle stages (e.g., *Staging* or *Production*).

---
