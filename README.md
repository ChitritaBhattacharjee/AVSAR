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


````
### **2. Create a Virtual Environment (Recommended)**
It is best practice to run the project inside an isolated virtual environment to avoid dependency conflicts:
```bash
python -m venv venv

# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

```

### **3. Install Dependencies**

Install the necessary Python packages required for data processing, machine learning, and the web interface:

*(Note: You can install the standard core libraries directly: `pip install scikit-learn pandas numpy` along with your specific web framework like `flask` or `streamlit`.)*

### **4. Run the Application**

Launch the local predictive server by executing the primary application script:

```bash
python app.py

```

Open your web browser and navigate to the local URL displayed in your terminal (typically `http://localhost:5000` or `http://localhost:8501`) to access the interactive dashboard.

---

## 🛠️ Usage Guide

1. **Input Parameters:** Enter the student's demographic details, socio-economic factors, and current academic metrics into the front-end interface.
2. **Generate Prediction:** Submit the form to pass the data through the pre-trained `model.pkl` pipeline (which automatically applies the required `scaler.pkl` and `label_encoder.pkl` transformations).
3. **Monitor Alerts:** View the instant risk assessment on screen. Any real-time system anomalies or specific threshold triggers will be automatically recorded in `alerts.log`.

---

## 🛡️ License & Acknowledgments

This project is developed for educational and academic research purposes. The predictive models rely on data publicly hosted by the **UCI Machine Learning Repository**. Please refer to the dataset attribution link above for specific data usage terms, licensing policies, and proper author citations.

