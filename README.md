# Credit Card Fraud Detection — ML vs Deep Learning

An end-to-end fraud detection system built on 284,807 real credit card transactions. This project benchmarks a Logistic Regression baseline against a Deep Learning neural network, with a focus on business-relevant metrics and operational decision-making.

---

## Project Structure

| Section | Description |
|---|---|
| 1. Project Architecture | Problem definition, objectives, and expected benefits |
| 2. Environment Setup | Library imports and version control |
| 3. Data Ingestion | Kaggle API integration, loading, and structural audit |
| 4. EDA | Class imbalance, transaction value, temporal, and correlation analysis |
| 5. Preprocessing | RobustScaler, train-test split, class weight computation |
| 6. Baseline Model | Logistic Regression benchmark with performance analysis |
| 7. Deep Learning Model | Neural network architecture, compilation, and training |
| 8. Evaluation | Confusion matrix, model comparison, and threshold tuning |
| 9. Business Insights | Operational strategy and financial ecosystem impact |

---

## Dataset

- **Source**: [Credit Card Fraud Detection — Kaggle (ULB)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Size**: 284,807 transactions over 48 hours
- **Imbalance**: 0.17% fraudulent transactions (492 fraud vs 284,315 legitimate)
- **Features**: V1–V28 (PCA-anonymized), Amount, Time

---

## Results

| Metric | Logistic Regression | Neural Network (0.5) | Neural Network (optimal) |
|---|---|---|---|
| Recall (Fraud) | 92.0% | 86.7% | 81.6% |
| Precision (Fraud) | 6.0% | 15.6% | 77.7% |
| ROC-AUC | 0.9720 | 0.9136 | 0.9136 |
| F1-Score (Fraud) | — | — | 0.796 |

**Key finding**: The neural network more than doubles precision over the baseline (6% → 15.6% at default threshold, 77.7% at optimal threshold), meaning 5x fewer legitimate customers are incorrectly flagged — a critical operational gain in any high-volume payment ecosystem.

---

## Tech Stack

- **Language**: Python 3.12
- **Deep Learning**: TensorFlow 2.20 / Keras 3.13
- **ML**: Scikit-learn 1.6
- **Data**: Pandas 2.2, NumPy 2.0
- **Visualization**: Matplotlib 3.10, Seaborn 0.13
- **Environment**: Google Colab

---

## How to Run

- **View notebook**: [Open in NBViewer](https://nbviewer.org/github/MarcoMPinto/credit-card-fraud-detection-ml-vs-dl/blob/main/credit_card_fraud_detection_ml_vs_dl.ipynb)
- **Run notebook**: Open in [Google Colab](https://colab.research.google.com/drive/19pMP0BNMAPjf3-iEttmeXyXmBzMtYyco?usp=sharing) (Google account required)
  - Go to left sidebar → 🔑 Secrets
  - Add `KAGGLE_USERNAME` and `KAGGLE_KEY`
  - Run all cells (`Runtime → Run all`)

---

## Author

**Marco Antonio Moreira Pinto**
