# 🧠 Machine Learning Experiments with MLflow

This repository contains hands-on projects demonstrating how to use **MLflow** for experiment tracking, model management, and model deployment across different machine learning workflows.
Each project highlights how MLflow can be integrated into real-world ML pipelines — from training and evaluation to tracking, registration, and inference.

---

## 🚀 Getting Started

### 1. Install Dependencies

Before running any project, make sure you have the required Python packages installed:

```bash
pip install mlflow scikit-learn pandas
```

### 2. Start the MLflow Tracking Server

Launch the MLflow UI locally to visualize experiments, runs, and models:

```bash
mlflow ui
```

By default, the MLflow UI will be available at:
👉 **[http://127.0.0.1:5000](http://127.0.0.1:5000)**

---

## 📂 Projects Overview

### 🌸 **1. Iris Classification (Logistic Regression)**

**Goal:** Train and track a Logistic Regression model to classify iris flowers based on sepal and petal dimensions.

**Highlights:**

* Uses the classic **Iris dataset** from scikit-learn.
* Logs parameters, metrics, and model artifacts to MLflow.
* Demonstrates model registration and versioning using **MLflow Model Registry**.
* Shows how to load and serve models using `mlflow.pyfunc`.

**Key Concepts Covered:**

* Experiment tracking (`mlflow.start_run`, `mlflow.log_param`, `mlflow.log_metric`)
* Model logging and registration (`mlflow.sklearn.log_model`)
* Serving validation and inference from registered models

**Experiment Name:** `Iris-Classification`
**Registered Model Name:** `tracking-quickstart`

---

## 🧭 MLflow Components in Use

* **Tracking Server:** Logs metrics, parameters, and artifacts.
* **Model Registry:** Manages model versions, stages (e.g., Staging/Production), and metadata.
* **MLflow UI:** Provides visual tracking and comparison of runs.
* **MLflow PyFunc Interface:** Loads models for batch or real-time inference.

---

## 📊 Viewing Your Runs

Once the MLflow UI is running:

1. Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.
2. Navigate to the **“Experiments”** section to view:

   * Model parameters and metrics
   * Training runs and comparisons
   * Logged models and artifacts
3. Use the **“Models”** tab to explore registered models, versions, and deployment stages.


---

## 🧾 References

* [MLflow Documentation](https://mlflow.org/docs/latest/index.html)
* [Scikit-learn Documentation](https://scikit-learn.org/stable/)
* [MLflow Model Registry Guide](https://mlflow.org/docs/latest/model-registry.html)

---



