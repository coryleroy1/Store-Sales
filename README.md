# Store-Sales
Ecuadorian store sales predictor

# Authors:
- Cory LeRoy
- Will Earley
- Alec Bothwell

# Directory
- data
    - raw
        - train.csv training data of the time series data
        - test.csv test data having the same features as the train data. dates in test are the 15 days after the train
        - stores.csv store metadata. includes city, state, type, and cluster
        - oil.csv daily oil price for both train and test timeframes
        - holiday_events.csv holidays and metadata
    - processed
        - df_train.pkl
        - df_val.pkl
        - df_test.pkl
        - df_train_fb.pkl
        - df_val_fb.pkl
        - df_test_fb.pkl
        



    


# Project Overview
Every year millions of pounds of food are wasted to do incorrect inventory predicitions by grocery stores. In this project we will be using time-series forecasting to forecaast stores sales on data from Corporación Favorita, an Ecuadorian based grocery retailer. We are building a model that predicts the unit sales of items sold at different stores in the Favorita network. 

# Table of Contents
1. data - The raw and processed data are kept here.
2. code - This folder contains more basic exploratory analysis and early exploration of the data.
    - data exploration notebooks made by each of the team memebers
    - additional data exploration on Tableau
        - Holiday sales: https://public.tableau.com/app/profile/cory.leroy/viz/EcuadorianStoreholidays/holiday
        - Store cluster analysis: https://public.tableau.com/app/profile/cory.leroy/viz/EcuadorianStoreClusters/StoreClusters
        - Seasonality by day: https://public.tableau.com/app/profile/cory.leroy/viz/EcuadorianStoreSalesDailySeasonality/weeklyseasonality
4. Feature Engineering - This folder contains the notebooks describing how we extract and engineer important features we discovered during exploratory data analysis.
4. Models - We worked on several different models for this task. The model notebooks can be found and ran here for each of the models.  
5. documents - Important explanatory documents are in this folder.
    - milestone progress reports
    - data and model documentation

# Installing and running the project
1. download the train.csv file from https://drive.google.com/drive/folders/1jw7e5UprTug09C0tOb73oATMqk16qqKi, place it in the data > raw folder. the rest of the data files should already be in there
2. Create virtual environment and install requirements from requiremetns.txt found in the main directory. Then, activate the virtual environment. To do these steps from command prompt:
    - Create a new virtual inv: python -m venv nameofenv
    - activate new virtual env: nameofvenv\Scripts\activate
    - Install libraries from requirements doc. make sure you are in the main store sales folder. pip install -r requirements.txt
    

3. Run the Feature Engineering jupyter notebook. This creates pickle files for the cleaned train, validation, and test dataset in the data\processed folder
4. Move to the models folder and run FBProphetFinal, OLS, SARIMA, XGBoost. Models may take up to 20 min to run

# Credits
We used a variaty of resources to help us learn more about time series forecasting and the associated models, they can be found below.

https://ieeexplore.ieee.org/abstract/document/9752916
https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/
https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview
https://www.youtube.com/@ritvikmath
https://iopscience.iop.org/article/10.1088/1742-6596/1873/1/012067/pdf
https://dl.acm.org/doi/abs/10.1145/3355402.3355417
https://medium.com/@isaacrambo/revealing-the-power-of-time-series-forecasting-predicting-ecuadors-grocery-sales-with-precision-8c3b0bac97be
