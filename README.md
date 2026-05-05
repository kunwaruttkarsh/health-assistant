# Health Assistant

A Streamlit web app for predicting Diabetes, Heart Disease, and Parkinson's Disease using machine learning models trained from included datasets.

## 🌐 Live Web App
https://healthassistance.streamlit.app/

## Features

- Predicts Diabetes risk based on user health inputs.
- Predicts Heart Disease risk using common cardiac measurements.
- Predicts Parkinson's Disease risk using voice and speech-related features.
- Built with Streamlit for an interactive browser interface.

## Project Structure

- `main.py` - Streamlit application source code.
- `requirements.txt` - Python dependencies.
- `saved_models/` - Trained model files used for predictions.
- `dataset/` - Original dataset files (diabetes, heart, Parkinson's) used to train the models.
- `colab_files_to_train_models/` - Colab notebooks for model training and experimentation.
- `images/` - Dashboard images for the Home page.

## Training Data & Models

- Diabetes
  - Dataset: `dataset/diabetes.csv` (PIMA Diabetes Dataset)
  - Model: `sklearn.svm.SVC(kernel='linear')`
  - Train/test split: 80/20 with stratified sampling
  - Accuracy: training 78.34%, test 77.27%

- Heart Disease
  - Dataset: `dataset/heart.csv`
  - Model: `sklearn.linear_model.LogisticRegression()`
  - Train/test split: 80/20 with stratified sampling
  - Accuracy: training 85.12%, test 81.97%

- Parkinson's Disease
  - Dataset: `dataset/parkinsons.csv`
  - Model: `sklearn.svm.SVC(kernel='linear')`
  - Train/test split: 80/20
  - Accuracy: training 87.18%, test 87.18%

## Requirements

Install the dependencies with:

```bash
pip install -r requirements.txt
```

## Run Locally

From the project root:

```bash
streamlit run main.py
```

Then open the local Streamlit URL shown in the terminal.

## Usage

1. Open the app.
2. Use the sidebar navigation to select one of:
   - Home
   - Diabetes Prediction
   - Heart Disease Prediction
   - Parkinson's Prediction
   - About
3. Enter the required values for the selected prediction.
4. Click the prediction button to see the result.

## Notes

- The app expects numerical input values for prediction.
- The models are loaded from `saved_models/`.
- The datasets used to train the models are available in the `dataset/` folder.
- Training notebooks are available in `colab_files_to_train_models/`.

## Author

**Kunwar Uttkarsh Singh**
