# NYC Taxi Trip Duration Prediction

## 📌 Project Overview
This project focuses on predicting the duration of taxi trips in New York City. By leveraging geospatial and temporal data, I developed a machine learning model capable of estimating travel times, which is a critical component for logistics, urban planning, and ride-sharing efficiency.

## 🛠️ Technical Stack
- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn (Random Forest Regressor, KMeans, GridSearchCV)
- **Visualization:** Matplotlib, Seaborn, Folium (Geospatial Mapping)

## 🚀 Key Features & Implementation

### 1. Data Cleaning & Engineering
- **Geospatial Filtering:** Implemented hard boundaries for New York City coordinates (-74.03 to -73.75 Longitude, 40.63 to 40.85 Latitude) to remove noise and out-of-city trips.
- **Statistical Outlier Removal:** Utilized standard deviation (μ ± 2σ) to filter anomalous trip durations, ensuring model stability.
- **Feature Extraction:** - Calculated **Manhattan Distance** from raw GPS coordinates using the Haversine formula.
    - Engineered temporal features: `day_period` (Morning, Afternoon, Evening, Late Night), `season`, and `day_name`.

### 2. Machine Learning Pipeline
- **Clustering:** Used **K-Means Clustering** to identify high-traffic pickup and dropoff zones.
- **Regression:** Developed a **Random Forest Regressor** to handle non-linear relationships in the data.
- **Optimization:** Employed **GridSearchCV** for hyperparameter tuning to minimize error metrics.

### 3. Evaluation
The model was evaluated using:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R² Score:** Achieved a score of **~0.70**, indicating strong predictive power.

## 📊 Visualizations
The project includes interactive maps built with **Folium** to visualize pickup/dropoff densities and seaborn-based statistical distributions of trip patterns across different days of the week.

## 📂 Project Structure
- `tede-2.ipynb`: Full Jupyter Notebook containing data preprocessing, EDA, and model training.
- `data/`: (Not included) Dataset containing NYC taxi trip records.
