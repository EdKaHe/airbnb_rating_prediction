# airbnb_rating_prediction

## Introduction
This repository results from my Udacity Nanodegree. The goal is to analyse datasets from 
[Inside Airbnb](http://insideairbnb.com/get-the-data.html) and predict potential ratings of housings that are not rated yet. 
Several graphs and key figures are shown during the analysis process to reveal dependencies and assess the performance of the model.
In a first step the data is loaded and cleaned using a custom function. The as the cleaning process is time consuming the cleaned data is saved
to a seperate spreadsheet. Data cleaning is performed on the listings in Amsterdam, Boston and Stockholm but can be done
with any other city available at Inside Airbnb. The cleaned data is modeled by cross-validated lasso regression to prevent overfitting and
have an easy model that can be set up fast and provides additional insights. The notebook is designed according to the **Cr**oss-**I**ndustry **S**tandard **P**rocess for **D**ata **M**ining (CRISP-DM) in order to
have a consistent structure. 

## Data Acquisition
The data can be downloaded from [Inside Airbnb](http://insideairbnb.com/get-the-data.html). For the analysis the zipped listings dataset of
any city can be used. The original and cleaned datasets of Boston, Amsterdam and Stockholm are available in this GitHub.

## Files
This repository contains the jupyter notebook "airbnb.ipynb" for the data engineering and modeling
and the original and cleaned datasets of the Airbnb listings in Boston, Stockholm and Amsterdam.

## Problem Formulation
The key questions are:
- On which factors does the rating of a listing depend the most?
- How accurately can we predict the actual rating?
- How do different cities compare?

## Results
The key findings are that the rating of a listing strongly depends on factors that are determined rather by the host than the housing
itself. The model performance was good for highly rated offers between 85 and 100. For lower ratings not enough data was available to
ensure a reliable performance with the methods used. The model achieves a good average prediction performance but is not able to map the
full complexity of the underlying processes. More sophisticated feature engineering and more complex models are promising to drastically
improve the performance. More detailed information can be found at [Medium](https://medium.com/@edizherkert/how-can-you-predict-airbnb-ratings-125a5491db3e).

## Further Notes
Please be aware that you have to enter your own mapbox access token in order to use the scattermapbox capability of plotly. 
