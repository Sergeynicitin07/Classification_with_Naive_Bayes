# Breast Cancer Diagnosis Model

The **Breast Cancer Diagnosis Model** repository contains a project that builds and evaluates a predictive model for diagnosing breast cancer. This project utilizes the **Gaussian Naive Bayes (GNB)** classifier to distinguish between benign (non-cancerous) and malignant (cancerous) tumors based on medical data.

---

## Problem Statement

In medical diagnostics, it is critical to accurately classify tumors to ensure patients receive appropriate care. While traditional diagnostic methods exist, leveraging machine learning can provide an additional, data-driven tool to assist medical professionals.  
A key challenge is to build a model that is not only accurate but also reliable, especially in avoiding **false negative predictions**, where a malignant tumor is incorrectly classified as benign.

---

## Solution Overview

This project provides a solution by using the **Gaussian Naive Bayes classifier** on the well-known **Breast Cancer Wisconsin (Diagnostic)** dataset.  
The project performs a detailed analysis of the data, evaluates the model's performance under different conditions, and highlights the importance of proper methodology.  

A central focus of this project is to investigate the classifier's **assumption about feature distribution** and its practical impact on model performance.

---

## Key Features

- **Gaussian Naive Bayes Classifier**  
  Utilizes a probabilistic model that assumes features follow a normal distribution, making it computationally efficient for this task.

- **Exploratory Data Analysis (EDA)**  
  Includes comprehensive visualizations (histograms) to analyze the distribution of all 30 features.

- **Correct Methodology**  
  Demonstrates the correct approach to model evaluation by splitting the data into separate training and testing sets, avoiding the pitfalls of overfitting.

- **Performance Analysis**  
  Compares the model's performance on a full feature set versus a reduced one, showing how feature selection impacts key metrics like **Accuracy, F1-Score**, and, most importantly, **Recall**.

---

## Methodology and Findings

This project's core is a structured experiment that tested a key hypothesis about the Gaussian Naive Bayes classifier.

### 1. Baseline Overfitting Test
- Initially, a quick test was performed by training and evaluating the model on the entire dataset **without a train-test split**.  
- This served as a baseline check for overfitting, showing misleadingly high accuracy results that are not representative of real-world performance.  
- This step confirmed the necessity of a proper evaluation methodology.

### 2. Initial Hypothesis
- Based on the theoretical assumption of the GNB classifier, we hypothesized that **removing features that did not have a normal distribution would improve performance**.  
- The exploratory data analysis (EDA) had already identified several highly skewed features that seemed like good candidates for removal.

### 3. Experiment
- **Model 1 (Full Feature Set):** Trained and evaluated on a properly split dataset using all 30 features.  
- **Model 2 (Reduced Feature Set):** Trained and evaluated on a dataset with the non-normally distributed features removed.

### 4. Unexpected Findings
- **Model 1 (all features):** Achieved a perfect **Recall of 1.0**, meaning it correctly identified every malignant tumor in the test set.  
- **Model 2 (reduced features):** Performed worse, making **two critical false negative errors**.

### 5. Conclusion
- This finding directly **challenges the initial hypothesis**.  
- Even if features don’t perfectly adhere to the model’s assumptions, they may still contain **critical information** essential for accurate and safe predictions.  
- In high-stakes domains like medical diagnosis, **using the full feature set is the better and safer approach**.

---

## Author

**Sergey Nikitin**
