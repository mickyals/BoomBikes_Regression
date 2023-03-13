# BoomBike Demand
> A multivariate regression model with the goal of predicting demand for a bike share service in the US as well as identify the variables with the most impact.. 

## Table of Contents
* data_dictionary.txt - data dictionary
* day.csv - dataset
* BoomBikes_Regression_Model_Mickell_Als.ipnb - notebook
* Model_Results.md - OLS Regression Outputs For Best Performing Models
* Linear_Regression_Subjective_Questions_Mickell_Als.pdf - pdf of questions and answers

## General Information
* Multiple Linear Regression
* Libraries used - Pandas, Numpy, Matplotlib.pyplot, Seaborn, Statsmodels, Scikit-Learn, SciPy

## Conclusions
 Based on the business objective and linear regression best practice - the model that should be selected should be able to explain most of the variability using the least number of features, with no multicollinearity, having a residual mean of 0, show homoscedasticity for the errors and show normality in the distribution of the errors. While all three models are not perfect, I believe model 13 is the best model. It retains a test set r2 of nearly 82%, while having the lowest residual mean value, the lowest Cond No, indicating little multicollinearity. was to project demand then a more complex model could be used such as Model 12 or Model 10. Our goal was prediction and thus the driving variables matter more.

1) Using manual and automatic feature selection (RFE), I was able to drop the number of initial features from 33 to 12 then manual selection to drop the features to 10 with only a minute drop in R-squared and a significant rise in the F statistic and significant drop in AIC while having all predictor p-values fall to near 0. This means the model is significantly less complex

2) On the training set, the model scored an R-squared value of 83.3% and on our test set the score was 81.7%. This indicates the model does a very good job of predicting demand in the dataset.

3) The equation for the best fit line is:

𝑐𝑛𝑡 = 0.2597 + 0.3577(𝑡𝑒𝑚𝑝) − 0.3004(𝐿𝑖𝑔ℎ𝑡_𝑃𝑟𝑒𝑐𝑖𝑝) + 0.2369(𝑦𝑟) − 0.1467(𝑤𝑖𝑛𝑑𝑠𝑝𝑒𝑒𝑑)  − 0.1402(𝑤𝑖𝑛𝑡𝑒𝑟) − 0.0822(𝑀𝑖𝑠𝑡/𝐶𝑙𝑜𝑢𝑑𝑦) + 0.0729(𝑆𝑒𝑝𝑡𝑒𝑚𝑏𝑒𝑟) + 0.0666(𝑆𝑎𝑡) + 0.0663(𝑂𝑐𝑡𝑜𝑏𝑒𝑟) + 0.0557(𝑤𝑜𝑟𝑘𝑖𝑛𝑔𝑑𝑎𝑦)

Based on the absolute values of the coeffients the following are the features with the most impact and their effect

|Position|Feature      | Coef   | Impact  |
|--------|-------------|--------|---------|
|   1    | temp        |  0.3577| Increase|
|   2    | Light_Precip| -0.3004| Decrease|
|   3    | yr          |  0.2369| Increase|
|   4    | windspeed   | -0.1467| Decrease|
|   5    | winter      | -0.1402| Decrease|
|   6    | Mist/Cloudy | -0.0822| Decrease|
|   7    | September   |  0.0729| Increase|
|   8    | Sat         |  0.0666| Increase|
|   9    | October     |  0.0663| Increase|
|   10   | workingday  |  0.0557| Increase|

#### Recommendations for BoomBike
Based on the available data, we can see that having a higher temperatures increases demand more so than all other features while Light_Precip decreases more so than other features. That being said, the yr variable clearly indicates that 2019 was linked to higher demand for services.

Days with the most demand would be warm Saturdays in September, with sunny skies and light winds in 2019.

# Acknowledgements

Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}


Contact
=========================================
	
For further information about this dataset please contact Hadi Fanaee-T (hadi.fanaee@fe.up.pt)