# Secrets of Clinton
**Authors:** [Yusi Zou](https://github.com/yusiZou), [Junze Li](https://github.com/JunzeLeo) and [Zhantao Deng](https://github.com/GentleDell)

**Data story**: [The legend of Zalda](https://thelegendofzalda.github.io)

## Abstract
In 2015, Hillary Clinton was embroiled in controversy over the use of personal email accounts on non-government servers during her time as the United States Secretary of State. Over 2000 confidential emails were leaked, some of them are even classified as “Top Secret”. 

In this project, we looked at the politic, security and economic aspects through the 7945 leaked emails redacted and published by the State Department and cleaned by Kaggle. We also analyzed the personal social network of Hillary Clinton and the top topics they discussed.

As a superpower, the United States has a great impact on the world’s stability, and their position and attitude will strongly influence international affairs. So, We figured out the countries mainly mentioned, the problems concerned and conclude the impact they made on the international affairs throughout the analysis of these emails.

## 1. Prerequisites
This project is based on [Anaconda](https://www.anaconda.com/) and [Jupyter notebook](https://jupyter.org/).  We install all packages through the Anaconda Prompt. These packages have been tested in **Window 10 Home** and **macOS Mojave**, but it should be easy to implement in other platforms. 

### Anaconda
This project is based on anaconda and jupiter notebook. Download and install instructions can be found at: https://www.anaconda.com/download/. After installing Anaconda, `pip` and `conda` can be used to install Python packages.

### Scipy
We use the scientific computing and visualization functionalities of [scipy](https://www.scipy.org/install.html), especially the numpy, pandas and matplotlib package. These packages can be installed by typing the following command in your Anaconda Prompt.
```
python -m pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose
```

### Seaborn
We use [Seaborn](https://seaborn.pydata.org/) to visualize data. The package can be installed by typing the following command in your Anaconda Prompt.
```
pip install seaborn
```

### Plotly
We use [Plotly](https://plot.ly/) to generate .html files for our figures. The package can be installed by typing the following command in your Anaconda Prompt.
```
pip install plotly 
```
optional:
```
pip install plotly --upgrade
```

### Folium
We use [Folium](https://pypi.org/project/folium/) to display data on maps. The package can be installed by typing the following command in your Anaconda Prompt.
```
pip install folium
```

### NLTK
We use [NLTK](https://www.nltk.org/) to analyze the attitudes of Hillary toward different countries. The package can be installed by typing the following command in your Anaconda Prompt.
```
pip install -U nltk
```

### Wordcloud
We use [wordcloud](https://amueller.github.io/word_cloud/index.html) to generate a wordcloud of keywords in Hillary's emails. The package can be installed by typing the following commands in your Anaconda Prompt.
```
conda install -c conda-forge wordcloud 
conda install -c conda-forge/label/gcc7 wordcloud 
```

## 2. Research questions
In this project we have figured out:
- With whom does she communicate most? What are their positions?
- What countries are mostly mentioned in the emails?
- What topics does she discuss?
- What is the time series relation between the global events and the emails?
- Is her attitude positive or negative in the emails? How is her attitude to the other countries?

## 3. Dataset
### Original Dataset:
We use the dataset on [Kaggle](https://www.kaggle.com/kaggle/hillary-clinton-emails). It contains four csv files: 
- `Aliases.csv` (~ 20kB)
- `EmailReceivers.csv` (~ 117Kb)
- `Emails.csv` (~ 24.4 MB)
- `Persons.csv` (~ 9.93KB)

The most important information is in `Emails.csv`. It contains 7945 rows (emails), some of them are less important, just "FYI" or without any body text. It contains 22 columns, including the alias of sender and receiver, the sending time and the body text. The other data files help us to identify the real name of people involved: `Aliases.csv` identifies the alias to the _PersonId_, `EmailReceivers.csv` maps the receivers of emails to the _PersonId_ and `Persons.csv` translate the unique _PersonId_ to their realname.

The number of samples in the data set is not very large. Therefore, in addition to the analysis of numeric data, we also concentrated on textual content and keywords.

### Additional Dataset:
- In addition to our basic dataset, we used a dataset for country names which can be found in [Statgraphics](http://www.statgraphics.com/). 
- In order to visualize the world map, we used a json file for country borders which can be found on [this website](https://geojson-maps.ash.ms/). 

## 4. What we have done
**Until milestone 2:**
- Data wrangling: clean and deal with invalid or missing data.
- Combined and merged data files for further analysis.
- Found the communication frequency between Hillary and the others in both directions.
- Constructed a countries occurrence list and visualization.

**Until milestone 3:**
- Analyzed the position of people with whom Hillary communicate with.
- Figured out the time series relation between the global events and the emails: analyzed the distribution of time for the most frequently mentioned countries and searched for the reason behind.
- Conducted sentiment analysis (positive or negative) on the emails and found the US government's (or more precisely, Hillary's) attitude to the other countries. Used the Natural Language Toolkit (NLTK) to analyze the email texts and classify the mood.
- Found the topics that she discusses in general and w.r.t the different countries and different people. Used the term-frequency-inverse document frequency (TF-IDF) method to find topics. The term frequency indicates the number of times a term occurs in a specific document, and the inverse document frequency indicates the frequency of a term in all document. If the TF is high, then it seems to be an important topic, but if at the same time the IDF is high, it means that this word is in too many documents that it losses importance.
- [Data story](https://thelegendofzalda.github.io)

## 5. Contributions of group members
**Yusi Zou:**
- Data wrangling
- The communication network of Hillary
- Data story

**Junze Li:**
- The countries occurrence list
- Sentiment Analysis
- Data story

**Zhantao Deng:**
- Occurrence World Map
- Visualizing and analyzing occurrences by months and by countries
- Topic analysis using TF-IDF

The team collaborate very well together and will work together for the final poster and presentation.