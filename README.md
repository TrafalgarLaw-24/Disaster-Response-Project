# Disaster Response Pipeline Project
Performing ETL to read the dataset, clean the data, and store it in a database and then using the stored data to build a Machine Learning model with Natural Language Processing to predict classification of 36 categories (multi-output classification).

## Getting Started
Clone the repository and install the necessary packages mentioned in the 'requirements.txt' file.

## Content
* Data
	* process_data.py: reads the dataset, cleans it and stores it in a SQL database.
	* disaster_categories.csv and disaster_messages.csv (datasets)
	* DisasterResponse.db: created database and table from the data that was processed.
* Models
	* train_classifier.py: includes the code necessary to load data, transform it using natural language processing, run a machine learning model using GridSearchCV and train it.
* App
	* run.py: Flask app and the user interface used to display the result. An interactive web app.
	* templates: folder containing the html templates

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    1. The first command is to run the ETL pipeline that cleans data and stores in database.
	2. The second is to run the ML pipeline that trains classifier and saves the result in pickle file.

```
python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
```
```
python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
```

2. Run the following command in the app's directory to run your web app.

```    
python run.py
```

3. Go to http://0.0.0.0:3001/

## Screenshots
WebApp's Landing Page
![Alt text](https://github.com/TrafalgarLaw-24/Disaster-Response-Project/blob/master/Webapp_screenshot1.png "Screenshot1")
![Alt text](https://github.com/TrafalgarLaw-24/Disaster-Response-Project/blob/master/Webapp_screenshot2.png "Screenshot2")
![Alt text](https://github.com/TrafalgarLaw-24/Disaster-Response-Project/blob/master/Webapp_screenshot3.png "Screenshot3")
![Alt text](https://github.com/TrafalgarLaw-24/Disaster-Response-Project/blob/master/Webapp_screenshot4.png "Screenshot4")

Enter a word in the text box and you can see the results
![Alt text](https://github.com/TrafalgarLaw-24/Disaster-Response-Project/blob/master/Webapp_screenshot5.png "Screenshot5")

## About

* Created this project as part of the Udacity Data Scientist Nanodegree programme. The data was provided by Figure Eight.
