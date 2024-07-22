# Geo Topics

Goal of this project was to create a tool for geospatial sentiment analisys of certain topics in social media.
Results of our project were summed up on attached poster and presented at open days, media days and AI days on Wrocław University of Science and Technology.

Co-authors: [mprzymus](https://github.com/mprzymus), [tomdrozdz](https://github.com/tomdrozdz)

## How it works ?
### Data
Data was scrapped from Twitter using [snscrape](https://github.com/JustAnotherArchivist/snscrape).
For the purpose of presentations we used 3.3 mln tweets posted between 2018 and 2022 referring to on of 5 Polish cities: Wrocław, Kraków, Poznań, Gdańsk and Warszawa.  

All the tweets were filtered to refer to only one of the cities. Accounts specialized in posting about multiple cities (e.g. weather forcasting, news) were also filtered out.

### Topics

Selection of topics can be done in two ways:
- predefined list of topics
- detection of topics using [BERTopic](https://github.com/MaartenGr/BERTopic)

For the purpose of presentations, topics found by BERTopic were grouped into 10 general categories.

### NLI

To group tweets into topics, we used Natural Language Inference ([DeBERTa](https://huggingface.co/docs/transformers/model_doc/deberta)).
With prepared template, model was prompted to determine if tweet belongs to specified topic. 
Tweets that did not pass confidence threshold were discarded.

### Sentiment

To determine sentiment of tweets, we used [HerBERT](https://huggingface.co/docs/transformers/model_doc/herbert) based model from [sentimentPl](https://pypi.org/project/sentimentpl/) library.
Each tweet was assigned a score between -1 and 1, where -1 is negative sentiment and 1 is positive sentiment.

### Results
As a result, we got a map of sentiment for each topic in each city.
This map can be used to determine how sentiment of certain topics changes over time.  
Such information can be correlated with real-life events, government decisions etc., for example we can see how restrictions during Covid-19 pandemics strongly affected people's feelings about economical situation.

![poster.png](poster.png)
