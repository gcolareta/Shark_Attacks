# Shark Attacks
Final Project

## Database Integration

The ERD of the database comprises two main tables: Attacks and Hemisphere.   
The table attack will be the result of the cleanup and final merging of the two shark attacks datasets above mentioned.  The table Hemisphere will be used to do a join with the Shark table, which will make possible to incorporate the season in the analysis.   
The new table created by the join of Shark table and Hemisphere table will be exported from PG Admin as csv file for further ETL in Pandas,  where the column season will be added to the dataframe.  Season column will be one of the contributor features for the model. 
The final dataframe will be stored in the database on Postgres SQL server where a new table will be created for this purpose.  Besides other tables will be created in the database to import the results obtained from the model.
Please find below the ERD

![Database%20ERD](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Database%20ERD.png)git 