# Car-price-prediction

### Problem Statement

Customers buying a new car should be assured of the money they invest to be worthy.
It is important to know the actual market value of a car while both buying and selling, especially in case of used cars.
But how to know whether is it worthy to buy a car for a price seller says? Or How to know whether we can sell our car with a better price other than you think?
Our model helps both buyers and sellers who are losing money while trading their car.


### Business Understanding
Give a happy face to the customers by suggesting a reasonable price for both buyers and sellers involved in trading a car. The asset should be easy to access and utilize with minimal data from the customer.

### Data Understanding
Dataset has been taken from the Kaggle.com to build a ML model. We have a total of 13 attributes including the price of the car which is a dependent on all the other attributes. The length of the dataset id 6019.
The url of the dataset is https://www.kaggle.com/code/billumillu/predicting-costs-of-used-cars-machinehack/data

### Attributes in the dataset.

Name of the car
Location of the car

Year of manufacturing

Kilometers_Driven

Fuel_Type

Transmission

Owner_Type

Mileage

Engine

Power

Seats

New_Price

Price


### Grouping the cars.
![image](https://user-images.githubusercontent.com/96214945/162640613-1ca1c0bf-109a-49ad-8efc-1891e88c7e57.png)

### Data Statistics
![image](https://user-images.githubusercontent.com/96214945/162640642-cf5ca785-b8fd-4772-b529-709e83678e77.png)


### Data preparation

Make the data ready to be fit for the model and then predict the results of new values.

Convert attributes to required datatypes.

Handle null values.

Remove duplicates.

Handing Categorical variables using duplicates().

Create correlation map of the data frame object and then heatmap to get better understanding of the attributes and their importance in predicting the dependent variable.

#### Data preparation – Datatype conversion
Attributes like Mileage, Engine, Power should be of floating data type and its in string format with some letters on it. We need to remove that units and convert it into float.
![image](https://user-images.githubusercontent.com/96214945/162640696-492ae0b2-3752-4be0-b192-aba2f16645c3.png)


#### Data preparation – Handle null values
Null values creates a negative scoring for a regression while building a model.
We need to fill them with mean/median of the data from for the same column we are filling null values.
Incase of inappropriate to fill for the mean data we need to remove it.
For example, we can’t fill 5195 rows of data based on the mean of 824 rows.


#### Data preparation – Categorical Duplicating
Categorical variables should be converted into numerical form for applying the machine learning model without changing their value in predicting the dependent variables.
Duplicating is the process to make categorical variables valuable while creating a new ML model 


### Modelling
Steps to build a machine learning model
Data Splitting
Deciding on type of model that fit for our data and problem statement. (Regression/Classification/Clustering etc..)
Creating different types of models and evaluate them using the test data and decide on best model that fits for the data.
Visualizing the difference between prediction and actual values.

### Train and test split
Need to split the data into train and test dataset where train dataset is used to build a model and test dataset is used to evaluate a model.
We have used the train_test_split function of sklearn preprocessing module of python with test size as 20% of the whole data and train size as 80%.
Used the random_state as 42 to make the split of data set even every time we run the train test split function.

### Applied three machine learning models like Linear regression, KNN regression, RFR.
Used the BayesSearchCV of the skpot library of python to estimate the best sutiable hyperparameters for the models built.
