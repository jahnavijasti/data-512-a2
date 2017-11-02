# Bias in Wikipedia Data

The purpose of the project is to explore the concept of bias in Wikipedia articles on politicians from different countries.


## Data
There are two datasets used in this project. 

Wikipedia dataset: This dataset contains data from English Wikipedia. The articles concentrate on politicians from various countries. The data was extracted from wikipedia API and saved as a csv file (which is downloaded directly from https://figshare.com/articles/Untitled_Item/5513449) 

Columns in Wikipedia dataset:
Country - names of different countries from which the articles are extracted
Page - contains the page title
last_edit - contains the id of the last edit of that particular page


Population dataset: This dataset contains the population data of various countries (downloaded from http://www.prb.org/DataFinder/Topic/Rankings.aspx?ind=14)


## Getting article quality predictions
For predicting the quality scores of each of the article in Wikipedia data, Wikipedia API endpoint called ORES is used. It estimates the quality of an article and assigns a prediction for them. The prediction can be one of the following six groups:

FA - Featured article

GA - Good article

B - B-class article

C - C-class article

Start - Start-class article

Stub - Stub-class article



