ETL Project Report
Bic Vu

EXTRACT
Data was pulled from three separate sources, Kaggle, US Census Bureau and USDA. The Obesity CSV was shared with other team members while the Census data and USDA data on school lunch programs was pulled specific to my part of the analysis. The data was available in multiple formats and were normalized as three separate CSV files.

TRANSFORMATION
A lengthy process of cleaning, checking and formatting was required to transform the three files into data that could cross-reference each other.
Utilizing Jupyter Notebook and panda libraries, the rows and columns had to be filtered for matching information. 

Starting with the Obesity data which was a survey spreadsheet, relevant questions and their ID needed to be identified and used as a filter. There was far more data than necessary for this study, so only relevant columns of information where kept. Upon cross referencing the data, I noticed that only three years (2013, 2015, and 2017) had corresponding data. The year was used as a groupby mechanism for smaller datasets that can be easily compared. The state was identified as the primary key for all three data chart and needed to be sorted alphabetically. 

The Census and School Lunches data were similarly filtered for states and quantity. The quantity of lunches were compared with state population for a very rough estimate of percentages of population in each state that received school lunches. The percentages were rounded to a corresponding decimal value as those in the Obesity Data.

LOAD
A final Comparison analysis merged all three datasets was saved onto a database using Postgres and also exported as a final CSV file.

CONCLUSION
The challenge of this project was constantly checking if I was working with apples or oranges. Values that appears as numbers may turn out to be strings, integers as floats, and NaN were always somewhere in the nether. Multiple debugging measures where added to the scripts to see if filtering mechanisms affected value formats.


