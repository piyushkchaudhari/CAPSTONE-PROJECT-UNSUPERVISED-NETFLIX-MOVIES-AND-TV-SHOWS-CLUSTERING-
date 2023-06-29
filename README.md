# CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-

## Problem Statement
This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flixable which is a third-party Netflix search engine.
In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.
Integrating this dataset with other external datasets such as IMDB ratings, rotten tomatoes can also provide many interesting findings.
![image](https://github.com/piyushkchaudhari/CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-/assets/123857050/06ba1af5-49a7-402e-bd75-2b9d401390d2)

## Attribute Information
1. show_id : Unique ID for every Movie / Tv Show
2. type : Identifier - A Movie or TV Show
3. title : Title of the Movie / Tv Show
4. director : Director of the Movie
5. cast : Actors involved in the movie / show
6. country : Country where the movie / show was produced
7. date_added : Date it was added on Netflix
8. release_year : Actual Releaseyear of the movie / show
9. rating : TV Rating of the movie / show
10. duration : Total Duration - in minutes or number of seasons
11. listed_in : Genere
12. description: The Summary description

## About dataset :
Only two types of types are present in this dataset namely Movies and TV Shows. This dataset has 7787 rows and 12 columns. Only one column is in numerical format.
 
## In this project
### 1. Exploratory Data Analysis
- Top actors with higest count of movies and tv shows
- Top actors with higest count of tvshows
- Top actors with higest count of Movies
- Which words frequently use in title column
- Netflix Content Analysis
- Movies and Tv Show Duration Distribution Analysis
- How does the movie runtime vary across different genres
- Which genres have the highest number of movies produced
- Which genres have the highest number of tv show produced
- Which words frequently use in Description column
- content release over the year
- content release over the year by content type
- Highest Number of Movies and Tv Show produced by Country
- Top director with higest count of movies and tvshows
- Top rating with highest count of movies and tv show
![image](https://github.com/piyushkchaudhari/CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-/assets/123857050/432350bb-e7d1-4250-addf-4ea9ba57c5ab)

### 2. Understanding what type content is available in different countries
- Number of Movies and Tv Show produced by Country
- Number of Movies produced by Country
- Number of TV Show produced by Country
- Average Movie Duration by Country
- Country wise Rating trend
- Country wise Genres trend
![image](https://github.com/piyushkchaudhari/CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-/assets/123857050/46fb3271-5fb8-4f1f-a7e8-a2dadcda4581)

### 3. Is Netflix has increasingly focusing on TV rather than movies in recent years.
![image](https://github.com/piyushkchaudhari/CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-/assets/123857050/0d8b0083-8d76-4fff-bc0e-45ce47fc42cf)

### 4. Clustering similar content by matching text-based features
I have clustered Netflix Moves and TV Shows on the basis of Genre and Description.

For clustering, first of all punctuation marks have been removed by using 'NLTK' library in text format, then by converting the format to lower case, stop words have been removed. I used porter stemming to get the base format in words.

Through TFIDF Vectorization, I created a total of 10000 attributes.

I used Principal Component Analysis (PCA) to handle the curse of dimensionality. 3000 components were able to capture more than 88% of variance, and hence, the number of components were restricted to 3000.

To find K, the silhouette scores and elbow method are used. 16 clusters have scored the highest according to silhouette scores

Clusters are created using the K-Means clustering algorithm, and the optimal number of clusters is 16.

Final cluster visualization done using plotly library.

A content based recommender system was built using the similarity matrix obtained after using cosine similarity. This recommender system will make 10 recommendations to the user based on the type of show they watched.
![image](https://github.com/piyushkchaudhari/CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-/assets/123857050/fc995ccd-add6-4ff2-814d-c6a374019028)


![image](https://github.com/piyushkchaudhari/CAPSTONE-PROJECT-UNSUPERVISED-NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING-/assets/123857050/90cc5970-4e64-454f-bec1-cb1f430e6ffa)
