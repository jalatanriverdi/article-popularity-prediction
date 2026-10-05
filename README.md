# Article Popularity Prediction

This project predicts whether a Mashable article will become popular based on article-level features available before publication.

An article is considered popular if it receives at least 1,400 social media shares. The evaluation metric is ROC-AUC, so the model predicts probabilities for the positive class.

## Project Structure

```text
.
├── data/
│   ├── train.csv
│   ├── test.csv
│   ├── metaData.csv
│   └── sample_submission.csv
├── article_popularity.ipynb
├── submission.csv
├── README.md

```

## Approach

The notebook covers data exploration, preprocessing, feature engineering, model comparison, hyperparameter tuning, and final prediction.

A chronological train/validation split is used because the test set contains articles published later than the training data.

The models compared are:

- Logistic Regression
- LightGBM
- CatBoost

The final model is a tuned CatBoost classifier using the engineered feature set.

## Requirements

Install the required packages with:

```bash
pip install pandas numpy matplotlib scikit-learn catboost lightgbm
```

## Run

Open `article_popularity.ipynb` and run the cells from top to bottom.

The final cell creates `submission.csv` in the required competition format.
