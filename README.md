# Movies (Extract, Transform, Load)

## Purpose
### Overview
#### Amazing Prime is a platform for streaming movies and TV online. The Amazing Prime video team loves the dataset and wants to keep it updated on a daily basis. In order to do this, we created an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables, 

### Process
#### To prepare for the Hackathon event, we followed the Extract, Transform, and Load process to extract the Wikipedia and Kaggle data from their respective files, transform the dataets by cleanng them up and joining them together, and loading the cleaned dataset into an SQL database called "Movies."
#### Wikipedia has a ton of information about movies, including budgets and box office returns, cast and crew, production and distribution, and more. After loading the Wikipedia scrape, we found a dataset on Kaggle that contains ratings data from MovieLens. After we completed the data extraction we transformed the data to filter to only movies, created a function called clean_movie, removed duplicate rows and null columns, and parsed the data for usage.
#### Next, we cleaned the Kaggle data by removing "bad data" and changing the data types. After the Wikipedia data and Kaggle data were both cleaned up and in tabular formats with the right data types for each column, we joined the datasets together.
#### Lastly, we connected Pandas to our PostgreSQL database and loaded our transformed data set to a databse using the to_sql() method.  

### Checking Our Database
#### To ensure that our data was properly loaded into the SQL database, we ran two queries -- 1) on the movies table and 2) on the ratings table.
<img width="464" alt="movies_query" src="https://user-images.githubusercontent.com/94096530/155758250-2b38ef09-00c1-454d-9af7-a337cd53042b.png">
<img width="462" alt="ratings_query" src="https://user-images.githubusercontent.com/94096530/155758256-189cfe8d-245f-4a16-9e64-2b8f948843bb.png">

#### We can see that the COUNT returned the correct amount of entries per table, this our data was sucessfully loaded to our database.
