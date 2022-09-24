# Shark Attacks

## Topic and Reason for Selection
There is risk associated with all ocean activities and while the risk of a shark attack is very low, it still occurs fairly frequently.  With this information we hope to increase our customer base by shining a light on which factors contribute toward the attack having a fatal outcome or not. 

## Sources of Data
#### Sources of Data
- Global Shark Attack File (GSAF): https://www.sharks.org/global-shark-attack-file (link to file: https://docs.google.com/spreadsheets/d/1rH3O8JQ1v6tt7swPNbE5B5-AtVr9OtjhhmwpEuBQFbc/edit?usp=sharing)
- attacks.csv: https://www.kaggle.com/datasets/felipeesc/shark-attack-dataset?resource=download

#### Factors to Consider
- Fatality: Dependent variable
- Type: unprovoked only
- Activities: surfing, swimming, snorkeling/scuba diving, fishing
- Locations: area, country

## Questions
What is the probability of a shark attack based on location?
Contributing factors that can cause a fatal shark attack

## Communication Protocols
Slack: to coordinate zoom meetings and ongoing communication
Zoom: 
  - Sunday morning, 9:00 AM
  - Monday, Wednesday
  - Tuesday (TBD)

## Machine Learning Model
Using a logistic regression model, we will explore which features are most likely to produce a target variable of a fatal shark attack or not fatal attack. Such features include: Date, year, type, country , area, location, activity, name, sex, age, injury, time, and species.  There is risk associated with all ocean activities and while the risk of a shark attack is very low, it still occurs fairly frequently.  With this information we hope to shine light on which factors contribute toward the attack having a fatal outcome or not. 

Data will need to be cleaned to eliminate non-useful columns, and data. Text features will have to to converted into numeric data and the numeric data will need to be scaled before the models can ran. In the end, we will produce a confusion matrix and classification report to determine if the model was successful.

## Database Integration

The ERD of the database comprises two main tables: Attacks and Hemisphere.   
The table attack will be the result of the cleanup and final merging of the two shark attacks datasets above mentioned.  The table Hemisphere will be used to do a join with the Shark table, which will make possible to incorporate the season in the analysis.   
The new table created by the join of Shark table and Hemisphere table will be exported from PG Admin as csv file for further ETL in Pandas,  where the column season will be added to the dataframe.  Season column will be one of the contributor features for the model. 
The final dataframe will be stored in the database on Postgres SQL server where a new table will be created for this purpose.  Besides other tables will be created in the database to import the results obtained from the model.
Please find below the ERD

![Database%20ERD](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Database%20ERD.png)