# House-pricing

![image](https://github.com/user-attachments/assets/3b32e62f-bbbd-4acd-81dd-8c52936e0e0c)



## 📋 Overview

This project implements a machine learning model to predict California house prices based on various features including location, size, population, and more. The system provides accurate estimations using regression modeling techniques and is deployed as a web application using Flask.

## 🏠 Project Description

Real estate pricing is complex and depends on numerous factors. This project employs machine learning to analyze these factors and develop a predictive model that can estimate house prices with high accuracy. The project follows a complete end-to-end machine learning workflow:

- **Data Collection & Analysis**: Using the California Housing dataset with features like median income, housing age, room counts, location coordinates
- **Data Preprocessing**: Handling missing values, feature scaling, and encoding
- **Model Development**: Training and optimizing regression algorithms
- **Web Application**: Interactive interface for users to input property details and receive price predictions
- **Deployment**: Containerized application with CI/CD pipeline

## 🔧 Technologies Used

### Machine Learning
- Scikit-learn
- NumPy
- Pandas
- Pickle (for model serialization)

### Web Development
- Flask
- HTML/CSS with responsive design
- Bootstrap for UI components
- JavaScript for interactivity

### DevOps
- Docker for containerization
- Git for version control

## 📊 Machine Learning Pipeline

1. **Exploratory Data Analysis (EDA)**: 
   - Statistical analysis of the dataset
   - Visualization of feature distributions and correlations
   - Identification of key predictors for house prices

2. **Data Preprocessing**:
   - Handling missing values in features like bedrooms
   - Feature scaling to normalize numeric values
   - Converting categorical features to numerical representation

3. **Model Selection & Training**:
   - Implemented multiple regression models:
     - Linear Regression
     - Random Forest
     - XGBoost
   - Hyperparameter tuning using GridSearchCV
   - Cross-validation to ensure model robustness

4. **Evaluation**:
   - R-squared score: 0.83
   - Mean Absolute Error (MAE): 0.31
   - Root Mean Squared Error (RMSE): 0.42

## 💻 Web Application

The project includes a user-friendly web interface built with Flask that allows users to:
- Input property details (location, size, rooms, etc.)
- Receive instant price predictions
- Visualize the impact of different features on the predicted price

The application features:
- Responsive design that works on both desktop and mobile
- Intuitive form with tooltips explaining each input
- Professional styling with modern UI components

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Installation

1. Clone the repository
   git clone https://github.com/yourusername/House-pricing.git
cd House-pricing
2. Install dependencies
   pip install -r requirements.txt
3. Run the Flask application
   python app.py
4. Open your browser and navigate to `http://localhost:5000`

## 📊 API Usage

The application also provides a REST API endpoint for integrating with other systems:

```python
# Example API call
import requests
import json

url = 'http://localhost:5000/predict_api'
data = {
 'data': {
     'MedInc': 8.3252,
     'HouseAge': 41.0,
     'AveRooms': 6.984127,
     'AveBedrms': 1.02381,
     'Population': 322.0,
     'AveOccup': 2.555556,
     'Latitude': 37.88,
     'Longitude': -122.23
 }
}

response = requests.post(url, json=data)
print(response.json())
```
Results and Insights
Through this project, several key insights were discovered:

Median income is the strongest predictor of house prices.
Location (latitude and longitude) significantly impacts property values.
Age of housing has a non-linear relationship with price.
The model performs better in urban areas compared to rural regions.

