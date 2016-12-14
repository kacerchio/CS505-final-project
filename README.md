# CS505-final-project
### *by Kristel Tan and Nisa Gurung*

The main goal of this project was to identify trends in movie attributes that correlate with a movie’s success in respect to the genre that it belongs in. Movie attributes analyzed include the duration of a movie, its allocated budget, average actor similarity, title length, director hits, and plot keywords. For the purposes of this project, we defined a film’s success by how much gross profit it made in the box office, independent of critic reviews and ratings. By analyzing this data, we expect to be able to make recommendations for such movie attributes and predictions of whether or not a given set of attributes will result in a highly profitable movie launch. 

#Datasets 

The dataset to support this project was initially retrieved from ‘kaggle.com’. It was a CSV file of 5,000 movie attributes scraped from IMDB and ‘the-numbers.com’. We cleaned this dataset of entries that were missing relevant attributes. Because this step eliminated a significant amount of data, we manually scraped and cleaned more data from IMDB’s top box office lists for the past 12 years. We then merged this data back with the original dataset, totaling roughly 6,000 that had all of the attributes we were looking to analyze. We removed movies that were missing column entries because we wanted to ensure that every movie could contribute to every analysis equally. 

#Techniques 

For this project, we planned to use two different techniques to help identify movie attributes related to its success. These methods include multiple linear regression and k-means clustering. Multiple linear regression was a natural choice because it gives us an idea of whether or not certain independent variables are significant to any given genre and how strongly they correlate with its gross profit. In particular, we looked at the duration, title length, budget, number of hits the director has produced, and average actor similarity in relation to the gross profit it made. Applying an OLS linear regression function to this data provided us with coefficients and confidence intervals to identify correlations. 

Furthermore, we used k-means clustering to analyze a different kind of attribute, which were plot keywords. We chose to focus on evaluating a movie’s plot keywords for the top 
1,000 profitable movies and least 1,000 profitable movies of our overall dataset. In other words, we clustered these movies by the most similar plot keywords that are associated with them, provided from IMDB’s website. Clusters formed based upon words of similar themes and meaning. Individuals points stayed closer to the center of the cluster or strayed away from it depending upon how similar it was to the other plot keywords in that cluster. At a high level, this gave us an idea of what plot keywords formed the largest clusters, which also indicated what storylines movie critics and audiences found most interesting.

#Scripts 
The scripts for this project are data-collection.ipynb which is in the data folder and Regression.ipynb and Kmeans.ipynb. 

We retrieved our movie_master_dataset.csv from data-collection.ipynb. Regression.ipynb runs multiple linear regression on five popular genres: action, thriller, drama, romance and comedies and also on three unpopular genres: documentary, history and musical. Kmeans.ipynb runs k-means clustering on the plot keywords of the top 1000 profitable movies and also the 1000 least profitable movies. 