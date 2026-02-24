#Smart-Heating: Room Occupancy Detection

## Project Overview
Heating empty rooms wastes energy, but turning the heating off completely decreases comfort. This project builds a Machine Learning model to predict room occupancy based on environmental sensor data (Temperature, Humidity, CO2), enabling smart heating optimization.

## Tech Stack
- Language: Python

- Libraries: Pandas, NumPy, Scikit-Learn, Plotly, Seaborn

- Models: Logistic Regression, Decision Tree, Random Forest

## Data Processing & Feature Engineering
- Data Cleaning: Removed sensor anomalies and interpolated missing values to prevent data leakage.

- Feature Engineering: Extracted working hours and weekends from timestamps, added quadratic features for temperature/humidity, and calculated 5-minute rolling differences for CO2 levels.

- Encoding: Applied One-Hot Encoding for categorical time variables.

## Key Results & Business Impact
Due to class imbalance, the models were evaluated using F1-Score and validated via TimeSeriesSplit to respect the chronological order of the data.

- Best Model: Random Forest.

- Business Value: Successfully optimized the classification threshold to find the perfect balance between two conflicting business metrics: minimizing unnecessary heating costs (False Positives) and minimizing the time people spend in a cold room (False Negatives).

## Repository Structure
- Datensatz-Sensor.csv — Raw sensor dataset.

- Übungsprojekt final.ipynb — Main Jupyter Notebook containing EDA, preprocessing, and model evaluation.
