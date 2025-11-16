# A2_G4_Transaction_Fraud_Detection_System

#### A machine-learning–powered fraud detection system that predicts whether a transaction is **fraudulent or legitimate**.

The project includes data preprocessing, model training, evaluation, and an interactive Gradio web app where users can test transactions.

## 1. Objective
The goal of this project is to:
- Build a reliable machine learning system that can accurately classify fraudulent vs. legitimate Transaction transactions.
- Compare two major ML models
  - Logistic Regression
  - Random Forest Classifier
- Build an interactive fraud simulation app where the user enters an amount, and the system:
  - generates a realistic transaction pattern
  - predicts risk levels
  - provides a consensus output
- Understand how fraud detection works in real-life and how ML models learn subtle hidden patterns.


## 2. Dataset Details
This project uses the Credit Card Fraud Detection Dataset provided by the Machine Learning Group (MLG) at the Université Libre de Bruxelles (ULB).

It is one of the most widely used benchmark datasets for fraud detection research.


### Dataset Source
Kaggle: Credit Card Fraud Detection
Original research dataset collected by ULB (Machine Learning Group)

- Total Transactions - 568630
- Legitimate Transactions - 284315
- Fraudulent Transactions - 284315
- Fraud percentage - 50%
- File Format - .csv
- No of features - 30(Including target)


Feature Description
The dataset contains 30 columns, divided as follows:

1. Time
- Represents the number of seconds elapsed since the first transaction.
- Helps capture temporal patterns.
2. Amount
- The actual transaction amount .
- Important for cost-sensitive fraud detection.
3. Class
   Target label
    - 0 → Legitimate transaction
    - 1 → Fraudulent transaction

### Why This Dataset?
- **Research benchmark:** Used in hundreds of ML papers for fraud detection performance comparison.
- **Temporal + behavioral patterns:** Allows both time-based and feature-based fraud analysis.


## 3. Algorithms Used
### 3.1 Logistic Regression
- A linear model that separates fraud vs. non-fraud using a decision boundary.
- It calculates fraud probability using the sigmoid function.
- Works well for:
  - linearly separable patterns
  - fast predictions
  - baseline fraud detection models
### How It Detects Fraud ?
- Learn relationships between V1–V28 + Amount and the Class.
- If the weighted sum is strongly positive → predicts fraud.
- If negative → predicts legitimate.
- Outputs a probability (0–1), making it suitable for risk scoring.

### 3.2 Random Forest Classifier
- A powerful ensemble model made of multiple decision trees.
- Each tree learns different patterns of fraud signals.
- The final prediction is a majority vote.
### How It Detects Fraud
Each decision tree checks:
- unusual patterns in features
- extreme feature deviations
- suspicious behavior combinations
- correlations found in historical fraud cases
The forest aggregates outputs:
- If most trees vote Fraud → Class 1
- If most trees vote Legit → Class 0
This makes it extremely effective for non-linear, complex, and imbalanced data.


## 4. Results & Evaluation
### Accuracy Scores and model comparisons
- Accuracy Comparison and confusion matrix
- High true-positive capture rate and Very few false negatives in confusion matrix


## 5. Interactive Application (Gradio App)
The system allows users to:
- Enter a transaction amount
- Auto-generate a realistic transaction profile
- Predict risk level using both models
- Output consensus recommendation:
  - Approve
  - Review
  - Block
This simulates real-banking fraud detection behaviour.


## 6. Conclusion
- Fraud detection is possible with high accuracy using machine learning.
- Random Forest outperforms Logistic Regression due to its ability to learn complex patterns.
- Components (V1–V28) play the biggest role in detecting hidden fraud signals.
- Even with imbalanced data, proper preprocessing + scaling + model selection gives strong results.
- The Gradio application provides an interactive, real-world demo of how fraud detection systems function.


## 7. Future Scope
- Add deep learning models
- Deploy the Gradio app online with a proper backend API
- Build a live fraud detection dashboard
- Use SHAP for model explainability
- Integrate with real-time transaction streams




## 8. References
- Transaction Fraud 2023 Dataset (Kaggle)
- Scikit-Learn Documentation
- Imbalanced Learning Concepts
- Random Forest Classification Papers
- Gradio Library Documentation
