# Heart Disease Prediction Web App

A Streamlit-based web application for predicting heart disease risk using machine learning.

## 🎯 Overview

This application uses a trained K-Nearest Neighbors (KNN) model to predict the risk of heart disease based on various medical parameters. The model was trained on a dataset of 918 patients with 12 different features.

## 🚀 Features

- **Interactive Interface**: User-friendly web interface built with Streamlit
- **Real-time Prediction**: Instant heart disease risk assessment
- **Comprehensive Input**: 11 different medical parameters
- **Visual Feedback**: Clear success/error messages with emojis
- **Responsive Design**: Works on desktop and mobile devices

## 📊 Model Performance

- **Algorithm**: K-Nearest Neighbors (KNN)
- **Dataset**: 918 heart disease records
- **Features**: 12 medical parameters
- **Preprocessing**: StandardScaler normalization
- **Output**: Binary classification (High Risk/Low Risk)

## 🛠️ Installation & Setup

### Prerequisites
```bash
pip install streamlit pandas joblib scikit-learn
```

### Running the Application
```bash
streamlit run app.py
```

The app will open in your default web browser at `http://localhost:8501`

## 📋 Input Parameters

| Parameter | Type | Range/Options | Description |
|-----------|------|---------------|-------------|
| Age | Slider | 18-100 | Patient's age |
| Sex | Selectbox | M/F | Patient's gender |
| Chest Pain Type | Selectbox | ATA/NAP/TA/ASY | Type of chest pain |
| Resting BP | Number | 80-200 | Resting blood pressure (mm Hg) |
| Cholesterol | Number | 100-600 | Cholesterol level (mg/dL) |
| Fasting BS | Selectbox | 0/1 | Fasting blood sugar > 120 mg/dL |
| Resting ECG | Selectbox | Normal/ST/LVH | Resting electrocardiographic results |
| Max HR | Slider | 60-220 | Maximum heart rate achieved |
| Exercise Angina | Selectbox | Y/N | Exercise-induced angina |
| Oldpeak | Slider | 0.0-6.0 | ST depression induced by exercise |
| ST Slope | Selectbox | Up/Flat/Down | Slope of peak exercise ST segment |

## 🔧 Technical Details

### Model Files
- `KNN_heart.pkl`: Trained KNN model
- `scaler.pkl`: StandardScaler for feature normalization
- `columns.pkl`: Expected column names for input preprocessing

### Data Preprocessing
1. **Feature Encoding**: Categorical variables are one-hot encoded
2. **Normalization**: All features are standardized using StandardScaler
3. **Input Validation**: Ensures all required columns are present

### Prediction Logic
```python
# Input preprocessing
input_df = pd.DataFrame([raw_input])
for col in expected_columns:
    if col not in input_df.columns:
        input_df[col] = 0

# Feature scaling and prediction
scaled_input = scaler.transform(input_df)
prediction = model.predict(scaled_input)[0]
```

## 🎨 User Interface

- **Title**: "Heart stroke prediction by Heisenberg"
- **Input Form**: Interactive sliders and selectboxes
- **Predict Button**: Triggers the prediction process
- **Results**: 
  - ✅ Green success message for low risk
  - ⚠️ Red warning message for high risk

## 📈 Usage Example

1. Open the application in your browser
2. Fill in the patient's medical information
3. Click the "Predict" button
4. View the risk assessment result

## 🔍 Model Training Details

The model was trained using:
- **Dataset**: Heart disease dataset with 918 samples
- **Features**: 12 medical parameters
- **Target**: Binary classification (0: No heart disease, 1: Heart disease)
- **Preprocessing**: One-hot encoding + StandardScaler normalization
- **Algorithm**: K-Nearest Neighbors

## 🚨 Important Notes

- This application is for educational and demonstration purposes
- **Not intended for medical diagnosis or treatment decisions**
- Always consult healthcare professionals for medical advice
- Model accuracy may vary with different populations

## 🔗 Related Files

- `Heart.ipynb`: Jupyter notebook with model training and analysis
- `heart.csv`: Original dataset used for training
- Model files: `KNN_heart.pkl`, `scaler.pkl`, `columns.pkl`

## 📝 License

This project is part of the ML Projects Portfolio. See main README for license information.

---

**Developer**: Ankushsph  
**GitHub**: [https://github.com/Ankushsph](https://github.com/Ankushsph)
