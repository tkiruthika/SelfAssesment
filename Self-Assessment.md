# Self-Assessment

## Contribution

In the process of creating a machine learning model for the New Delhi Weather Machine Learning Model, I chose the 'Square Role'. The below list shows my contribution to the project in different segments.
- For cleaning our dataset, helped the team member in grouping the conditions, and got involved in all the discussions for creating the database from our csv file.
- Being in the square role, I prepared the ReadMe for the first segment deliverable according to the rubric, which helped us get 100% score in our first segment of the project. In addition to that I also created the DecisionTree machine learning model for the first segment, so that our team tried two machine learning models in our first segment itself.
- The DecisionTree Model had high accuracy than the other model that was created by the other team member. As ours is a Weather data set we need high precision, for the second segment of our project I along with other team member created the RandomForestClassifier model which is like the expansion of the DecisionTree Model with multiple trees. And the RandomForest out performed the DecisionTree model.
- As our data was highly imbalanced data other team member came with the idea to do RandomOversampling  for the third segment of our project and RandomUndersampling for all the three models we created. As expeceted RandomForestClassifier with RandomOversamlpling performed little better than normal RandomForestClassifier. So, I created the excel sheet to show the results comparison of all the three models we created with Oversampling and Undersampling.
- In the dashboard creation we discussed on feature analysis and tried finding out important features of our dataset.

## Personal Challenge

One personal challenge I faced during the project was, I have to move to my new home. So was busy otherside packing and moving all household stuffs along with the project. 

# Team Assessment 

## Communication Protocol

Our team communicated through slack very frequently. And we meet in the zoom 2 or 3 times a week apart from our class hours.

## Team Strength

The team strength I believe for the sucess of our project is all our team members played a all rounder role. We didnt get stick to one particular role that we chose to do. We worked with one another in each phase. 

# New Delhi Weather Machine Learning Model

## Description of the source of data

The source of our dataset is from https://www.kaggle.com/datasets/mahirkukreja/delhi-weather-data. It is a weather dataset for the New Delhi city in India. This data was taken out from wunderground with the help of their easy to use api. It contains various features such as temperature, pressure, humidity, rain, precipitation,etc. from the year 1996 to 2017.

## Questions to answer with the data

With the given atmospheric condition such as temperature, pressure, humidity, rain, snow, etc. we are trying to predict the weather if it is haze, rain, cloudy or clear.

## Database

We created a database using SQLite which can be found in delhi.sqlite. We began with two tables split from the original database, both using the datetime column as their primary key. The two tables were then merged, written into the database file, and then we were able to connect the database into the second set of machine learning models tested.

### Preliminary feature selection

The dataset we started with contained 18 features, which we subsequently reduced to 14. Features such as snow, tornado, hail, and a wind direction column as string were determined not to contribute to the success of the machine learning model as they were too rare to provide meaningful change in outcome. Apart from this, we determined to drop all NaN values. Due to the nature of a weather dataset, we felt this would not have a significant impact on the spread of the dataset, as any given feature from any given day would not have a critical impact on the classification and would be difficult to provide an accurate value. We also narrowed down a total of 37 possible conditions to four. The four conditions now are haze, rain, cloudy, and clear. The haze category contains conditions such as sandstorm, smoke, and blowing sand. The rain category contains conditions such as drizzle, rain, and thunderstorm. The cloudy category contains conditions such as overcast and partly cloudy. The clear category remains the same and only contains the condition clear. Following the consolidation these categories and cleaning the dataset from missing values and unnecessary columns, the dataset was exported as a CSV, plugged into a SQLite database, and connected into our machine learning models.

## Machine Learning

Feature Engineering
The 'datetime-utc' column was converted to two separate columns 'year' and 'month' so that we were dealing strictly with numeric values. We also dropped the 'wdire' column because it was a duplicate column where wind directions were labeled as string values. This left us with a total of 16 features including the target variable.

### Data splitting

We separated our target value, 'conds', from our features and imported sklearns 'train_test_split' library to split our training and test sets.

### Models Results/Comparison

We used Logistic Regression, Decision Tree, and Random Forest classifiers and added over and undersampling techniques to these models and compared the performance of the models

### Models_Classification

![Models_Classification](https://user-images.githubusercontent.com/95719819/172752000-da15e71a-c0fd-4ff4-802b-e5f2f94c01a4.png)

### Model Choice

Our final model choice is the Random Forest classifier with Oversampling techniques applied. Benefits to using a Random Forest classifier are that the model is robust against overfitting as well as it runs efficiently on large datasets such as ours. Some cons to this model specifically is that it has a low balanced accuracy score but high recall and precision scores which show not very many false negatives and false positives.

### Confusion Matrix & Classification Report

![confusion class](https://user-images.githubusercontent.com/95719819/172752054-981dd02d-9895-4dac-885c-292f600c6269.png)

