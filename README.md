# OKCupid - Predicting Drug Use with Machine Learning
This project analyzes OKCupid survey data to predict whether a user takes drugs or not based on other personal characteristics. By applying supervised learning techniques, the goal is to determine if it’s possible to predict drug use using users’ demographic and lifestyle attributes. In addition to the Jupyter Notebook, this repository contains a **PowerPoint presentation** that summarizes the key findings, models used, and results of the project. 

## Project Goals
1. Many users did not answer the "Do you take drugs?" question.
2. This project aims to predict drug use using other profile information.
3. It explores whether dating apps can infer missing data using machine learning.

## Dataset
- Source: Codecademy (profiles.csv). This project uses a dataset provided by Codecademy as part of their Data Science course.  
Due to size and licensing restrictions, the dataset (`profiles.csv`) is **not included** in this repository.
- Size: 59,946 rows and 31 features
- Preprocessing Steps:
  - Encoded categorical variables (LabelEncoder & One-Hot Encoding).
  - Merged response categories for drug use (never/did not answer = 0, sometimes/often = 1).
  - Addressed class imbalance using class weights in Logistic Regression.

## Machine Learning Models Used
- Logistic Regression (Baseline)
- Support Vector Machine (SVM) (Non-performant)

## Key Findings
1. Logistic Regression achieved 87% accuracy but struggled with minority class recall.
2. SVM performed poorly for drug use prediction due to class imbalance.
3. Tuning class weights (1:6 ratio) improved recall for drug users from 0.10 to 0.63.
4. Next Steps: Try Random Forest, KNN, and different resampling techniques to improve predictions.

## Technologies Used
- Python
- Jupyter Notebook
- scikit-learn
- pandas
- Matplotlib & Seaborn

## How to run this project
1. Clone this repository:
   git clone https://github.com/marrubios86/OKCupid-Date-A-Scientist/blob/main/date-a-scientist.ipynb
2. Install dependencies:
   pip install -r requirements.txt
3. Open Jupyter Notebook:
   jupyter notebook
4. Open date-a-scientist.ipynb in the Jupyter interface and run the cells.

## Future Work
- Test Random Forest and K-Nearest Neighbors models.
- Improve feature selection.
- Explore oversampling techniques like SMOTE.
- Evaluate model performance using AUC-ROC curves.
