# Toronto Motorcycle Accident Severity Prediction

This project uses machine learning and clustering to predict the severity of motorcycle-related traffic accidents in Toronto, Ontario. Leveraging public datasets, seasonal patterns, and geolocation clustering, the application provides an interactive Flask-based interface to forecast whether a collision will result in property damage only or fatal/injury outcomes.

---

## 🚦 Project Overview

This project aims to:

- Analyze Toronto traffic and motorcycle collision data
- Engineer features such as seasonality, time of day, and distance from city center
- Build a predictive model to classify accidents by severity
- Serve predictions using a Flask web application with address-based geolocation

---

## 🗂️ Datasets Used

1. **Large Traffic Dataset**  
   [Toronto Police Service - Traffic Collisions (Open Data)](https://data.torontopolice.on.ca/datasets/bc4c72a793014a55a674984ef175a6f3_0/explore)

2. **Motorcycle KSI Dataset**  
   [Killed or Seriously Injured (KSI) Motorcycle Collisions Dataset](https://data.torontopolice.on.ca/datasets/d691a9391c2a4c6d85bb761530d33310_0/explore?location=43.721298%2C-79.378929%2C9.29)

---

## 🧠 Machine Learning Approach

- **Preprocessing**: Filtering motorcycle-related collisions and creating seasonal/time features
- **Feature Engineering**:
  - Season derived from `OCC_DATE`
  - Distance from Toronto’s geographic center
  - K-Means clustering based on coordinates
- **Model**: Gradient Boosting Classifier (sklearn)
- **Evaluation**: Trained to classify outcomes into:
  - `Property Damage Only`
  - `Fatal/Injury`

---

## 🌐 Flask Web App

Users can interact with the model through a simple UI. The app:

1. Accepts an address, time, and date as inputs
2. Geocodes the address using Google Maps API
3. Extracts features (hour, month, distance, cluster)
4. Returns the predicted accident severity and probability scores

---

## 💻 How to Run Locally

1. **Install requirements**:
    ```bash
    pip install -r requirements.txt
    ```

2. **Set your API key**:
    ```bash
    export GOOGLE_API_KEY=your_key_here
    ```

3. **Run the app**:
    ```bash
    python app.py
    ```

4. Open your browser at `http://127.0.0.1:5000/`

---

## 📊 Sample Visualizations

- Monthly distribution of accidents
- Seasonal trends affecting severity
- Severity prediction breakdowns

---



