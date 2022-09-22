# Shark_Attacks

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

