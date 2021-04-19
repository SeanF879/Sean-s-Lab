

The country chosen for this project was Kenya. For the project I initially downloaded many different geospatial data types, ranging from the topography to night time light.  

Two models, a linear regression model and a random forest model, were run to predict population distribution in Zambia. The predicted values were compared to known population data through mapping, mean square error calculation, and plotting of statistics (mean square error, absolute square error, and root mean square error).

Goals of this project: Use two machine learning methods predict population values at 100 x 100 meter resolution throughout your selected country. Validate the two models using different methods presented in this class. Write a report assessing the two approaches and which of the two models was more accurate. Be sure to account for spatial variation throughout your selected location and provide substantive explanations for why those variations occurred.


Model 1:  Linear Regression

The first model used for this project was an OLS Regression.  These are always a useful tool in any data scientists tooltik when trying to use variables to predict something.  But first, I needed to preprocess the data for the model, which was done by creatng a test and training data split from all the available data.  The model's prediction for the total population of Kenya was a little bit off, predicting it to have a total summed population of about 55.2 million.  However, compared to Kenya's actual population of a little over 55.1 million people, this seemed to be a rather good prediction.  The only other question was how accurate was it at predicting population in the individual admministrative regions.

The below R output shows the absolute error for predicted versus actual populations in each administrative region.  

<img width="400" alt="Kenya_1" src="https://user-images.githubusercontent.com/78227412/115165747-67eeee00-a07d-11eb-92b9-0412b4a7dafa.png">

The output confirms that the model was slightly overpridting populations, seemingly mostly in Southeastern Kenya, which has many urban/costal regions, so perhaps the model struggled with these types of special urban environments.


Model 2:  Random Forest
The preprocessing of the data used for the second model, the Random Forest, was very similiar to the Linear Regression's with a training/test data splitting.  The model's prediction for the total population however was better than the Linear Regression's being almost 10,000 people closer to the true value.  

Below is the R output for the node purity

![Kenya_3](https://user-images.githubusercontent.com/78227412/115166129-7938fa00-a07f-11eb-9317-ebc04fe12cf6.png)

Below is the R output for mean absolute error for the Random Forest model

<img width="400" alt="Kenya_2" src="https://user-images.githubusercontent.com/78227412/115165749-69201b00-a07d-11eb-810b-31d53e5e3fb8.png">


Conclusion:
Both models were surprisngly good at preidcting the aggregate populations, with the Random Forest doing a little better, but both struggled with the asmaller scale predictions at the administrative region level.  However, the error was lower with the Random Forest model so that is the winner.  Most likely the spatial variations caused by desnley populated urban/costal regions threw off the model, because some areas contain things such as apartment living, tall buildings, etc... that all allow for desner populations than would be expected by the model especially because those things that allow for very densly populated regions don't exist in the majority fo the country.

