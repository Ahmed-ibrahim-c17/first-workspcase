# first-workspcase
Project- investigate-a-dataset
Udacity data analyst nanodegree - project  investigate a dataset

In this project, I will analyze a dataset and then communicate my findings about it. I will use the Python libraries NumPy, pandas, and Matplotlib to make my analysis easier.

The libraries that I needed to install :

pandas
NumPy
Matplotlib
csv
In this project I will apply all the concepts That I've learnt including:

1- Know all the steps involved in a typical data analysis process. 2- Be comfortable posing questions that can be answered with a given dataset and then answering those questions. 3- Know how to investigate problems in a dataset and wrangle the data into a format I can use. 4- Have experience communicating the results of my analysis. 5- Be able to use vectorized operations in NumPy and pandas to speed up my data analysis code. 6- Be familiar with pandas' Series and DataFrame objects, which let me access my data more conveniently. 7- Know how to use Matplotlib to produce plots showing my findings.

Step 1 - Choosing data set
I chose TMDB movie data which contains information about 10,000 movies collected from The Movie Database (TMDb), including user ratings and revenue.

Certain columns, like ‘cast’ and ‘genres’, contain multiple values separated by pipe (|) characters. The final two columns ending with “_adj” show the budget and revenue of the associated movie in terms of 2010 dollars, accounting for inflation over time.

Step Two - Get Organized

The report communicating your findings Any Python code I wrote as part of your analysis The data set I used. I'll use a Jupyter notebook, that I can submit both the code I wrote and the report of my findings in the same document.

Step Three - Analyze my Data
Questions to answer: 1- Which genres are most popular from year to year?

2- What kinds of properties are associated with movies that have high revenues?

SAMPLES OF CODE:
first i have to load data and print out a few lines . perform operations to inspect data types and look for instances of missing or possibly errant data
code:
df=pd.read_csv('tmdb-movies.csv')
df.head(1)
after that 
df.info() # to see information of dataset
now i have to visualizing the data to get a better inderstanding of its distrbuions
code: 
df.hist(figsize=(20,16))
now i can answer the first questiong 
code:
plt.subplots(figesize(20,6))
plt.bar(genres_popularity.index, genres_popularity)
plt.title('popularity by genre')
plt.xlabel('genre')
plt.ylabel('popylarity');

so now we can see the most popular genre.
---
continue to explore the data to address your additional reserch 
questions add more headrs as needed if you have more questions to investigate
sort movies by revenue in descending order
code:
sorted_revenue_biggest=df.sort_values(by=['revenue'], ascending = False).head(200)
sorted_revenue_bigges.head(1)
 and see the histogram
code:
sorted_revenue_biggest.popularity.hist()
sorted_revenue_biggest.runtime.hist()
--
and they last : are short movies more popular
to see that :
code:
shorter_movies = df.sort_values(by=['runtime'], ascending = False).head(200)
runtime = shorter_movies['runtime']
popularity = shorter_movies['popularity']
plt.scatter(runtime, popularity)
plt.show()
so we can see that the more popular movies.
