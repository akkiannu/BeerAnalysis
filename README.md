# Craft Beer Analysis

For this project, I have gathered the data from Kaggle.com. Link for the database: https://www.kaggle.com/nickhould/craft-cans

I am a big beer lover, so this project was an eye opener for me as well. Although I started my beer journey with Lager, I have grown to like IPA's a lot. It is just one of those things where your taste buds evolve slowly and steadily. 

When getting into this project, one of the biggest question I had for myself was, if I had to be a consultant for a brewery who is looking to expand their business in a new state or city, what would I advice them? This is the question I would be trying to answer throughout this project. Right from which beer style to how much ABV and IBU (explained below) to how much of a serving size is ideal for a specific market.

###### ABV: 
Alcohol by volume (abbreviated as ABV, abv, or alc/vol) is a standard measure of how much alcohol (ethanol) is contained in a given volume of an alcoholic beverage (expressed as a volume percent). It is defined as the number of millilitres (mL) of pure ethanol present in 100 mL of solution at 20 °C (68 °F).

###### IBU: 
International Bitterness Units are a chemical measurement of the number of bittering compounds, specifically isomerized and oxidized alpha acids, polyphenols, and a few other select bittering chemicals, that make your beer taste bitter. The IBU correlates well, in most cases, with the sensory bitterness of beer, and this is why brewers use it. Almost all the beer you’ll ever drink will have a measured IBU between five (which is a very low measured bitterness) up to 120 (which is a very high measured bitterness). One thing to keep in mind though, bitterness of a beer doesn't make it better or worse. Since there was no way of measuring how bitter a beer is, IBU came to be. 

Additionally, to understand more about the beer styles, craftbeers has explained it the best: https://www.craftbeer.com/beer-styles

So we have established our base and understanding of the common termonologies, let's get to data exploration.

## Gathering, Assessing & Cleaning:
### Gathering:
There are two separate datasets:
1. beers.csv
2. breweries.csv

Both of these datasets were downloaded from the Kaggle link above on to my local drive.

### Assessing and Cleaning:
The dataset as such was clean and required a little bit of tidying up.
There were some basic cleaning operations performed for this project. It involved removing rows that had ABV and IBU as an empty value. Additionally, I merged the two datasets above to form one dataframe. The key to joining the dataset was the brewery_id.

## Analysis:
Coming to the main part of this project, the main questions for the analysis were as follows:
* What are the most common Beer Styles?
* Which States are the most popular for Breweries?
* What composition of ABV and IBU does a beer have?
* What are the most common serving size?

Coming to the first question, I have ordered the top 10 beer styles by count when looking at the whole country, following was the graph for it:
![image](https://user-images.githubusercontent.com/32137335/116268265-27f9cc00-a74b-11eb-87e9-082318679ad5.png)













