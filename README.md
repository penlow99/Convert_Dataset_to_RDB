# Convert_Dataset_to_RDB

The purpose of this project is to convert an existing dataset (from a single spreadsheet) into a relational database to demonstrate RDB design. The data used for this endeavour was Metro Nashville Police Department calls for service records. Hopefully, the resulting database can be used in future demo projects.

## Outline of project
1. Acquire dataset from Nashville Open Data Portal (https://data.nashville.gov/)
2. EDA with Pandas notebook
3. ERD design
4. Write CREATE statements for postgreSQL db
5. Write script to import data from CSV

## 1. Acquire dataset
The dataset was retrieved manually from the Metro Nashville goverment website, specifically the Nashville Open Data Portal (located at https://data.nashville.gov/). Once at the website, navigate to the Public Safety section, then locate the Metro Nashville Police Department Calls for Service dataset. You can preview the data, or download it in a variety of formats. For the purpose of this excercise, CSV format was the option chosen.

## 2. EDA with Pandas notebook
Upon loading the CSV data into a Pandas dataframe, several things stood out:
* the dataset contained over **7.3 million rows**
* there were many null values for almost all columns except for 'Event Number', 'Call Received', 'Tencode', and 'Shift'
* neither 'Event Number' or 'Call Received' will work (as is) as a primary key, as they have duplicate rows (but they appear to be data for the same call for service)



