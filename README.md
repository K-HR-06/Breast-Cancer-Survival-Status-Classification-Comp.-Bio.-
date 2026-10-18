# Breast Cancer Survival Status Classification

A Computational Biology group project that compares machine learning models for classifying breast cancer patients' survival status using demographic and clinical data.

The project covers data exploration, statistical testing, feature encoding, and model evaluation.

## Dataset

`Breast_Cancer.csv` contains **4,024 patient records** and **16 columns**.

The target variable, `Status`, contains:

- **3,408 Alive**
- **616 Dead**

Predictors include age, cancer stage, tumor size, hormone receptor status, lymph node measurements, and survival months.

The report identifies the dataset as the SEER-based Breast Cancer dataset shared on Kaggle by Reihaneh Namdari.

## Methods

- Explore data using histograms, box plots, scatter plots, and a correlation heatmap.
- Examine associations with survival status using chi-square tests and Welch's t-tests.
- Apply one-hot encoding and ordinal encoding.
- Split the data into **70% training and 30% testing**.
- Use SMOTE during model development to address class imbalance.
- Tune models using randomized search and grid search.
- Evaluate accuracy, precision, recall, F1-score, confusion matrices, and ROC curves.

## Models and Recorded Results

The notebook records the following results for the tuned models:

| Model | Accuracy | Weighted F1-score |
| --- | --- | --- |
| Logistic Regression | 90.73% | 0.9008 |
| Decision Tree | 84.11% | 0.8470 |
| Random Forest | 91.72% | 0.9111 |
| Gaussian Naive Bayes | 80.30% | 0.8221 |
| AdaBoost | 87.50% | 0.8800 |

Random Forest achieved the highest recorded accuracy and weighted F1-score. These results are taken from saved notebook outputs and have not been independently reproduced.

## Tools

Python, pandas, NumPy, Matplotlib, seaborn, SciPy, scikit-learn, imbalanced-learn, and SHAP.

## Project Files

| File | Description |
| --- | --- |
| `Computation_Biology(Progress).ipynb` | Data exploration, preprocessing, model training, and evaluation |
| `Breast_Cancer.csv` | Dataset used in the analysis |

## How to Run

Open the notebook in Jupyter Notebook or Google Colab, install the required libraries, and place `Breast_Cancer.csv` in the working directory.

Run the notebook cells in order to perform the analysis and train the models.

## Notes

- `Survival Months` is included as a predictor, so the results describe classification using recorded follow-up information rather than prediction solely from information available at diagnosis.
- The final Random Forest and tuned Logistic Regression models are refitted on the original training data after tuning with SMOTE.
- The final SHAP force-plot cell contains a saved error and requires adjustment.

## Authors

**Computer Science and Statistics — BINUS University**

- Ann Abigail Halim
- Hazel Zaki Adityo
- Joycelin
- Marcell Prasetyo
