# BoomBike Demand
> A multivariate regression model with the goal of predicting demand for a bike share service in the US as well as identify the variables with the most impact.. 

## Table of Contents
* data_dictionary.txt - data dictionary
* day.csv - dataset
* BoomBikes_Regression_Model_Mickell_Als.ipnb - notebook

## General Information
* Multiple Linear Regression
* Libraries used - Pandas, Numpy, Matplotlib.pyplot, Seaborn, Statsmodels, Sci-kit Learn

## Conclusions
 1) Using manual and automatic feature selection (RFE), I was able to drop the number of initial features from 33 to 12 with only a minute drop in R-squared and a significant rise in the F statistic and significant drop in AIC while having all predictor p-values fall to near 0. This means the model is significantly less complex

 2) On the training set, the model scored an R-squared value of 84.7% and on our test set, this score was 82.15%. This indicates the model does a very good job of predicting demand in the dataset.

 3) The equation for the best fit line is:

𝑐𝑛𝑡=0.0614×𝑆𝑎𝑡+0.0486×𝐴𝑢𝑔𝑢𝑠𝑡+0.1183×𝑆𝑒𝑝𝑡𝑒𝑚𝑏𝑒𝑟+0.0598×𝑂𝑐𝑡𝑜𝑏𝑒𝑟−0.0918×𝑠𝑢𝑚𝑚𝑒𝑟−0.133×𝑤𝑖𝑛𝑡𝑒𝑟−0.2531×𝐿𝑖𝑔ℎ𝑡𝑃𝑟𝑒𝑐𝑖𝑝−0.0609×𝑀𝑖𝑠𝑡/𝐶𝑙𝑜𝑢𝑑𝑦+0.2309×𝑦𝑟+0.0522×𝑤𝑜𝑟𝑘𝑖𝑛𝑔𝑑𝑎𝑦+0.4715×𝑡𝑒𝑚𝑝−0.1538×ℎ𝑢𝑚−0.1875×𝑤𝑖𝑛𝑑𝑠𝑝𝑒𝑒𝑑

From the coeefficients, we can see that temperature, yr have the largest impact in increasing demand while Light_Precip and windspeed and hum act to against demand. Therefore, we can conclude that days with higher temperatures in 2019 with lower humidity, windspeed and humidity will be the days where demand is highest. If the day falls on a Saturday in Aug/Sep or Oct then demand was highest.

Assuming this holds true in post covid, we can assume that the factors which will increase demand are those days matching the aforementioned variables. Of note, is that while yr is significant within this model, it can not be used to model future demand.

- Recommendations for BoomBike
Demand increases during the late summer (Aug) and early Autumn (Sep,Oct) these are the times of year when demand will be hightest
Saturdays will have the highest demand of any day in the week BUT days when more persons are not home i.e working days will also have more demand
demand is hindered by colder temperatures therefore winter will see the lowest demand, high winds and humidity also limit demand

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