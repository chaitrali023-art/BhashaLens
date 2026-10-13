# BhashaLens
Indian Language Identification using Character-Level NLP | NLP CA3 Project
BhashaLens

Indian Language Identification Using Character-Level NLP | NLP CA3 Project

Overview

BhashaLens is a Natural Language Processing project that identifies the language of a text headline using character-level TF-IDF features and Logistic Regression.

Objectives

- Build a complete NLP text-classification pipeline.
- Clean and preprocess labelled text data.
- Train a character-level language classifier.
- Evaluate model performance using accuracy and macro F1-score.
- Audit performance across short and long headlines.
- Investigate influential character n-grams for explainability.

Dataset

Source: "Indian Language Identification Dataset — Kaggle" (https://www.kaggle.com/datasets/processvenue/indian-language-identification)

Split| Records after cleaning
Training| 95,045
Validation| 20,368
Testing| 20,368
Language classes| 18

The dataset contains headline text and language labels. Missing or blank text and label rows were removed. The dataset is not included in this repository; obtain it from the original source and follow its licence terms.

Methodology

1. Load and clean the dataset.
2. Extract character-level TF-IDF features using character n-grams of lengths 2–5.
3. Train a Logistic Regression classifier.
4. Evaluate performance on the held-out test set.
5. Analyse the confusion matrix and class-wise performance.
6. Compare short-text and long-text performance.
7. Inspect influential character n-grams.

Reported Results

Metric| Result
Test accuracy| 99.73%
Test macro F1-score| 99.68%
Short-vs-long accuracy gap| Approximately 0.114 percentage points

These results are from the current notebook run. Refer to the notebook for detailed metrics and audit results.

Bias Audit and Explainability

The project compares performance across short and long headlines and examines class-wise performance. Influential character n-grams are inspected to help understand model predictions.

A small performance gap does not establish fairness across all languages or real-world text conditions.

Technology Stack

- Python
- Google Colab
- pandas and NumPy
- scikit-learn
- Matplotlib
- TF-IDF character n-grams
- Logistic Regression

Limitations

- The model predicts only among its 18 known language classes.
- It does not currently provide an unknown-language rejection option.
- Noisy, transliterated, and code-mixed text may be challenging.
- Test performance may not generalise to new datasets.

Repository Contents

- "BhashaLens_CA3.ipynb" — NLP pipeline and evaluation notebook.
- "README.md" — Project documentation.

Additional evaluation results, the model card, report, and presentation will be added as they are finalised.

Reproducibility

Open the notebook in Google Colab, obtain the dataset from the original source, upload the required CSV files when prompted, and run the notebook cells in order.

Academic Context

Subject: Natural Language Processing — CA3 Build, Audit, and Pitch
Student: chaitrali Chaskar, Aditya pune 

Institution: Symbiosis Artificial Intelligence Institute (SAII), Lavale, Pune
Academic year: 2026–27

Acknowledgements

The dataset is credited to its original Kaggle publisher. Consult the dataset page for attribution and licensing requirements.
