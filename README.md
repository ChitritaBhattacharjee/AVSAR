# 🎓 AVSAR ML: Student Dropout & Academic Success Predictor

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-orange.svg)
![Status](https://img.shields.io/badge/Status-Active%20Deployment-brightgreen.svg)

An end-to-end Machine Learning pipeline and interactive web application designed to predict whether an undergraduate student is at risk of dropping out, remaining enrolled, or graduating successfully. By analyzing demographic data, socio-economic factors, and academic performance, this tool provides actionable, real-time predictive insights.

---

## 📊 Dataset Attribution

The predictive models trained in this repository utilize data sourced from the UCI Machine Learning Repository. 

**Full Citation:**
> Realinho, V., Vieira Martins, M., Machado, J., & Baptista, L. (2021). *Predict Students' Dropout and Academic Success* [Dataset]. UCI Machine Learning Repository. [https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)

---

## 🧠 Project Architecture & Key Features

* **Interactive Web Interface**: A user-friendly front-end allowing users to input student criteria and receive instant risk assessments.
* **Automated Feature Engineering**: Serialized preprocessing pipelines that handle raw categorical encoding and numeric scaling automatically.
* **Integrated Event Monitoring**: Custom system alert triggers that log inference anomalies and system events in real-time.

---

## 🗂️ Repository Structure

The project directory contains the following modular components:

### **Application & Automation Scripts**
* **`app.py`**: The primary web application script serving the interactive interface and executing live model inference.
* **`train.py`**: The automated pipeline script used to ingest data, train the predictive models, and export serialized assets.
* **`alerts.py`**: The event-monitoring module responsible for evaluating system thresholds and triggering notifications.
* **`alerts.log`**: The output background log file tracking runtime events and alert histories.

### **Serialized Machine Learning Assets**
* **`model.pkl`**: The fully trained primary predictive estimator.
* **`model_type.pkl`**: Configuration metadata tracking the algorithm architecture.
* **`features.pkl`**: The extracted structural mapping of required input variables.
* **`scaler.pkl`**: The serialized feature scaler ensuring standardized numerical inputs.
* **`label_encoder.pkl`**: The categorical encoder translating string classes into model-readable formats.

### **Datasets**
* **`data.csv`**: The foundational dataset utilized for exploratory data analysis and model training.
* **`demo_data_for_app.csv`**: A lightweight sample dataset provided to quickly test and verify the live web application.

---

## 🚀 Quick Start & Installation

### **1. Clone the Repository**
```bash
git clone [https://github.com/your-username/AVSAR_ML.git](https://github.com/your-username/AVSAR_ML.git)
cd AVSAR_ML
