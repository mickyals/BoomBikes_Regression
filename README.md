# BoomBike Demand
> A multivariate regression model with the goal of predicting demand for a bike share service in the US as well as identify the variables with the most impact.. 

## Table of Contents
* data_dictionary.txt - data dictionary
* day.csv - dataset
* BoomBikes_Regression_Model_Mickell_Als.ipnb - notebook
* Model_Results.md - numerical summary of results

## General Information
* Multiple Linear Regression
* Libraries used - Pandas, Numpy, Matplotlib.pyplot, Seaborn, Statsmodels, Scikit-Learn, SciPy

## Conclusions
 1) Using manual and automatic feature selection (RFE), I was able to drop the number of initial features from 33 to 12 with only a minute drop in R-squared and a significant rise in the F statistic and significant drop in AIC while having all predictor p-values fall to near 0. This means the model is significantly less complex

2) On the training set, the model scored an R-squared value of 84.4% and on our test set, this score was 82.4%. This indicates the model does a very good job of predicting demand in the dataset.
 

3) The equation for the best fit line is:

 $ cnt = 0.3191 + 0.0633	\times Sat + 0.1003 \times	September + 0.0590	\times October - 0.0695 \times summer - 0.1340 \times winter - 0.2569 \times LightPrecip - 0.0599 \times Mist/Cloudy + 0.2319 \times yr + 0.0534 \times workingday + 0.4681	\times temp - 0.1457 \times hum - 0.1873 \times windspeed $
 
Based on the absolute values of the coeffients the following are the features with the most impact and their effect

|Position|Feature      | Coef   | Impact  |
|--------|-------------|--------|---------|
|   1    | temp        | 0.4681 | Increase|
|   2    | Light_Precip| -0.2569| Decrease|
|   3    | yr          |  0.2319| Increase|
|   4    | windspeed   | -0.1873| Decrease|
|   5    | hum         | -0.1457| Decrease|
|   6    | winter      | -0.134 | Decrease|
|   7    | September   | 0.1003 | Increase|
|   8    | summer      | -0.0695| Decrease|
|   9    | Sat         | 0.0633 | Increase|
|   10   | Mist/Cloudy | -0.0599| Decrease|
|   11   | October     | 0.059  | Increase|
|   12   | workingday  | 0.0534 | Increase|

 
#### Recommendations for BoomBike

Based on the available data, we can see that having a higher temperatures increases demand more so than all other features while Light_Precipe decreases more so than other features. That being said, the yr variable clearly indicates that 2019 was linked to higher demand for services. 

- We can expect higher demand in summer due to its higher temperatures. It is  likely the summer variable itself is linked to a decrease in usage not due to temperature but due to summer having a higher chance of light to heavy shower. In addition to this, we can also expect demand to be higher on days when persons are working and Saturdays likely due to persons taking the bike to work and using the bike for trips on Saturdays. 

For example warm Saturdays in September with clear skies, low humidity and calm winds in 2019 would have the highest demand for bikes

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