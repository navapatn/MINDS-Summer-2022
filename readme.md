# Sentiment Analysis

## Environment
I used Jupyter Notebook as my main editor. My python version is 3.8+

## Steps and Methodologies
There are four main steps I implemented for this project.

**1.Data Collection**: In this step I used beautifulSoup package to perform data scraping from each article in https://www.aljazeera.com/where/mozambique/
I scraped each article and stored the data in a JSON file (data.json), an example the JSON format I used is below:

{article_id: "article_1"
    {
     title: "title1"
     description: "description1"
     article: "article1"
    }
}
basically, I only stored title, description and the actual news article for out sentiment analysis and classified each article into article_ids.
I was able to do that because of the BeautifulSoup package allowed me to find and extract the class_id in the HTML file that this website uses to identify the article.

**2.Data Preprocessing**: I did not have to do much work since I excluded unrelated part of the article out in the scraping step, but I did cleaned up some extra HTML tags that came along in the scraping steps.


**3.Compute Sentiment using Vader**: 
I chose Vader since it is a pre-trained sentiment analysis algorithm that is easy to implement, and the result is clear and easy to interpret.
In this file (sentiment.py) I read the JSON file from step 1 and 2, then formatted and plugged it into Vader algorithm.

**4.Visualization and Result**:
I used plotly library to visualize the result I got from Vader algorithm.
Out of 10 most recent articles, 8 of them have negative sentiment and 2 of them have positive sentiment according to Vader.
image



