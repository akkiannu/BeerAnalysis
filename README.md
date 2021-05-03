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
### Exploratory
I would first like to explore the relation between ABV and IBU as well as their distribution for it.
* IBU and ABV distributions
* Serving Size distributions

#### IBU and ABV Distributions


![image](https://user-images.githubusercontent.com/32137335/116833893-aa3e2200-ab89-11eb-99fd-424bb0644fab.png)

We can clearly see that the ABV Distibution is that of a normal distribution.

Whereas the IBU distribution is a bimodal distribution.

![image](https://user-images.githubusercontent.com/32137335/116833874-97c3e880-ab89-11eb-9b35-cdc80d224ec2.png)


When we plot the ABU vs IBU, we see a that are highly correlated to one another when we change the x scale to a log scale.

![image](https://user-images.githubusercontent.com/32137335/116833947-f7ba8f00-ab89-11eb-98f6-2a053a5143b5.png)

#### Serving Size Distribution

Majority of the beers we see are being served in either12 ounces or 16 ounces as we can see in the image below:
![image](https://user-images.githubusercontent.com/32137335/116833990-246ea680-ab8a-11eb-86e6-cfab496d4f95.png)

It would be interesting to see the above three variables in combination with the beer styles and state of origination.


### Explanatory
Coming to the main part of this project, the main questions for the analysis were as follows:
* What are the most common Beer Styles?
* Which States are the most popular for craft Beers?



#### Coming to the first question, I would like to know the top beer styles:

I have ordered the top 10 beer styles by count when looking at the whole country, following was the graph for it:

![image](https://user-images.githubusercontent.com/32137335/116271154-b96a3d80-a74d-11eb-8b62-8707f16420c7.png)

We see one of the most common types of beer styles in United States is American IPA followed by American Pale Ale and then the American Amber / Red Ale.

Let's see what the ABV vs IBU distribution for the top 10 beers look like:

![image](https://user-images.githubusercontent.com/32137335/116288655-ba0bcf80-a75f-11eb-8168-8d6fc1bc45a0.png)

Interestingly, the top 3 beer style look like their ABV and IBU are highly correlated (i.e. IBU increases with increase in ABV or vice versa) but for the rest, that correlation drops considerably. For example, the vegetable beer although high in alcohol content doesn't seem to have a high IBU.

I would be more interested in the top 3 beers to better answer my question though. I would lieke to compare them on the same graph. Let's see what it looks like:

![image](https://user-images.githubusercontent.com/32137335/116276568-a443dd80-a752-11eb-9d63-516630ca20aa.png)

This is an interesting graph, where we see what composition of ABV and IBU does each of the top 3 beer styles have. American IPA generally is seen to have a high IBU as well as ABV.

Let's look at the most common serving size for the top 10 beer styles:

![image](https://user-images.githubusercontent.com/32137335/116276972-07357480-a753-11eb-9308-436ab9b9ad55.png)

So the ideal serving size for a beer is 12 ounces or 16 ounces.

So to answer the first question, the most common beer style is an American IPA with a high ABV and IBU served in either 12 ounces or 16 ounces. 

#### But this does not pain the whole picture. We would also want to know which states the beer is popular. So coming to the second question, Which states are most popular for craft beers?

Let's first see the distribution of beers across the states. We will only consider the top 10 states by count of beers available there:

![image](https://user-images.githubusercontent.com/32137335/116277627-aa868980-a753-11eb-8eec-14a1eba4c767.png)

Seems like Colorado is one of the most popular states for craft beers followed by California and then Indiana. Let's see if there is anything from the ABV or IBU stand point that differs for each of this state:

![image](https://user-images.githubusercontent.com/32137335/116286147-e1ad6880-a75c-11eb-8057-429929a87725.png)

There doesn't seem to be a lot of difference between each state. Seems like the ABV vs IBU is consistent across the board. Let's see the top 5 beer styles across these top 10 states:

![image](https://user-images.githubusercontent.com/32137335/116289398-74033b80-a760-11eb-8a71-ebf20ce79f54.png)

This seems very interesting, even though American IPA is the most famous beer type across the country, seems like Colorado prefers American Pale Ale over the American IPA. In all the other top 10 states, American IPA is preferred over the rest.



All in all, depending on the State, the beer styles differ. The serving size would make a huge difference as well.














