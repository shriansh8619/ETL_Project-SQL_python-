# ETL_MYSQL_Python
This project expands on Project 1 by performing ETL on two CSV files containing air pollution data from eight cities between 2017 and 2020.

#### Tools Used: MYSQL Workbench,Jupyter Notebook, Python, Pandas.

## Extract:
Loaded two CSV files from the Resources folder using pd.read_csv().

## Transform:
Removed unnecessary columns and renamed the Count column in each dataframe to Count_o3 and Count_pm25. Merged both dataframes using a left join on Date, Country, and City, creating a single dataframe with daily o3 and pm25 counts for each city.

## Load:
Created a schema with quotes for capitalized column names. In PGAdmin, set up the etl_projct2 database and created the merge_counts table. Loaded the transformed data into the database using new_df.to_sql(), then verified the upload with pd.read_sql_query(). 
