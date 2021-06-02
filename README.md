# House-Price-Prediction-using-Multiple-Linear-Regression

You will learn the generic steps that are required to build a multiple linear regression model. 
You will build this model for a housing dataset and predict the price of a house using the various potential predictor variables provided.
You will first read and visualise your dataset and then prepare your data for building a linear model.
This will include dealing with categorical variables, adding dummy variables, and scaling.
You will then start building the model with a bottom-up approach, i.e., you will start with one variable and keep on adding more.
Once all the variables have been added, you will perform a manual feature elimination and move on to the <b>residual analysis</b> and predictions, as usual.
In the end, you will solve the same problem using <b>RFE</b>.

<b> Reading and Understanding the Data: </b>

Linear regression is used in various fields such as real estate, telecom, e-commerce, etc. to build predictive models. Let's look at one such example from the real estate industry.
Here, you will predict the price of a house on the basis of some predictor variables, such as floor area, number of bedrooms, parking space, etc.

<b>Problem Statement:</b>
Consider that a real estate company has the data of real estate prices in Delhi.
The company wants to optimise the selling price of the properties, based on important factors such as area, bedrooms, parking, etc.

Essentially, the company wants:
<ul><li>To identify the variables affecting house prices, e.g., area, number of rooms, bathrooms, etc.</li>
<li>To create a linear model that quantitatively relates house prices with variables, such as the number of rooms, area, number of bathrooms, etc.</li>
<li>To know the accuracy of the model, i.e. how well do these variables predict the house prices</li></ul>

<b>Data Preparation:</b>
Here that you have a sense of what variables are important and that the data is well behaved with very few outliers, let’s move on to preparing the data for multiple linear regression.
This involves handling the categorical variables first and then performing dummy encoding.

<b>Initial Steps</b>
Before model building, you first need to perform the <i>test-train split and scale the features</i>.

Scaling of variables is an important step because, as you may have noticed, the variable ‘area’ is on a different scale with respect to all other numerical variables, which take very small values.
Also, the categorical variables that you encoded earlier take either 0 or 1 as their values. Hence, it is important to have everything on the same scale for the model to be easily interpretable.

You have seen the two popular rescaling methods- Min-Max scaling and Standardisation (mean=0 and sigma=1).
The advantage of Standardisation over the other is that it doesn't compress the data between a particular range as in Min-Max scaling. 
This is useful, especially if there are extreme data point (outlier).


<b>Residual Analysis and Predictions </b>
Before making the predictions, you need to be certain that the model is reliable.
To that end, you need to first perform a residual analysis of the error terms and then move on to making the predictions on the test set; and finally, evaluate the model based on the predictions.
Now that the model building is done, let’s go ahead and make inferences on the model.

Let's summarize what you have learned in this session. 

𝑝𝑟𝑖𝑐𝑒=0.236×𝑎𝑟𝑒𝑎+0.202×𝑏𝑎𝑡ℎ𝑟𝑜𝑜𝑚𝑠+0.11×𝑠𝑡𝑜𝑟𝑖𝑒𝑠+0.05×𝑚𝑎𝑖𝑛𝑟𝑜𝑎𝑑+0.04×𝑔𝑢𝑒𝑠𝑡𝑟𝑜𝑜𝑚+0.0876×ℎ𝑜𝑡𝑤𝑎𝑡𝑒𝑟ℎ𝑒𝑎𝑡𝑖𝑛𝑔+0.0682×𝑎𝑖𝑟𝑐𝑜𝑛𝑑𝑖𝑡𝑖𝑜𝑛𝑖𝑛𝑔+0.0629×𝑝𝑎𝑟𝑘𝑖𝑛𝑔+0.0637×𝑝𝑟𝑒𝑓𝑎𝑟𝑒𝑎−0.0337×𝑢𝑛𝑓𝑢𝑟𝑛𝑖𝑠ℎ𝑒𝑑+0.0428
