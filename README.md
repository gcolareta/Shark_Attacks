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

## Machine Learning Model
We will conduct a logistic regression model. The target variable we are trying to predict is the fatality of the bite. We will explore which features are most likely to produce a fatal vs. not fatal shark attack. Such features include: Date, year, type, country , area, location, victim's activity, injury, time, and species.  There is risk associated with all ocean activities and while the risk of a shark attack is very low, it still occurs fairly frequently.  With this information we hope to shine light on which factors contribute toward the attack having a fatal outcome or not. 

Data will need to be cleaned to eliminate non-relevant variables. Text features will have to to converted into numeric data and the numeric data will need to be scaled before the models can ran. In the end, we will produce a confusion matrix and classification report to determine if the model was successful.

## Database Integration

The ERD of the database comprises two main tables: Attacks and Hemisphere.   
The table attack will be the result of the cleanup and final merging of the two shark attacks datasets above mentioned.  The table Hemisphere will be used to do a join with the Shark table, which will make possible to incorporate the season in the analysis.   
The new table created by the join of Shark table and Hemisphere table will be exported from PG Admin as csv file for further ETL in Pandas,  where the column season will be added to the dataframe.  Season column will be one of the contributor features for the model. 
The final dataframe will be stored in the database on Postgres SQL server where a new table will be created for this purpose.  Besides other tables will be created in the database to import the results obtained from the model.
Please find below the ERD

![Database%20ERD](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Database%20ERD.png)
![Join](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Join.png)


![Untitled](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Presentation/Untitled.png)

**Index of the Presentation** (Please see Presentation folder)

+ Topic and Target Audience

+ Data processing

+ Test Cases

+ Database Integration

+ Machine Learning Model

+ Recommendations