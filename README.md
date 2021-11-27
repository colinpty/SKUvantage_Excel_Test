# SKUvantage Excel Test
Convert spreadsheet into sql to query workers data for SKUvantage.

1. Find the correct SKU ID by extracting only numbers from SKU in the output table to match SKUid in the workers table and create a relational database.
```
=REGEXREPLACE(C3,"\D+", "")
```
2. Create a database in your sql server called "skuvantage_db".
```
CREATE DATABASE skuvantage_db;
```
3. Create a output table.
```
CREATE TABLE OUTPUT (
    SKU VARCHAR, 
    COLOUR VARCHAR,
    CORRECT_ID VARCHAR
);
```
4. Create a workers table.
```
CREATE TABLE WORKERS (
    SKUID VARCHAR, 
    CONTRACTOR VARCHAR,
    TIME_TAKEN NUMERIC,
    CORRECT_ID VARCHAR
);
```
5. Find the local directory with your CSV files.
```
show data_directory;
```
6. Insert the CSV files in your SQL Database.
```
COPY output FROM '/Users/colinrocha/output_correct.csv' WITH CSV HEADER; 

COPY workers FROM '/Users/colinrocha/workers_correct.csv' WITH CSV HEADER; 
```

