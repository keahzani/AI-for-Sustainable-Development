# 🌍 AI-Driven Crop Yield Forecasting for Food Security (SDG 2)

## Project Overview
This project demonstrates the application of supervised machine learning to the UN Sustainable Development Goal 2 (Zero Hunger). By analyzing historical climate, soil, and input data, a Random Forest Regression model is used to accurately forecast crop yields (tons per hectare). The goal is to provide actionable insights for proactive policy-making, resource allocation, and food security planning.

## 🚀 Technical Implementation

### ML Approach
- **Objective:** Regression (Predicting a continuous numerical value).
- **Model:** Scikit-learn's **Random Forest Regressor**.
- **Data:** A dataset of 1,000,000 records including variables like `Rainfall_mm`, `Temperature_Celsius`, `Fertilizer_Used`, and categorical features like `Region` and `Soil_Type`.

### Setup and Running the Code

1.  **Clone the Repository:**
    ```bash
    git clone [YOUR_REPO_LINK]
    cd SDG2_Crop_Predictor
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas scikit-learn matplotlib numpy
    ```
3.  **Data:** Ensure your `crop_data.csv` is in the project root directory.
4.  **Execute:** Run the code using Jupyter Notebook or Python.
    ```bash
    # If using a .py script:
    python crop_yield_predictor.py
    # If using a notebook:
    jupyter lab crop_yield_predictor.ipynb
    ```

## 📊 Model Performance and Results

The model achieved high predictive accuracy, validating its usefulness for large-scale forecasting.

| Metric | Result |
| :--- | :--- |
| **R-squared ($\mathbf{R}^2$) Score** | $\mathbf{0.907}$ |
| **Mean Absolute Error (MAE)** | $\mathbf{0.412 \text{ t/ha}}$ |

### 1. Prediction Accuracy Visualized

The scatter plot below shows a tight clustering of predicted values along the "Perfect Prediction" line, confirming the model's reliability across different yield values.

****
<img width="989" height="590" alt="prediction accuracy" src="https://github.com/user-attachments/assets/ae89d983-f4cd-4913-94d1-e802a9a05ad8" />

### 2. Feature Importance Analysis (Actionable Insight)

The Random Forest model quantified the importance of each input feature. This finding is crucial for guiding investment and policy.

| Feature | Importance Score |
| :--- | :--- |
| **Rainfall\_mm** | $\mathbf{0.607}$ |
| **Fertilizer\_Used** | $\mathbf{0.196}$ |
| **Irrigation\_Used** | $\mathbf{0.125}$ |
| Temperature\_Celsius | $0.029$ |
| Days\_to\_Harvest | $0.017$ |

****
<img width="989" height="590" alt="random forest feature" src="https://github.com/user-attachments/assets/8859b547-6e4d-4604-a00f-dbaadc8211bd" />
---
***Note:*** *This analysis highlights that water availability (Rainfall and Irrigation) is overwhelmingly the most critical factor, justifying prioritized investment in water management for food security.*
