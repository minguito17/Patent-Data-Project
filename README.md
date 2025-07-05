
# Patent Data Case Classification and Litigation Duration

## Description / Overview

**EnterpriseIntel** helps law firms and corporate legal teams:  

- Predict case resolution timelines  
- Analyze key relationships between patents, entities, and legal outcomes  
- Optimize resource allocation  
- Enhance litigation strategy  
- Identify emerging IP trends  

Using AWS SageMaker and a fine-tuned BERT model, the project extracts insights to assist law firms, corporations, and courts in decision-making.

## Business Challenge

The U.S. legal system lacks transparency in early-stage litigation analysis. Companies struggle to understand case complexity, legal risk, and estimated durations early in the process. This often leads to inefficient resource allocation, poor strategy, and missed opportunities.

**EnterpriseIntel** addresses this by:  
- Classifying case complexity (Low, Medium, High)  
- Predicting litigation duration  
- Resolving legal entities with advanced NLP  

## Table of Contents

- [Installation](#installation)  
- [Usage](#usage)  
- [Features](#features)  
- [Contributing](#contributing)  
- [License](#license)  
- [Authors / Credits](#authors--credits)  
- [Contact Information](#contact-information)  
- [References / Acknowledgments](#references--acknowledgments)  

## Installation

1. Clone this repository:  
   ```
   git clone <YOUR_REPO_URL>
   cd <YOUR_REPO_DIRECTORY>
   ```

2. Install Python packages:  
   ```
   pip install pandas numpy scikit-learn seaborn matplotlib torch transformers sagemaker imbalanced-learn
   ```

3. Make sure your AWS SageMaker environment is set up properly.

## Usage

- Ingest and process Kaggle patent litigation data (20,000+ records).  
- Run notebooks or scripts to:  
  - Clean and transform the dataset  
  - Engineer features (standardize causes, encode entities)  
  - Fine-tune BERT for entity resolution and classification tasks  
  - Train and evaluate models on AWS SageMaker

## Features

- Fusion model combining BERT embeddings with tabular metadata  
- Case complexity classification (Low, Medium, High)  
- Patent trends and time-to-resolution insights  
- EDA with bar charts for patent statuses, court districts, entity types, causes of action  
- SMOTE balancing for class imbalance  
- Metrics: Accuracy, Precision, Recall, F1 Score, Confusion Matrix

## Contributing

Pull requests are welcome. Please open an issue first to discuss proposed changes.

## License

This project is for academic research and demonstration only.

## Authors / Credits

- Marinela Inguito  
- Sophia Jensen  
- Maria Mora Mora

## Contact Information

For questions, contact the project team through your university or course platform.

## References / Acknowledgments

- Public Kaggle Patent Litigation Dataset  
- Fregly, C., & Barth, A. (2021). *Data Science on AWS*. O'Reilly Media.  
- Fregly, C., Barth, A., & Eigenbrode, S. (2023). *Generative AI on AWS*. O'Reilly Media.  
- Layer-Aware Embedding Fusion for LLMs in Text Classification: [arXiv](https://arxiv.org/html/2504.05764v1#abstract)
