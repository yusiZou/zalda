# Secrets inside Clinton's email

# Abstract
In 2015, Hillary Clinton has been embroiled in controversy over the use of personal email accounts on non-government servers during her time as the United States Secretary of State. Over 2000 confidential emails were leaked, some of them are even classified as “Top Secret”. 

In this project we will look at the politic, security and economic aspects through the 7945 leaked emails redacted and published by the State Department and cleaned by Kaggle. We also want to analyze the personal social network of Hillary Clinton and the top topics they discussed.

As a superpower, the United States has a great impact on the world’s stability, and their position and attitude will strongly influence the international affairs. We want to figure out the countries mainly mentioned, the problems concerned and conclude the impact they made on the international affairs throughout the analysis of these emails.

# Research questions
In this project we want to figure out:
- What countries are mostly mentioned in the emails?
- What is the time series relation between the global events and the emails?
- What sentiment and emotion are expressed in the emails?
- To whom does she communicate most? What are their position?
- What are the key words in these emails?
- What topics do they discuss?

# Dataset

We will use the dataset on [Kaggle](https://www.kaggle.com/kaggle/hillary-clinton-emails). It contains four csv files: 
- `Aliases.csv` (~ 20kB)
- `EmailReceivers.csv` (~ 117Kb)
- `Emails.csv` (~ 24.4 MB)
- `Persons.csv` (~ 9.93KB)

The most important information is in `Emails.csv`. It contains 7945 rows (emails), some of them are less important, just "FYI" or without any body text. It contains 22 columns, including the alias of sender and receiver, the sending time and the body text. The other data files will help us to identify the real name of people involved: `Aliases.csv` identifies the alias to the _PersonId_, `EmailReceivers.csv` maps the receivers of emails to the _PersonId_ and `Persons.csv` translate the unique _PersonId_ to their realname.

The number of samples in the date set is not very large. In addition to the analysis of numeric data, we will also concentrate on textual content and keywords.

# A list of internal milestones up until project milestone 2
_to be done before 25th November_
- Data wrangling: clean and deal with unvalid or missing data; combine data files for useful information
- Construct a countries occurence list
- Identify key words related to international affairs in the body text
- Find the communication frequency between Hillary and the others
- Personal social network creation and analysis: use the communication frequency to create a personal social network of Hillary and analyze the network structure

# Questions for TAa
1. How do you find the scope of our project? Does it fit the expectation?
2. We want to relate our project to the theme "Data Science for social good" in this way: we think that by looking at these emails, we can figure out its impact on international affaires which influence the global stability and security. Is our motivation clear enough?



