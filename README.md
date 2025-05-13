# AIM240-Capstone-Anomaly-Detection
My AIM240 Capstone: Credit card fraud detection using Isolation Forest (unsupervised) and LightGBM (supervised benchmark), deployed via a GitHub–Colab workflow.
# AIM240 Capstone Project — Anomaly Detection in Credit Card Fraud

## Project Overview
AIM240 Capstone Project — Anomaly Detection in Credit Card Fraud
This project continues the anomaly detection theme developed during AIM230. It applies unsupervised machine learning to detect fraudulent transactions in a credit card dataset using Isolation Forest, with LightGBM used as a supervised comparison benchmark. The goal is to build a lightweight, explainable, and deployable anomaly detection pipeline suitable for integration into edge environments or GitHub-hosted Colab workflows.

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
- /notebooks — Jupyter or Colab notebooks with model pipeline code used for model training and evaluation
- /models — Trained model files (if saved)
- /outputs — Evaluation results, graphs, and confusion matrices
- /diagrams — Pipeline diagrams or model visualizations
- /docs — Final PDF deliverables and Capstone report

## Requirements
- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- These libraries are listed in the requirements.txt file and can be installed in one step.

## Results Summary
This project successfully used Isolation Forest to detect fraudulent credit card transactions without relying on labeled data. It also implemented LightGBM as a supervised benchmark to compare results.

Final metrics:
- Isolation Forest F1-score (fraud): 0.3365
- LightGBM F1-score (fraud): 0.8634
- Inference time (batch size 128): ~8ms
- Memory usage after cleanup: ~690.65 MB

Visualizations and confusion matrices confirmed each model’s performance. 

## Memory Profiling
Memory usage was measured using the `psutil` library to assess the resource footprint of the Isolation Forest model during execution.

Due to the nature of Jupyter/Colab environments, memory usage may incrementally increase with repeated cell executions. This is caused by retained object references and memory that is not automatically released between runs. To obtain a reproducible measurement, a fresh runtime was used before this profiling step.

The reported usage was approximately 690.65 MB of RAM, confirming suitability for deployment on modern laptops, edge devices, or lightweight cloud containers (i.e., systems with moderate memory constraints). The output below reflects the model’s memory usage immediately after reinitialization.

NOTE: Cleanup commands such as `gc.collect()`, `plt.close('all')`, and `del` statements can be used in development environments to manage memory manually and improve consistency between runs.

The full pipeline runs in Google Colab and is shared through GitHub.

## Author
Edward Smith
AIM240 — Artificial Intelligence Capstone Project
Chandler-Gilbert Community College
Spring 2025
