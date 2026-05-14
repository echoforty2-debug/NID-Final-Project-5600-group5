# Notebook Outputs

This folder contains figures and CSV summary files produced from the final executed notebook.

## Figures

- `eda_class_distribution.png` — final CSE-CIC-IDS2018 benign vs. attack class split
- `eda_feature_distributions.png` — selected feature distributions by class
- `eda_correlation_heatmap.png` — selected numeric feature correlations
- `eval_roc_pr_curves.png` — ROC and precision-recall curves
- `eval_confusion_matrices.png` — confusion matrices at threshold 0.5
- `calibration_curves.png` — reliability diagrams and Brier score comparison
- `threshold_optimization.png` — threshold sweep for LightGBM + Platt calibration
- `drift_analysis.png` — KS feature drift analysis between CSE-CIC-IDS2018 and CIC-IDS2017
- `drift_performance_drop.png` — PR-AUC degradation under drift
- `results_heatmap.png` — final model performance heatmap
- `feature_importance.png` — top LightGBM feature importances

## CSV Files

- `ids_results_summary.csv` — final model metric summary
- `ids_drift_analysis.csv` — cross-year drift robustness summary
