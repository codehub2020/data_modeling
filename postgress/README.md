# Project 

ETL design and data modeling with postgres

### Description

The project design consist of designing a database schema and ETL pipeline for a music streaming services. The choice of dimensions and fact tables will help the streaming service understand what type of songs subscribers are listening to. 

The company data resides in directories of json logs of user activities and json metadata on songs. The ETL pipeline is designed to transfer data from the json directories to the tables using python scripts and SQL

The database should will be able to provide the company reportings like - 
- the number of active subscribers and the top songs they are listening to
- top rated artists and songs
- stream traffic that describes what time the subscribers use the service the most




## Database Schema

### Fact Table 
songplay - holds information associated with song plays

### Dimensions

users - holds subscriber information
songs - holds songs information
artist - holds artists information
time - holds information associated with song play activity

The table design and data types can be found in sql_queries.py


## Deployment Scripts

The projects consist of several python and sql scrpits 

sql_queries.py - contains the sql queries that creates and load the tables. This script is imported in the etl scripts
create_tables.py - drops and creates tables. Used to reset tables each time the etl process is run
etl.ipynb - design template for the etl process, it reads and process the json files into the tables
etl.py - reads and process the json files into the tables based off the design in etl.ipynb
test.ipynb - run this script to validate the data in the database