# Shark Attacks

## Topic and Reason for Selection
There is risk associated with all ocean activities and while the risk of a shark attack is very low, it still occurs fairly frequently.  With this information we hope to increase our customer awareness of the reasons associated with unprovoked shark bites, determine which factors contribute toward the attack having a fatal outcome and educate swimmers on ways to reduce their risk of being bitten by a shark. 

An unprovoked shark attack is defined as a shark bite that occurs in the natural environment of the animal and was not caused by a provocation from the human.

## Sources of Data
#### Sources of Data
- Global Shark Attack File (GSAF): https://www.sharks.org/global-shark-attack-file (link to file: https://docs.google.com/spreadsheets/d/1rH3O8JQ1v6tt7swPNbE5B5-AtVr9OtjhhmwpEuBQFbc/edit?usp=sharing)
- attacks.csv: https://www.kaggle.com/datasets/felipeesc/shark-attack-dataset?resource=download

#### Factors to Consider
- Fatality of the attack
- Type of attack: for the purpose of this research we will focus on unprovoked attacks only.
- Victim Activity during attack
- Locations where the attack occur: area and country
Identifying severity is difficult as the coding used is not uniform and detailed enough to verify severity of the incident. 
Identify if certain activities increase the probability of a fatal encounter. (We could also drive down for each activity to see which one, takes you near larger sharks.)

- Fatality: (Y) Dependent variable
- Type: unprovoked 
- Activities: surfing, swimming, snorkeling/scuba diving, fishing
- Locations: area, country

Identify if size of the shark increases the probability of a fatal encounter. (We could look at the type as well, we would need to extract it.)

* Fatality: (Y) Dependent variable
* Type: unprovoked 
* Species: Extract size. 
* Locations: area, country

Identify if seasons increases the probability of a fatal encounter. (We could do the same with a weather model and look at different temperatures)

* Fatality: (Y) Dependent variable
* Type: unprovoked 
* Date: Compare the time of year to identify which season it is. We could also find or create a dataset that will do this automatically by joining them both. 
* Locations: area, country

Identify if an increase in tourism increases the probability of a fatal encounter. 

* Fatality: (Y) Dependent variable
* Type: unprovoked 
* Date: Compare the time of year to identify which season it is. We could also find or create a dataset that will do this automatically by joining them both. 
* Locations: area, country

Identify if certain activities increase the probability of having an encounter.

* Fatality: (Y & N) Dependent variable
* Type: unprovoked 
* Activities: surfing, swimming, snorkeling/scuba diving, fishing
* Locations: area, country

## Questions
What is the probability of a shark attack based on location?
Which factors contribute to a fatal vs non-fatal shark attack?

## Communication Protocols
1. Slack: used for ongoing communication and to coordinate zoom meetings.
2. Zoom: 
  - Sunday morning, 9:00 AM
  - Monday, Wednesday (during class time)
  - Tuesday (TBD)

### Technology
- Git Hub 
- Excel
- Pandas and Jupyter notebook
- Postgress SQL
- Supervised Machine Learning Models
- Google collab
- Google slides
- Slack
- Tableau
- Zoom

### Data preprocessing

Data was cleaned to eliminate irrelevant variables. Text features were converted into numeric data and the encoded values were scaled before storing the data in the database and to be used by the model.

In the process we came accross of several challenges due to the quality of the data.  Bins were created to group the activities in which victims were involved at the moment of the attack. Besides, the month was extracted from the case number, rather than the date column, due to the inconsistencies of the data types in that column.

Null values in the activities, age and sex columns were replaced by other, 0, and unknown, respectively. 


## Database Integration

The ERD of the database was created comprising two main tables: Unprovoked and Hemisphere.
Hemisphere table was created to do a join with Unprovoked table,  which made possible to incorporate the season in the analysis.    

The newly created table "df" was uploaded in Jupyter Notebook from PG Admin as a csv file  by using an engine for the integration of the database with the model and for the creation of the season column in Pandas.  Season column was added as one of the contributor features for the model. 

The final dataframe with the season incorporated was stored in the database on Postgres SQL server where a new table was created for this purpose.  Besides, the table "Model_results" was  created in the database to store the results obtained from the model.
![m2](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/m2.png)

![Database%20ERD](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Database%20ERD.png)
![Join](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Join.png)


## Machine Learning Model
We  conducted a logistic regression model. The target variable we were trying to predict is the fatality of the bite. We  explored which features are more likely to produce a fatal vs. not fatal shark attack. Such features include:  year, type, country , area and  victim's activity  

There is risk associated with all ocean activities and while the risk of a shark attack is very low, it still occurs fairly frequently.  With this information we hope to shine light on which factors contribute toward the attack having a fatal outcome or not. 

Although date, location, injuries were considered as features at the begining of the project, on the road they were taken off the model due to inconsistency and low quatility of the raw data which made the preprocessing extremely challenging.

Additional features added: hemisphere, month and season trying build a more robust dataset for the model.

A confusion matrix and classification report were created to determine if the model was successful.

![model](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/model.png)


### Presentation

**Index of the Presentation** (Please see Presentation folder)

+ Topic and Target Audience

+ Data processing

+ Test Cases

+ Database Integration

+ Machine Learning Model

+ Recommendations


![Tableaumap](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Tableaumap.png)

***Model Results***

![m1](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/m1.png)
![m2](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/m2.png)
![m3](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/m3.png)


***Summary***
+ The features chosen are inconclusive when trying to predict whether the shark attacks are fatal or not. 
+ There is an imbalance in the occurrances of fatal and non fatal attacks so this fact makes difficult for the model to predict the likehood of fatalities.
+ For future projects it is recommended to follow other approaches that might serve better the customer expectations regarding safety analysis. 
+ For example other variables could be added are:
  - beach attendance, to predict the probabilty of shark attacks by area/location,
  - severity of attacks, 
  - migration patterns 
  - climate change factor (sea temperature, food chain...)
  - type of attendees (visitors, locals)
+ In this case an unsupervised machine learning model will be used to identify the labels for the predictive model to be used. 
+ Another recommendation is to compare shark attacks to other life threatening events.