# ADS508-Team4
ADS508-Team4 Final Project

## Overview

EnterpriseIntel enables law firms and corporate legal teams to:

- Predict case resolution timelines
- Analyze key relationships between patents, entities, and legal outcomes
- Optimize resource allocation
- Enhance litigation strategy
- Identify emerging IP trends

We leverage AWS SageMaker, a fine-tuned BERT model to extract insights that can assist law firms, corporations, and courts in decision making.

---

## Business Challenge

The U.S. legal system lacks transparency in early-stage litigation analysis. Companies often struggle to understand case complexity, legal risk, and estimated durations early in the process. This leads to inefficient resource allocation and poor decision-making.

![Patents Judges](https://github.com/mmoramora/ADS508-Team4/blob/main/image/concept-international-day-women-judges.jpg)

Picture Attribution: “Designed by Freepik” 

------------------------------------------

**EnterpriseIntel addresses this by:**
- Classifying case complexity (Low, Medium, High)
- Predicting litigation duration

## Project Goals

### 1. Data Ingestion & Processing
- Build a containerized pipeline to process .csv data from public kaggle patent data

### 2. Case Complexity Classification
- Implement a classification model to classify patent cases as low, medium, or high complexity based on resolution time predictions

### 3. Entity Resolution
- Apply BERT for advanced entity recognition to identify and standardize primary causes of action and key entities across patent documentation

### 4. Predictive Analytics
- Patent trends and time of case resolution
  
---

##  Data Sources

- **Patent Litigation Case Data (CSV)** – 20,000+ records from U.S. District Courts

The dataset is cleaned and stored in Amazon S3. 

---

## Exploratory Data Analysis (EDA)

EDA was conducted using Jupyter Notebook:

Bar charts were used to understand:
- Distribution of patent statuses
- Cases filed
- Distribution of court districs
- Distribution of entity types
- Frequent cause of actions
  
---

## Machine Learning 

We built a **fusion model** using:

1. **BERT Embeddings**: Fine-tuned on legal cause-of-action texts
2. **Tabular Features**: One-hot encoded & scaled features (e.g., court, entity type)
3. **Neural Network Classifier**: Trained on fused embeddings + tabular data using SageMaker (`ml.m5.xlarge`)

## Model Evaluation

- **Task **: Classify case complexity (`Low`, `Medium`, `High`)
- **Metrics**: Accuracy, Precision, Recall, F1 Score, Confusion Matrix
- **Class Imbalance**: Addressed using oversampling techniques and macro-averaged F1
