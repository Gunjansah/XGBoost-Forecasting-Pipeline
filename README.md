# XGBoost-Forecasting-Pipeline
### An end-to-end time series forecasting project using XGBoost and Streamlit to predict sales demand for retail products.

---

##  Project Overview

This project presents an end-to-end solution for forecasting daily sales demand for an online retail business. Using a large transactional dataset spanning two years, this repository demonstrates a complete machine learning workflow: from rigorous data cleaning and advanced feature engineering to training multiple specialized models and deploying them in a user-friendly, interactive dashboard.

The primary goal is to provide accurate product-level forecasts that can help a business optimize inventory, reduce stockouts, and make data-driven decisions.

---

##  Key Features

-   **End-to-End Data Pipeline:** Ingests raw transactional data and processes it into a clean, model-ready format.
-   **Data Cleaning:** Implements a multi-step cleaning process to handle missing values, duplicates, returns, transactional outliers, and non-product entries.
-   **Feature Engineering:** Creates a rich feature set including time-based features (day, week, month), lag and rolling window statistics, and crucial UK holiday indicators.
-   **Multi-Model Forecasting:** Trains, evaluates, and saves a dedicated XGBoost regression model for each of the top 5 best-selling products.

---

## Tech Stack

-   **Data Manipulation & Analysis:** Python, Pandas, NumPy
-   **Machine Learning Model:** XGBoost
-   **Model Evaluation:** Scikit-learn
-   **Data Visualization:** Plotly
-   **Interactive Dashboard:** Streamlit
-   **Model Persistence:** Joblib
-   **Feature Engineering:** `holidays` (for national holidays)
-   **Development Environment:** Jupyter Notebook

---

###  Model Performance & Visualization

The following chart shows the model's predictions (dashed line) against the actual sales (solid line) for one of the top products. The model successfully captures the weekly seasonality and general sales trends.

![image1](https://github.com/user-attachments/assets/256becc5-6c06-4547-ad8b-dd0081f3fd59)
![image2](https://github.com/user-attachments/assets/ffe7eac3-b0bf-43fd-9e3a-3bdce330d78b)
![image3](https://github.com/user-attachments/assets/877cb26c-a67b-466c-9a5c-ad9049ca9503)
![image4](https://github.com/user-attachments/assets/66437bc4-c28b-49d0-b961-d78746e2441f)
![image5](https://github.com/user-attachments/assets/649d1357-d36e-4297-9d70-3d50c38753b2)





---


## Setup and Usage

To run this project locally, please follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/Gunjansah/XGBoost-Forecasting-Pipeline.git
    cd XGBoost-Forecasting-Pipeline
    ```

2.  **Install Dependencies**
    It's recommended to create a virtual environment first. Then, install the required packages from the `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Train the Models (Generate Model Files)**
    Run the Jupyter Notebook `XGBoost-Forecasting-Pipeline.ipynb` from start to finish. This will perform the analysis and, most importantly, will train the models. 


---

## Future Improvements

-   **Hyperparameter Tuning:** Implement `GridSearchCV` or `RandomizedSearchCV` with `TimeSeriesSplit` to systematically find the optimal hyperparameters for each XGBoost model.
-   **Experiment with Other Models:** Compare the performance of XGBoost against other time-series models like Facebook Prophet or deep learning models like LSTMs.
-   **Add Exogenous Variables:** Incorporate external factors that could influence sales, such as marketing spend, promotional calendars, or general economic indicators.
-   **Cloud Deployment:** Deploy the Streamlit dashboard to a cloud service like Streamlit Community Cloud for public access.
