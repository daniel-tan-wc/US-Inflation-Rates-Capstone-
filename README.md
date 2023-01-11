
<h3 align="center">Forecasting US Inflation Rates in 2023</h3>

<br />
<div align="center">
  <a href="https://github.com/clone326/US-Inflation-Rates-Capstone-">
    <img src="https://www.uab.edu/news/images/2018/Inflation_stream.png" alt="Inflation" width="200" height="200">
  </a>

<div align="left">
  
  ## Table of Contents
  
1. [About the Project](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#about-the-project)
2. [Libraries used](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#libraries-used)
3. [Exploratory Data Analysis](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#exploratory-data-analysis)
      - [Correlation Heatmap](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#correlation-heatmap)
4. [fbProphet](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#fbprophet)
      - [Univariate](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#univariate)
      - [Seasonality](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#seasonality)
      - [Multivariate](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#multivariate)
5. [Final approach](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#final-approach)
6. [Tableau Dashboard](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#tableau-dashboard)
7. [Conclusion](https://github.com/clone326/US-Inflation-Rates-Capstone-/edit/main/README.md#conclusion)

## About The Project

<div align="left">
This is a Capstone project using a Timeseries ML model (FbProphet) to forecast US Inflation rates in 2023. Many factors contributes to Inflation but the main drivers are:
  
1. Consumer Price Index
2. Employment
3. Wages
4. Country's Gross Domestic Product
5. Federal and Bank Interest Rates
6. Currency Strength
7. Import & Export Price Index

Data on these inflation drivers was downloaded from <a href="https://beta.bls.gov/dataQuery/search">here</a><img src="https://beta.bls.gov/images/bls_emblem_trans.png" alt="Data Finder" width="80" height="80">

## Libraries Used
  ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=plastic&logo=pandas&logoColor=white)\
  ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=plastic&logo=plotly&logoColor=white)\
  ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=plastic&logo=Matplotlib&logoColor=black)\
  ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=plastic&logo=scikit-learn&logoColor=white)\
  ![Custom badge](https://img.shields.io/static/v1?label=fbProphet&message=0.7.1&color=informational&style=plastic)

## Exploratory Data Analysis
  ### Data Types
  Data columns | dtypes |
  --- | --- 
  Date | datetime64[ns] 
  CPI for All items | float64
  CPI for Commodities less Food and Energy | float64
  CPI for Communication | float64
  CPI for Education | float64
  CPI for Energy | float64
  CPI for Food | float64
  CPI for Gas | float64
  CPI for Medical Services | float64
  CPI for Shelter | float64
  Employment | int64
  Export Price Index | float64
  Fed rates | float64
  Import Price Index | float64
  Unemployment | int64
  Hourly Earnings | float64
  Avg Bank Rates | float64
  Nominal GDP | float64
  USD Strength | float64

  ### Consumer Price Index
  ![CPI](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/CPI.png?raw=true)
  You can see that the Financial crisis and Covid-19 hit Gas and Energy very hard
  
  ### Import/Export Price Index
  ![Import Export index](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Import_Export.png?raw=true)
  
  ### Employment
  ![Employment](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Employment.png?raw=true)
  Financial crisis affected employment and unemployment figures more gradually compared to Covid-19.
  This is also because the financial crisis was a more gradual build up compared to the pandemic.
  Covid-19 eliminated alot of jobs given that physical contact is present in numerous events, activities and businesses.
  
  ### Fed & Bank Rates
  ![Fed and Bank rates](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Fed%20&%20Bank%20rates.png?raw=true)
  Naturally, financial crisis would hit interest rates harder than a pandemic, and we can also see rates being an all time low during 2021 to boost economic activity.
  
  ### USA's GDP
  ![GDP](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/GDP.png?raw=true)
  Sharp hit again by the pandemic as opposed to the financial crisis
  
  ## Correlation Heatmap
  
  ![Correlation Heatmap](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Correlation%20Heatmap.png?raw=true)
  
  Key Positive Correlational Features:
  
  ![image](https://user-images.githubusercontent.com/113367891/210975593-d1f599f2-fb0d-4a3b-8e5a-251494e81469.png)
  
  Key Negative Correlational Features:
  
  ![image](https://user-images.githubusercontent.com/113367891/210975654-7f74edd2-13bf-4c7b-bb6a-eddea99c6aa7.png)


  ## fbProphet
  Introduction: fbProphet (or Prophet) is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.
  
Prophet is [open source software](https://code.facebook.com/projects/) released by Facebook’s [Core Data Science team](https://research.fb.com/category/data-science/). It is available for download on [CRAN](https://cran.r-project.org/package=prophet) and [PyPI](https://pypi.python.org/pypi/prophet/).
  
  [![Custom badge](https://img.shields.io/static/v1?label=Support&message=For-more-Info&color=informational&style=plastic)](https://facebook.github.io/prophet/)
  
  ## Univariate
  Model was trained based on only 1 variable, "CPI for all items".
  ![Univariate](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Forecast_Univariate.png?raw=true)
  
  After the train-test split of 80-20, Evaluation metrics used:
  * Mean Absolute Error = 7.27
  * Mean Absolute Percentage Error = 2.55%
  
  This means that the model is off by 7.27 index points which is about 2.55% (This is our baseline).
  
  ## Seasonality
  Model was trained based on only 1 variable, "CPI for all items", and
  ```sh
  model_season = Prophet(yearly_seasonality=True)
  model_season.add_seasonality(period = 30.4, name='monthly', fourier_order=5)
  ```
  ![Seasonality](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Forecast_Seasonality.png?raw=true)
  
  After the train-test split of 80-20, Evaluation metrics used:
  * Mean Absolute Error = 8.07
  * Mean Absolute Percentage Error = 2.84%
  
  This means that the model is off by 8.07 index points which is about 2.84% (Worst than baseline :-1::thumbsdown:).
  
  ## Multivariate
  Model was trained with all variables, "CPI for all items"
  ```sh
  # Create prophet model
  model_multivariate = Prophet()

  # Add regressor
  for i in data.columns[3:]:
    model_multivariate.add_regressor(i, standardize=False)
  ```
  ![Multivariate](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Forecast_Multivariate.png?raw=true)
  
  After the train-test split of 80-20, Evaluation metrics used:
  * Mean Absolute Error = 3.52
  * Mean Absolute Percentage Error = 1.25%
  
  This means that the model is off by 3.52 index points which is about 1.2% (Better than baseline :-1::thumbsup:).
  
  ## Final Approach
  
  In order to predict beyond the dataset's dates, i.e. Nov 2022 onwards, we will need to forecast the other feature variables before inserting them into our Multivariate model to predict our label "CPI for all items".
  
  Hence, 2 dictionaries were created to generate the univariate models and forecasted values for each of our feature variables:
  1. model_dictionary
  2. forecast_dictionary
  ```sh
  model_list = data.columns[2:]

model_dict = {}

forecast_dict = {}

for idx, key in enumerate(model_list):
    # print("Moving onto next data column.")

    data_sliced = data.iloc[:,[0, idx + 2]]
    data_sliced.rename(columns = {data_sliced.columns[1]:'y'}, inplace=True)
    # print("Data sliced and renamed.")
    
    #Training model with seasonality
    # print("Starting model training.")
    model_fb = Prophet(yearly_seasonality=True)
    model_fb.add_seasonality(period = 30.4, name='monthly', fourier_order=5)
    model_fb.fit(data_sliced)
    model_dict[key] = model_fb

    # print("Starting future forecast.")
    #Create time range for the forecast
    future = model_fb.make_future_dataframe(periods = 10, freq = 'MS')
    
    #Make forecast prediction
    forecast = model_fb.predict(future)
    forecast_dict[key] = forecast
    # print("Forecast generated and stored.")
 ```
  
  `Each forecasted value for the feature variables can be viewed after downloading the Capstone_dataset.csv and running the Captsone Assignment_Daniel Tan.ipynb`
  
  After adding forecasted values of feature variables onto the dataset, I fit the dataset into our trained multivariate model to predict "CPI for all items" from Nov 2022 till Aug 2023 (I chose an arbitrary number of 10 months for future prediction)
  Result:
  ![Final](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/True_Predict_MultiVariate.png?raw=true)
  
  
  ## Tableau Dashboard
  This dashboard allows you to set the date range, choose which CPI type you wish to view in the line graph and also choose which inflation type you wish to see in the table below for its monthly changes.
  `Caveat: Some inflation values may not be seen as the change is negligible (below 2 decimal percentages)`
  ![image](https://user-images.githubusercontent.com/113367891/211807927-060f2a11-ff2e-47b2-a2e4-e90ed7f80356.png)
  
  ## Conclusion
  November 2022 is supposed to be the month that inflation drops the most because of:
  * CPI drop in Energy :battery: and Gas :fuelpump:
  * High Fed and Bank Rates :bank:
  * Weaker USE strength :us:
  
  However, because the data was up till Oct 2022, and in Dec 2022 Fed and Bank rates increased again.
  
  [Forbes News Link](https://www.forbes.com/sites/simonmoore/2022/12/15/fed-sees-further-hikes-in-2023-heres-what-could-change-that/?sh=7f9a4a255a17)
  
  We **MAY** see inflation drop this month (Jan 2022)
