# ETL-Project

The purpose of the ETL project was to clean and prepare data using ETL methodologies learned within the course.  I wanted to understand how the cost of living and GDP related from country to country.  I sourced country master data and country cost of living data from Kaggle. I cleaned and prepared the data using the Pandas library within Jupitar Notebook before pushing it to my Postgres Database via SQLAlchemy. Below was the process:

Extract/Data Utilized<br>
The data was received from a couple of different sources on Kaggle in the form of CSV files(https://www.kaggle.com/andradaolteanu/2020-cost-of-living & https://www.kaggle.com/fernandol/countries-of-the-world). The Cost of Living data source had a lot of indices by Country on where each country fell within the Cost of Living categories.  The Countries of the World data source had master data for each country along with the GDP. At the end of the day, I needed to merge these sources to understand the correlations.

Transformation<br>
Once the 2 data files were extracted, the data was transformed using Python and Jupyter Notebooks.  Some unnecessary columns were removed and I produced a final 'Clean' data frame for each source.  These two data frames would be what fed my Postgres Database.  

Load<br>
Using SQLAlchemy, I created a connection from my Jupitar notebook to my Postgres database.  After opening the connection string, I pushed both of my clean data frames to Postgres, in my local machine.  

Outliers<br>
I spent the rest of the time working within PGAdmin to do some further analysis.  I was able to query both tables via an Inner Join to remove countries that did not exist in both data sets.  Now I had a consolidated view to review the GDP vs Cost of Living indexes.

Next Steps<br>
The next step in the process would be to create visualizations with this data to understand the correlation between a country's GDP and Cost of Living.  Also, pulling in some additional variables could be helpful in a regression analysis. 
