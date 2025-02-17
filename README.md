# Multiple Linear Regression for Predicting Highway MPG

## Overview

This Jupyter Notebook implements a Multiple Linear Regression (MLR)
model to predict Highway Miles Per Gallon (MPG) based on various vehicle
attributes. The dataset used undergoes preprocessing, feature selection,
and model evaluation to ensure optimal performance.

## How to Open and Run the Notebook

Install Jupyter Notebook (if not installed):

pip install notebook pandas numpy scikit-learn

Launch Jupyter Notebook:

jupyter notebook

Navigate to the Notebook and execute each cell sequentially.

Ensure the dataset (cars.csv) is in the same directory as the notebook
for seamless execution.

## Key Insights from the Model

### Feature Selection & Multicollinearity Handling

The selected features include Height, Length, Width, Forward_Gears,
Driveline Types, and City_MPG, as they have low multicollinearity (VIF
\< 5) and a meaningful impact on fuel efficiency.

Features such as Hybrid, Fuel Type Variables, Horsepower, and Torque
were removed due to high correlation and redundancy, which could lead to
misleading model interpretations.

### Model Performance

Training & Testing Split: 80% of the data was used for training, while
20% was reserved for validation.

Evaluation Metrics:

R² Score: Approximately 0.90 (indicating a strong correlation between
selected features and highway MPG)

Mean Absolute Error (MAE): \~1.23

Root Mean Squared Error (RMSE): \~1.55

Impact of Outlier Removal: Removing extreme values slightly reduced R²
but improved generalizability, preventing overfitting.

## Predicting Highway MPG with the Model

After training, the model can predict Highway MPG for new vehicle data:

\# Example of predicting Highway MPG for a new vehicle import numpy as
np new_data = np.array(\[\[Height_value, Length_value, Width_value,
Forward_Gears_value, Driveline_Four_wheel_drive_value,
Driveline_Front_wheel_drive_value, Driveline_Rear_wheel_drive_value,
City_MPG_value\]\]) predicted_mpg = model.predict(new_data)
print(f\"Predicted Highway MPG: {predicted_mpg\[0\]:.2f}\")

Replace placeholders (Height_value, Length_value, etc.) with actual
vehicle measurements to obtain predictions.

## Conclusion

This model provides a reliable estimation of a vehicle\'s Highway MPG
based on key physical and mechanical features. Future enhancements could
explore non-linear regression techniques, feature engineering, or
additional real-world driving conditions to further improve predictive
accuracy.
