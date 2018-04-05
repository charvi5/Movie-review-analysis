
Description
-------------------------------------------------------------------------------------------------------------------------
This analysis involved scraping movie ratings, critic and user reviews, genre, box office collection, director from a movies forum. The analysis helped understand how is box office collection driven by user and critic reviews. It also helped figure the frequently used words by critics for different genre of movie along with sentiment associated.

Notes
-------------------------------------------------------------------------------------------------------------------------
- The code has been written used Python3 using Jupiter notebook as interface

- The code needs to be executed in a sequential fashion as in certain case previously created tables are referred to later

**Approach**
------------------------------------------------------------------------------------------------------------------------
Audience and critic reviews along with other movie variables were scraped from a movies forum using Selenium and BeautifulSoup. The text data was cleaned by removing stopwords, [word stemming and lemmatization](https://nlp.stanford.edu/IR-book/html/htmledition/stemming-and-lemmatization-1.html).  
Word frequency for different genre types was calculated for critic reviews to understand the frequently used words.  
VaderSentiment was used to calculate sentiment scores for different movies and their relationship with box office collection was calculated.  
This analysis can be useful for movie marketing teams to brand their movie based on certain features.  
Also, it can help them figure out if critic reviews can sway their box office collection and then rebrand accordingly.  
For a more sophisticated solution, as part of future work, [topic modeling](https://en.wikipedia.org/wiki/Topic_model) with [sentiment analyzer](https://en.wikipedia.org/wiki/Sentiment_analysis) can be employed to look for topics which are frequently mentioned in different genre of movies and associated sentiments.  

Installing libraries and packages
-----------------------------------------------------------------------------------------------------------------------
To run the notebook, following list of packages must be installed in the system:
-  Pandas
-  Numpy
-  bs4
    -  ```from bs4 import BeautifulSoup```
-  selenium
- nltk
- re
- itertools
- string
- vaderSentiment

To scrap data for movie reviews from the website, Chrome was used as the web browser. 
- Download [latest Chromedriver] (https://sites.google.com/a/chromium.org/chromedriver/downloads) and transfer unzipped file to /usr/bin
- Run ```from selenium import webdriver```
      ```driver = webdriver.Chrome()```

**nltk** is a Natural Language toolkit and is used for natural language processing. Following libraries need to be imported form the toolkit:  
- ```from nltk.corpus import brown```
- ```from nltk.corpus import stopwords```
- ```from nltk.stem import WordNetLemmatizer```

**Mac OS:**
- To download libraries and packages being loaded in first block of the code, go to Terminal and download packages using 
```pip install package-name ```
- If pip throws an error due to packages not being a part of pip anymore, use ```conda install package-name``` , this is an Anaconda command and directly downloads packages in Anaconda . 

**Windows:**
- Open Windows command prompt and enter ```py -3.6 -m pip install package-name```

-------------------------------------------------------------------------------------------------------------------------
