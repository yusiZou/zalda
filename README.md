# Secrets inside Clinton's email

# Abstract
In 2015, Hillary Clinton has been embroiled in controversy over the use of personal email accounts on non-government servers during her time as the United States Secretary of State. Over 2000 confidential emails were leaked, some of them are even classified as “Top Secret”. 

In this project we will look at the politic, security and economic aspects through the 7945 leaked emails redacted and published by the State Department and cleaned by Kaggle. We also want to analyze the personal social network of Hillary Clinton and the top topics they discussed.

As a superpower, the United States has a great impact on the world’s stability, and their position and attitude will strongly influence the international affairs. We want to figure out the countries mainly mentioned, the problems concerned and conclude the impact they made on the international affairs throughout the analysis of these emails.

# Research questions
In this project we want to figure out:

- With whom does she communicate most? What are their positions?
- What countries are mostly mentioned in the emails?
- What is the time series relation between the global events and the emails?
- Is her attitude positive or negative in the emails? How is her attitude to the other countries? 
- What topics does she discuss?

# Dataset

### Original Dataset:
We will use the dataset on [Kaggle](https://www.kaggle.com/kaggle/hillary-clinton-emails). It contains four csv files: 
- `Aliases.csv` (~ 20kB)
- `EmailReceivers.csv` (~ 117Kb)
- `Emails.csv` (~ 24.4 MB)
- `Persons.csv` (~ 9.93KB)

The most important information is in `Emails.csv`. It contains 7945 rows (emails), some of them are less important, just "FYI" or without any body text. It contains 22 columns, including the alias of sender and receiver, the sending time and the body text. The other data files will help us to identify the real name of people involved: `Aliases.csv` identifies the alias to the _PersonId_, `EmailReceivers.csv` maps the receivers of emails to the _PersonId_ and `Persons.csv` translate the unique _PersonId_ to their realname.

The number of samples in the date set is not very large. In addition to the analysis of numeric data, we will also concentrate on textual content and keywords.

### Additional Dataset:
- In addition to our basic dataset, we also use a dataset for country names which can be found in [Statgraphics](http://www.statgraphics.com/). 
- In order to visulize the world map, we also use a json file for country boarders which can be found on [this website](https://geojson-maps.ash.ms/). 

# What we have done until milestone 2
* Data wrangling: clean and deal with unvalid or missing data.
* Combine and merge data files for further analysis.
* Find the communication frequency between Hillary and the others in both direction.
* Construct a countries occurence list and visualization.

# What we will do until milestone 3
- Analyze the position of people with whom Hillary communicate with.
- Figure out the time series relation between the global events and the emails : analyse the distribution of time for the most frequently mentioned countries and search for the reason behind.
- Do sentiment analysis (positive or negative) on the emails and find the US government's (or more precisely, Hillary's) attitude to the other countries. Use the Natural Language Toolkit (NLTK) to analyze the email texts and classify the mood.
- Find the topics that she discusses in general and w.r.t the different countries and different people. Use the term-frequency-inverse document frequency (tf-idf) method to find topics. The term frequency indicates the number of times a term occurs in a specific document, and the inverse document frequency indicates the frequency of a term in all document. If the TF is high, then it seems to be an important topic, but if at the same time the IDF is high, it means that this word is in too many documents that it losses importance.

