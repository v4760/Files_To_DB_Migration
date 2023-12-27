# Files_To_DB_Migration

## Overview

The objective of this project is to develop solutions based on the design provided. In this case, the source data was obtained in the form of files from a MySQL DB.

We require the data to be loaded into PostgreSQL, which is a common scenario in companies who want to change underlying database technologies, in which case the data from one DB needs to be migrated into another DB. The Project scope is to migrate file-based data to PostgreSQL tables

## Data Model Details

![image](https://github.com/v4760/Files_To_DB_Migration/assets/77496027/da308885-2d48-4286-9570-72c858574edf)

## Design

![image](https://github.com/v4760/Files_To_DB_Migration/assets/77496027/e2bd111d-f9e1-4d33-820d-becee051a44e)

## Setup Instructions

1. Setup the Project Using VSCode
2. Make sure you have set up a virtual environment (creating venv, requirements.txt, etc.,) and installed dependencies for the project.
3. It is essential that you deploy the application with the core logic.
4. Be sure to drop the tables and recreate them using the scripts OR simply truncate the tables with the truncate command before running the scripts
5. Run the project after setting all the environment variables.

## Validation Steps

1. You should check whether the data in the tables have been populated by running queries.
2. In postgres tables, we need to confirm that the schema structure (column name, data type, etc.) was accurately reflected from the CSV file. (Hint: Refer to schemas.json)
3. Take the count of records in the CSV files and compare it to the number of records in the PostgreSQL tables. The count should match the numbers below.
    select count(*) from orders; --68883
    select count(*) from order_items; --172198
    select count(*) from categories; --58
    select count(*) from customers; --12435
    select count(*) from departments; --6
    select count(*) from products; --1345

## Technologies Used

Programming Language – Python

Pandas – For Converting CSV to Dataframe and then load the Dataframe into Postgres Database

