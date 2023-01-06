
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
4. [fbProphet](url)
      - [Univariate]
      - [Seasonality]
      - [Multivariate]
5. [Final approach]
6. [Tableau Dashboard]

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
  Naturally, financial crisis would hit interest rates harder than a pandemic, but we can also see rates being an all time low during 2021 to boost economic activity.
  
  ### USA's GDP
  ![GDP](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/GDP.png?raw=true)
  Sharp hit again by the pandemic as opposed to the financial crisis
  
  ## Correlation Heatmap
  
  ![Correlation Heatmap](https://github.com/clone326/US-Inflation-Rates-Capstone-/blob/main/Images/Correlation%20Heatmap.png?raw=true)
  
  Key Positive Correlational Features:
  
  ![image](https://user-images.githubusercontent.com/113367891/210975593-d1f599f2-fb0d-4a3b-8e5a-251494e81469.png)
  
  Key Negative Correlational Features:
  
  ![image](https://user-images.githubusercontent.com/113367891/210975654-7f74edd2-13bf-4c7b-bb6a-eddea99c6aa7.png)


  
