# 🚢 Titanic Survival Prediction

A beginner machine learning project that predicts whether a Titanic passenger survived, based on features like age, sex, ticket class, fare, and family size — built from scratch using **Python**, **Pandas**, and **scikit-learn**.

## 📊 Result

**Model:** Logistic Regression
**Accuracy:** 73.7% on unseen test data

For comparison, always predicting "died" (the majority outcome) would only score ~61-62% — so the model genuinely learned meaningful patterns from the data.

## 🔍 Key Insight (from exploratory analysis)

| Group | Survival Rate |
|---|---|
| Female | 74.2% |
| Male | 18.9% |
| 1st Class | 63.0% |
| 3rd Class | 24.2% |
| Female + 1st Class | 96.8% |
| Male + 3rd Class | 13.5% |

Sex and Passenger Class were the two strongest predictors of survival.

## 🛠️ Tools Used

- Python
- Pandas & NumPy
- scikit-learn
- Google Colab

## 🧭 Pipeline

1. **Load & explore data** — inspected structure, spotted missing values
2. **Exploratory analysis** — survival rates by Sex, Pclass, and their combination
3. **Clean missing data** — Age filled with median, Cabin dropped (77% missing), Embarked filled with mode
4. **Drop unhelpful columns** — removed Name, Ticket, PassengerId
5. **Encode categorical data** — Sex mapped to 0/1, Embarked one-hot encoded
6. **Split features (X) and target (y)**
7. **Train/test split** — 80% train, 20% test
8. **Train model** — Logistic Regression (`max_iter=1000`)
9. **Evaluate** — predictions vs. actual outcomes on the test set

Full write-up with code snippets: [`Titanic_Survival_Prediction_README.pdf`](./Titanic_Survival_Prediction_README.pdf)

## 📁 Files

- `titanic_survival_prediction.ipynb` — the full notebook
- `Titanic_Survival_Prediction_README.pdf` — detailed step-by-step write-up

## 🚀 Possible Next Steps

- Try a Random Forest classifier for comparison
- Inspect a confusion matrix
- Feature engineering: FamilySize (SibSp + Parch), Title extraction from Name
- Hyperparameter tuning

---
*Built as a self-guided learning project.*
