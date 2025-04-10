# Breast-Cancer-Diagnosis-using-Custom-Decision-Tree-Classifier

This repository presents a custom implementation of a Decision Tree classifier to predict tumor malignancy using the Breast Cancer Wisconsin (Diagnostic) dataset. The model is built from the ground up without relying on libraries such as scikit-learn. It includes detailed implementations of decision tree construction, pruning, parameter tuning, and performance evaluation.

## Repository Contents

### `p1.ipynb` – Decision Tree on Normalized Data  
Implements the foundational version of the Decision Tree algorithm:
- Uses `wdbc_train_normalized.csv` and `wdbc_dev_normalized.csv`.
- Supports both entropy and Gini index as splitting criteria.
- Visualizes the decision tree using `graphviz`.
- Evaluates performance using standard classification metrics.

### `p2.ipynb` – Enhanced Tree with Pruning and Tuning  
Expands the model in `p1.ipynb` with:
- Object-oriented `Node` and `DTree` classes.
- Chi-square based pruning for tree simplification.
- Hyperparameter tuning over tree depth and splitting modes.
- Improved modularity and flexibility in experimentation.

### `p3.ipynb` – Baseline on Unnormalized Data  
Provides a baseline comparison by training the decision tree on:
- `wdbc_train.csv` and `wdbc_dev.csv`.
- Identical algorithmic structure as `p1.ipynb`.
- Helps demonstrate the effect of normalization on model accuracy and stability.

## Dataset

The notebooks use the **Breast Cancer Wisconsin (Diagnostic)** dataset, which contains 30 numerical features extracted from digitized images of fine needle aspirates (FNA) of breast masses. The classification target is:
- `M` (Malignant), encoded as `1`
- `B` (Benign), encoded as `0`

Ensure the following CSV files are available in the working directory:
- `wdbc_train.csv`
- `wdbc_dev.csv`
- `wdbc_train_normalized.csv`
- `wdbc_dev_normalized.csv`

## Dependencies

The following Python packages are required:

```bash
pip install pandas numpy matplotlib graphviz scipy
```

Additionally, make sure `graphviz` is installed on your system:
- On Ubuntu/Debian: `sudo apt install graphviz`
- On macOS: `brew install graphviz`
- Or download from [graphviz.org](https://graphviz.org/download/)

## Features

- Custom-built Decision Tree with support for entropy and Gini index
- Chi-square pruning for overfitting control
- Manual hyperparameter tuning
- Tree visualization using Graphviz
- Evaluation metrics computed from scratch:
  - Accuracy
  - Sensitivity (Recall)
  - Specificity
  - Precision
  - F1 Score
  - False Positive Rate
  - False Negative Rate
  - Negative Predictive Value (NPV)

## Getting Started

To run the notebooks:

1. Clone this repository.
2. Place the required CSV datasets in the same directory.
3. Launch Jupyter Notebook or JupyterLab.
4. Open and execute the notebooks step-by-step.

## License

This project is intended for academic and educational use. Attribution is appreciated.
