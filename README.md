# ETL-project-team1


ETL Project – Technical Report: Legos
by Cesar Serrano, Kathryn Buckwalter

Background
The group wanted to explore how lego sets have changed from 1950 to 2020. 

ETL Project
Use various csv files in different formats and combine them to have one comprenhsive dataframe that can be used in SQL.


Extraction
We downloaded three different data sets in csv form. One covered the years 1950-2017 was downloaded from data.world. The data.world csv schema had many columns that needed to be narrowed down.  The 2020 data was downloaded from Kaggle in diffenet csv files that needed to be joined.

Transform
Read in three csv files to create dataframes that would be used for the cleaning process.  After the original dataframes were created we joined the sets and themes data frames so the joined dataframe matched the cleaned schema of the 1950 cleaned dataframe.   The 1950 dataframe and 2020 were joined to create a new schema that allowed both years to be in the same table. The final dataframe was read into SQL to create a table.


Potential Uses
This allows the lego themes and sets to be identified by name and theme name from 1950-2020 in one table as opposed to searching thru multiple files which require cross refrencing.


Normalization of Datasets
Each csv file started with a different schema.  We used pandas and SQL to select the columns needed from each data set.  Then the data sets were joined to combined information to allow the set and theme names to show up for each year.  Then we created a SQL table result_c.


Steps to Create
 1. Read in each csv.
        sets.csv, themes.csv, sets_1950_2017.csv
 2. Merged the set and theme csv files from 2020 on the id number.
 3. Narrowed down all files to the columns needed.
        id, set name, set year, theme name
 4. Joined the cleaned 1950 and 2020 dataframes.
 5. Used a connection string to connect the jupyter notebook to SQL
 6. Read in dataframe to SQL.
 7. Created SQL table result_c
