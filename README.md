# Sonar binary classification

A small Jupyter/Google Colab example that trains a Logistic Regression classifier on sonar measurements. The repository name is historical; this notebook performs **classification**, not regression.

## Notebook workflow

1. Load `sonar_data.csv` and inspect its shape and class counts.
2. Use the first 60 columns as input measurements and the last column as the class label.
3. Create a stratified 90/10 train/test split.
4. Train Logistic Regression and print test accuracy.
5. Enter one sample and print the predicted class.

The notebook maps `R` to “rock” and currently displays `M` as “missile.” Verify the dataset's original label definitions before interpreting that class name. The repository does not include a verified test score.

## Run in Google Colab

1. Open [Missile_or_Rock_Prediction.ipynb](Missile_or_Rock_Prediction.ipynb).
2. Select **Open in Colab**.
3. Run the cells from top to bottom.
4. Upload `sonar_data.csv` when prompted.

## Run locally

```powershell
python -m pip install -r requirements.txt
jupyter notebook Missile_or_Rock_Prediction.ipynb
```

Place `sonar_data.csv` in the notebook's working folder first.

## Files

- `Missile_or_Rock_Prediction.ipynb` — notebook for data inspection, model training, evaluation, and a single-sample prediction.
- `requirements.txt` — pandas, NumPy, Matplotlib, and scikit-learn.
- `LICENSE` — project license.

## Limitations

This is a learning demonstration. It reports accuracy only; it does not include cross-validation, a confusion matrix, probability calibration, or a saved model. Do not use its predictions for real-world safety or defense decisions.
