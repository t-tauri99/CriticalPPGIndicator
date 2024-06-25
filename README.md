# CriticalPPGIndicator

## Objective
Photoplethysmography(PPG) signal to indicate a critically ill patient. Cardiovascular diseases (CVDs) have become a major contributor to human mortality. Therefore, early diagnosis, treatment, and control of hypertension could play an important role in the prevention and treatment of CVDs. The objective of our project is to design a model for classification of Photoplethysmography (PPG) signal to detect an elevated shock index which can indicate a critically ill patient. 

## Methodology
Our approach utilizes a three-part process to analyze PPG signals and predict critical illness:

1. **Heart Beat Detection**: Identify cardiac cycles from the PPG signals to determine heart rate.
2. **Blood Pressure Extraction**: Analyze arterial blood pressure (ABP) signals to extract systolic and diastolic values.
3. **Deep Learning Classification**: Apply advanced modeling techniques to classify the extracted features according to the shock index, determining the likelihood of critical illness.

## Model Building Approaches
To achieve our objective, we are experimenting with three distinct modeling techniques:
- **Self-Tuned Deep Neural Network (DNN)**
- **DNN with Keras Tuner**
- **Random Forest Classifier**

After building these models and comparing their performance we will select the model with highest train and test accuracy thus fitting our use case.

## Workflow

### Data Analysis and Record Selection
- **Notebook: `records_suitable_for_analysis.ipynb`**
  - Analyze patient records to identify suitable PPG and ABP signals.
  - Ensure each signal is at least 2 minutes long and free from significant gaps or artifacts, making them viable for detailed analysis.

### Feature Extraction and Dataset Preparation
- **Notebook: `DeepLearningDatasetPreparation.ipynb`**
  - Process the selected signals to detect heartbeats and extract blood pressure values.
  - Compile the features into a structured DataFrame, ready for input into our models.
  - Finally as a baseline comparison we also implement a Random Forest Classifer. **Notebook: `Random_forest_classifier.ipynb`**
