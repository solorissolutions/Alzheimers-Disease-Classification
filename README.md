# Alzheimer's Disease Classification Prototype

**Binary Classification of Alzheimer's Disease Status (Demented vs. Non-Demented)**  
*Intelligent Prototype Development – CET2001 Artificial Intelligence Module*

![Python](https://img.shields.io/badge/Python-3.9%2B-blue) 
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.5-orange) 
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-green) 
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## Project Overview

This repository contains a fully reproducible machine learning prototype for **binary classification of Alzheimer's disease** using demographic, clinical, and MRI-derived features from a structured healthcare dataset (2461 samples, ~1150 unique subjects with longitudinal visits).

The goal is to demonstrate best practices in healthcare ML:
- Exploratory Data Analysis (EDA)
- Missing data handling and preprocessing
- **Group-aware train/test splitting** to prevent data leakage from repeated subject scans
- Comparison of classical classifiers
- Comprehensive evaluation with multiple metrics and visualizations

**Key Results** (on held-out test set):
- **Best Models**: Logistic Regression & SVM (RBF)
  - Accuracy: **91.9%**
  - Precision: **98.3%**
  - Recall: **86.4%**
  - F1-Score: **91.9%**
  - ROC-AUC: **0.932** (LR) / **0.924** (SVM)
- Random Forest: Close second (AUC 0.929)
- KNN: Weakest (AUC 0.918, lower recall)

## Dataset

- `dataset.csv`: Custom structured dataset (synthetic-like, based on OASIS-style longitudinal MRI data)
- Features: Age, Sex (M/F), Education (EDUC), Socioeconomic (NIS), MMSE, CDR, eTIV, nWBV, ASF, Visit, MR Delay
- Target: `Group` → Binary (Demented = 1, Non-demented = 0)
- Class distribution: Mild imbalance (56% Demented, 44% Non-demented)
- 
## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/solorissolutions/Alzheimers-Disease-Classification.git
   cd Alzheimers-Disease-Classification
   Install dependencies (recommended: use Anaconda/Miniconda):Bashconda create -n alzheimers python=3.9
conda activate alzheimers
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
Launch Jupyter Notebook:
Bash - 
jupyter notebookOpen Alzheimers_Disease_Classification_ScikitLearn.ipynb and run all cells.

## Repository Structure
