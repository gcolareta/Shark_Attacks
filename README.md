# Shark Attacks
Final Project
##Database Integration

The ERD of the database comprises two main tables: Attacks and Hemisphere.   
The table attack will be the result of the cleanup and final merging of the two shark attacks datasets above mentioned.  The table hemisphere will be used to do a join with the Shark table, which will make possible to incorporate the season in the analysis with further iterations in Pandas.   
The new table created by the join of Shark table and Hemisphere table will be exported from PG Admin for further ETL in Pandas,  where a column season will be added.  Season column will be one of the contributor features for the model. 
The final dataframe will be store be stored in the Postgres SQL server where a table will be created for this purpose.  Besides other tables will be also created in the database to import the results obtained from the model.
Please find below the ERD and the code for the initial tables creaation in the database.

![Database%20ERD](https://github.com/gcolareta/Shark_Attacks/blob/connectime4ever/Database%20ERD.png)