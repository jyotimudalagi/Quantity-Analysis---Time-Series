Quantity Analysis & Forecasting — Time Series Project

This repository contains an end-to-end time series analysis and forecasting workflow built to study and predict product sales quantities over time using Python.

Files included:

Quantity_Analysis_TimeSeries_Structured.ipynb — A Jupyter notebook that walks through the full analytical pipeline: loading the raw sales data, aggregating daily quantities sold across products, performing seasonal decomposition (trend, weekly seasonality, and residuals) using statsmodels, and fitting an ARIMA model to forecast future demand. The notebook concludes with a train/test evaluation (RMSE, MAE, MAPE) and a plotted comparison of forecasted versus actual values, along with suggestions for future improvement (SARIMA, Prophet, LSTM).
Raw_Data_Predictive_Analysis.xlsx — The source dataset, containing 40,563 rows and 9 columns of transactional-level sales data. Key fields include OrderDate, ParentProductIdNew, ParentProductNew, ProductCategoryNew, ArtistNameNew, total_qty_sales, Selling Price, productListViews, and productListClicks. Each row represents an order for a specific product on a given date, making it suitable for both time series aggregation and product-level predictive analysis.
requirements.txt — Lists all Python dependencies needed to run the notebook, including pandas, numpy, matplotlib, seaborn, statsmodels, scikit-learn, openpyxl, and jupyter.

Project workflow:

Load and clean the raw Excel dataset.
Aggregate quantity sold per day to build a single univariate time series.
Decompose the series into trend, seasonal, and residual components.
Split data into training and test sets (90/10).
Fit an ARIMA model as a baseline forecasting method.
Evaluate model performance using standard error metrics and visualize forecasted vs. actual quantities.

Use case: This project is useful for e-commerce or retail businesses looking to understand demand patterns and build a baseline forecasting model for inventory planning, sales trend analysis, or business decision support.

Note: Before running the notebook, ensure the Excel file path matches your local directory structure, and install dependencies via pip install -r requirements.txt.
