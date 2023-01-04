
<h3 align="center">Forecasting US Inflation Rates in 2023</h3>

<br />
<div align="center">
  <a href="https://github.com/clone326/US-Inflation-Rates-Capstone-">
    <img src="https://www.uab.edu/news/images/2018/Inflation_stream.png" alt="Inflation" width="200" height="200">
  </a>

<div align="left">
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#libraries-used">Libraries Used</a></li>
      </ul>
    </li>
    <li><a href="#EDA">Exploratory Data Analysis</a></li>
    <li><a href="#correlation">Correlation Heatmap</a></li>
    <li><a href="#fbpropher">FbProphet</a>
      <ul>
        <li><a href="#univariate">Unviariate model</a></li>
        <li><a href="#seasonality">Seasonality model</a></li>
        <li><a href="#multivariate">Multiariate model</a></li>
      </ul>
    </li>
    <li><a href="#final">Final approach with FbProphet</a></li>
    <li><a href="#tableau">Tableau dashboard</a></li>
  </ol>
</details>

## About The Project

<div align="left">
This is a Capstone project using a Timeseries ML model (FbProphet) to forecast US Inflation rates in 2023. Many factors contributes to Inflation but the main drivers are:
1. Consumer Price Index
2. Employment
3. Wages
4. Country's Gross Domestic Product
5  Federal and Bank Interest Rates
6. Currency Strength
7. Import & Export Price Index

Data on these inflation drivers was downloaded from <a href="https://beta.bls.gov/dataQuery/search">here</a><img src="https://beta.bls.gov/images/bls_emblem_trans.png" alt="Data Finder" width="80" height="80">

## Libraries Used
* Pandas
* Plotly
* matplotlib
* sklearn
* fbProphet



<!-- Data columns | dtypes |
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
USD Strength | float64 -->
