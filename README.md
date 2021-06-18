# Movies-ETL

## Deliverable 1: Creating DataFrames (Extract)
- This is a crucial first step to being able to really do much with the data. ETL_function_test.ipynb holds Deliverable 1, and converts the kaggle csv and ratings csv to Pandas DataFrames, as well as the Wikipedia json into a DataFrame.

## Deliverable 2: Cleaning Wiki Data (Transform)
- In this stage, the extracted wikipedia data is pared-down into meaningful, data-dense columns, and some are converted from several inconsistent forms into the necessary types for analysis with consistent formatting. The columns that have been adjusted are as follows:
  -   Budget
  -   Box Office
  -   Running Time
  -   Release Date
-   See ETL_clean_wiki_movies.ipynb for full notebook.

## Deliverable 3: Cleaning Kaggle and Ratings Data (Transform)
- The data from Kaggle is cleaned similarly to the wikipedia data and merged on the imdb_id column. Once the DataFrames are merged, unnecessary columns are dropped. The dropped columns after merging are the following:
  - title_wiki
  - release_date_wiki
  - Language
  - Production company(s)
- Generally the wiki data was not as complete as the Kaggle data. As a result, the wiki columns were either just dropped, or were used to fill in some missing Kaggle data before being dropped. The following columns had Kaggle data supplemented with wikipedia information where missing:
  - Runtime
  - Budget
  - Revenue
- Once the merged DataFrame was created, the ratings were also grouped to show all the ratings for each movie.
