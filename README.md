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

To get the prediction of each article, the coreesponding revision_id from the Wikipedia dataset is called into ORES APi and it gives the prediction.

The prediction is saved as a new column in the Wikipedia dataset.

## Combining datasets

The Wikipedia and Population datasets are combined using an inner join, i.e, the rows that do not have matching data are removed.

A final single csv file is saved and contains the following columns:

country - name of the country

article_name - page title of the article

revision_id - id of the last edit

article_quality - predicted quality of the article

population - population in that particular country

## Analysis

From the final dataset, four tables are produced.

1. 10 highest-ranked countries in terms of number of politician articles as a proportion of country population

2. 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population

3. 10 highest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country

4. 10 lowest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country

## Reflections

It is quite surprising to see that no developed country is in the top 10 countries that has highest number of political articles as a proportion of country population. This may be because most of the countries in top 10 are very less populated. However, countries like Iceland and Tonga has made into the top list even with quite a big number of population.

It is logical to see that major countries like India and China are have the least percentage proportion of political articles to country population, as they are the highly populated countries in the world.

Eventhough countries like North Korea, Saudi Arabia are non-English speaking country, they stood top in the race of having highest percentage of good quality articles, while countries like Peru and Finland were in the bottom 10 of the list.


