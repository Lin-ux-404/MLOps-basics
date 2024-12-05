# Deploying a Training Pipeline and Batch Endpoint in Azure Machine Learning Studio

This repository demonstrates how to deploy a training pipeline in Azure Machine Learning Studio and create a batch endpoint for performing batch scoring tasks.

---

## **Scenario**

We train a machine learning model to determine whether a patient has diabetes. The workflow involves:

1. Uploading a CSV file with patient data to an Azure Storage Account.
2. Training two machine learning models:
   - A Decision Tree Classifier
   - A Logistic Regression Model
3. Comparing the models to determine which is better suited for the task.
4. Deploying the chosen model to a batch endpoint for batch scoring.

---

## **Contents**

### **1. Components**
The repository contains four YAML components for building the training pipeline:

- **`fixing-missing-data.yml`**: Handles missing data in the dataset.
- **`normalize-data.yml`**: Normalizes the data to improve model performance.
- **`train-decision-tree.yml`**: Trains a Decision Tree model on the dataset.
- **`train-logistic-regression.yml`**: Trains a Logistic Regression model on the dataset.

### **2. Data**
- **`diabetes.csv`**: Training dataset containing labeled patient data.
- Four unlabeled datasets for testing batch scoring.

### **3. Notebooks**
- **`training_pipeline_deployment.ipynb`**: Deploys the training pipeline.
- **`deploy_to_batch_endpoint.ipynb`**: Deploys the chosen model to a batch endpoint for scoring.

---

## **Setup**

### **Step 1: Configure Environment**
1. Create a `.env` file at the root of the directory.
2. Use the provided `.env.sample` file as a reference to fill in your environment variables.

### **Step 2: Set Up Azure ML Workspace**
- If you do not have a Machine Learning Workspace set up, run the `setup.ps1` script to automate the process.

### **Step 3: Run Training Pipeline**
- Use the `training_pipeline_deployment.ipynb` notebook to deploy a training pipeline in Azure Machine Learning Studio.

### **Step 4: Deploy Batch Endpoint**
- Use the `deploy_to_batch_endpoint.ipynb` notebook to deploy a batch endpoint for batch scoring.

---

## **Authors**
[Shenglin Xu](shenglinxu@microsodt.com)