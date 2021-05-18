Problem Statement that introduces your selected topic, identifies significant goals associated with the implementation of your applied machine learning method, demonstrates why your problem is important, and describes and analyzes the complex nature of your problem including any process oriented causes and effects. Conclude your problem statement with a stated central research question. You are welcome to articulate a central research question in broad and general terms, given the abbreviated time frame for this investigation.


A description of the data that you are using as input for your applied machine learning methodology, including the source of the data, the different features (variables) and well as their data class (i.e. continuous or discrete). Be sure to include a description of your dataset size (number of rows / observations as well as number of columns / variables / features) and provide context on how the data was collected as well as the source organization, as it is relevant to your investigation.


Provide the specification for your applied machine learning method that presented the most promise in providing a solution to your problem. Include the section from your python or R script that specifies your model architecture, layers, functional arguments and specifications for compiling and fitting. Provide a brief description of how you implemented your code in practice.


Conclude with a section that preliminarily assesses model performance. If you have results from your implementation, you are welcome to add those in this section. Compare your preliminary results with those from the literature on your topic for a comparative assessment. If you are not able to produce preliminary results, provide a cursory literature review that includes 2 sources that present and describes their validation. With more time and project support, estimate what an ideal outcome looks like in terms of model validation.


Below is my written responses to the above prompts:

Problem Statement:  An important factor when making any decision is risk. Risk is simply uncertainity in important outcomes that can potentially negatively effect you and others in the world. Therefore, managing and minimizing risk is generally seen to be a good thing, and one popular place where risk and risk management occurs is the stock market. When people have money that they dont need right now and other people want that money, they tend to turn to the stock market. Now, the combination of both risk and investing comes in the form of potentially predicting future values of stocks. From pseudo-science/statistics to guesswork to using every metric knwon to humanity, predicing future stock prices has been a commonly attempted project. I believe that for relatively lower risk financial instruments such as certain stocks that machine learning methods can be used to help predict future price movements.  While I doubt my model will be good at testing stocks with high volatility such as Tesla I believe that stocks such as Home Depot with a lower standard deviation the model will preform well.  My future job wil be dealing with economic statitics in relation to financial isntruments and so I thought it would eb a fun excersize to use a K-Nearest Neighbors to predict stock price movements as during my previous internship last summer I learned how to do a basic form of a KNN model that I would like to replicate.  

Data:  The data that I will be using is a Kaggle dataset of downloaded and compiled stock prices over the past decade.  For the pruposes of this project I will be testing Home Depot's stock price from 2014 to 2017 using an excel datasheet.  The variables including are as follows:  Date	Open	High	Low	Close	Volume	Dividend	Split	Adj_Open	Adj_High	Adj_Low	Adj_Close	Adj_Volume.  There are 1093 rows of data and the data is reputable as it can be easily cross referenced with actual publicly avialable historical stock price data.  

Model Specification:

