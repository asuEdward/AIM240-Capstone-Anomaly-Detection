# AIM240-Capstone-Anomaly-Detection
My AIM240 Capstone: Unsupervised credit card fraud detection using Isolation Forest with GitHub-Colab deployment workflow.
# AIM240 Capstone Project — Anomaly Detection in Credit Card Fraud

## Project Overview
AIM240 Capstone Project — Anomaly Detection in Credit Card Fraud
This project continues the anomaly detection theme developed during AIM230. It applies unsupervised machine learning to detect fraudulent transactions in a credit card dataset using Isolation Forest, with LightGBM used as a comparison benchmark. The goal is to build a lightweight, explainable, and deployable anomaly detection pipeline suitable for integration into edge environments or GitHub-hosted Colab workflows.

## Dataset 
- Source: Kaggle Credit Card Fraud Detection Dataset
- Link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
- The dataset contains 284,807 transactions, each with 30 anonymized features (V1 through V28), and two additional columns: Amount and Time.

## Setup Instructions (Windows Fresh Install)
1. Install Python (version 3.8 or higher recommended): https://www.python.org/downloads/

2. Clone this repository:
git clone https://github.com/YOUR_USERNAME/AIM240-Capstone-Anomaly-Detection.git
cd AIM240-Capstone-Anomaly-Detection

3. Create a virtual environment (optional but recommended):
python -m venv venv
venv\Scripts\activate

4. Install required Python libraries:
pip install -r requirements.txt

5. Launch the notebook:
jupyter notebook

Or open the notebook using Google Colab by uploading the .ipynb file located in the /notebooks folder.

## Project Structure
- /data — Contains the creditcard.csv dataset
- /notebooks — Jupyter or Colab notebooks with model pipeline code
- /models — Trained model files (if saved)
- /outputs — Evaluation results, graphs, and confusion matrices
- /diagrams — Pipeline diagrams or model visualizations
- /docs — Final PDF deliverables and proposal

## Requirements
- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- These libraries are listed in the requirements.txt file and can be installed in one step.

## Results Summary
This project successfully used Isolation Forest to detect fraudulent credit card transactions without relying on labeled data. Simulated profiling showed the model’s memory usage at ~253MB, with quantization reducing usage by 40% and improving inference latency by approximately 20%. Visualizations and confusion matrices confirmed the model’s ability to generalize well in low-resource environments. Results were shared using Google Colab and made reproducible through GitHub.

## Author
Edward Smith
AIM240 — Artificial Intelligence Capstone Project
Chandler-Gilbert Community College
Spring 2025
