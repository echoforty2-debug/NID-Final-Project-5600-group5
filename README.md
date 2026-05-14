# Comparative Analysis of Modern Tabular ML for Network Intrusion Detection

## Project Information

**Course:** CPRE/COM S 5600  
**Project:** Final Project  
**Team:** Group 5  
**Team Members:** Farman H. Sayem, Jace C. Rea, Kunle S. Oguntoye  

## Project Overview

This repository contains the final project materials for **Comparative Analysis of Modern Tabular ML for Network Intrusion Detection**. The project evaluates modern tabular machine learning models for binary network intrusion detection using a reproducible Google Colab workflow.

The project compares **LightGBM**, **XGBoost**, **CatBoost**, and a **LightGBM + SMOTE** variant on CSE-CIC-IDS2018, then evaluates cross-year robustness using CIC-IDS2017 as a drift dataset. The final evaluation focuses on model performance, class imbalance, calibration, threshold selection, and drift robustness rather than accuracy alone.

## Repository Structure

```text
network-intrusion-detection-5600/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── network_intrusion_detection_rea_Results.ipynb
│   └── network_intrusion_detection_rea_Results_colab_print.pdf
├── reports/
│   ├── 5600_Final_Project_Report_Group5.pdf
│   ├── 5600_Final_Project_Report_Group5.docx
│   ├── Project_Midterm_Submission.pdf
│   └── Project_Proposal_Sayem_Rea_Oguntoye.pdf
├── presentations/
│   ├── 5600_Final_Presentation_Group5.pdf
│   └── 5600_Final_Presentation_Group5.pptx
├── outputs/
│   ├── eda_class_distribution.png
│   ├── eda_feature_distributions.png
│   ├── eda_correlation_heatmap.png
│   ├── eval_roc_pr_curves.png
│   ├── eval_confusion_matrices.png
│   ├── calibration_curves.png
│   ├── threshold_optimization.png
│   ├── drift_analysis.png
│   ├── drift_performance_drop.png
│   ├── results_heatmap.png
│   ├── feature_importance.png
│   ├── ids_results_summary.csv
│   └── ids_drift_analysis.csv
└── data/
    └── README.md
```

## Main Files

- `notebooks/network_intrusion_detection_rea_Results.ipynb`  
  Main Google Colab notebook used for data loading, cleaning, feature alignment, model training, evaluation, calibration, threshold analysis, and drift testing.

- `notebooks/network_intrusion_detection_rea_Results_colab_print.pdf`  
  PDF export of the executed Colab notebook.

- `reports/5600_Final_Project_Report_Group5.pdf`  
  Final written report.

- `reports/5600_Final_Project_Report_Group5.docx`  
  Editable Word version of the final report.

- `presentations/5600_Final_Presentation_Group5.pdf`  
  Final presentation PDF.

- `outputs/`  
  Exported figures and CSV result summaries produced from the notebook.

- `data/README.md`  
  Instructions for accessing and organizing the external CIC-IDS datasets.

## Dataset Access

The raw datasets are **not included** in this repository because they are large external datasets. The notebook expects the datasets to be downloaded separately and placed in Google Drive.

Dataset instructions are provided in:

```text
data/README.md
```

Datasets used:

- CSE-CIC-IDS2018
- CIC-IDS2017

Both datasets are provided by the Canadian Institute for Cybersecurity.

## How to Run the Notebook

1. Download the required datasets using the instructions in `data/README.md`.
2. Place the CSV files in Google Drive using the expected folder structure.
3. Open `notebooks/network_intrusion_detection_rea_Results.ipynb` in Google Colab.
4. Mount Google Drive when prompted.
5. Install required packages if needed:

```python
!pip install lightgbm xgboost catboost imbalanced-learn
```

6. Run the notebook cells in order.

## Python Libraries Used

- pandas
- NumPy
- SciPy
- scikit-learn
- imbalanced-learn
- LightGBM
- XGBoost
- CatBoost
- matplotlib
- seaborn

## Summary of Final Results

The final same-year 2018 test results showed that LightGBM had the strongest overall same-year speed/performance tradeoff, with the best base PR-AUC and recall. XGBoost performed very similarly on the 2018 test data and was the most robust model under the cross-dataset drift test.

Calibration improved probability reliability, especially for LightGBM with isotonic calibration. Threshold tuning showed that increasing recall requires accepting a much higher false-positive rate. The drift analysis showed that all models experienced major performance degradation when evaluated on CIC-IDS2017, suggesting that model monitoring, recalibration, and retraining would be necessary before operational use.

## Notes on AI Assistance

An AI assistant, such as ChatGPT, was used to support the writing and revision process for grammar, clarity, organization, and sentence flow. The underlying project ideas, methodology, implementation decisions, debugging, testing, results interpretation, and analysis were completed by the team based on our own understanding of the project and course material.

AI support was used as a writing aid, not as a replacement for the project work, technical reasoning, or analysis presented in this project.

## Reproducibility Notes

The notebook uses a fixed random seed of `42` where applicable. The workflow includes data loading, cleaning, feature alignment, train/validation/test splitting, model training, probability calibration, threshold analysis, and drift testing.
