# Craft Beer Analysis
## by Akshay Gupta

## Dataset

For this project, I have gathered the data from Kaggle.com. Link for the database: https://www.kaggle.com/nickhould/craft-cans

I am a big beer lover, so this project was an eye opener for me as well. Although I started my beer journey with Lager, I have grown to like IPA's a lot. It is just one of those things where your taste buds evolve slowly and steadily. 

When getting into this project, one of the biggest question I had for myself was, how does the bitterness of the alcohol correlate with the alcohol percent of the beer. Throughtout this analysis, I have tried answering that question.

###### ABV: 
Alcohol by volume (abbreviated as ABV, abv, or alc/vol) is a standard measure of how much alcohol (ethanol) is contained in a given volume of an alcoholic beverage (expressed as a volume percent). It is defined as the number of millilitres (mL) of pure ethanol present in 100 mL of solution at 20 °C (68 °F).

###### IBU: 
International Bitterness Units are a chemical measurement of the number of bittering compounds, specifically isomerized and oxidized alpha acids, polyphenols, and a few other select bittering chemicals, that make your beer taste bitter. The IBU correlates well, in most cases, with the sensory bitterness of beer, and this is why brewers use it. Almost all the beer you’ll ever drink will have a measured IBU between five (which is a very low measured bitterness) up to 120 (which is a very high measured bitterness). One thing to keep in mind though, bitterness of a beer doesn't make it better or worse. Since there was no way of measuring how bitter a beer is, IBU came to be. 

Additionally, to understand more about the beer styles, craftbeers has explained it the best: https://www.craftbeer.com/beer-styles

So we have established our base and understanding of the common termonologies, let's get to data exploration.

### Gathering, Assessing & Cleaning:
#### Gathering:
There are two separate datasets:
1. beers.csv
2. breweries.csv

Both of these datasets were downloaded from the Kaggle link above on to my local drive.

#### Assessing and Cleaning:
The dataset as such was clean and required a little bit of tidying up.
There were some basic cleaning operations performed for this project. It involved removing rows that had ABV and IBU as an empty value. Additionally, I merged the two datasets above to form one dataframe. The key to joining the dataset was the brewery_id.

## Summary of Findings:
### Top 10 Beer Styles:

I first tried determining the top 10 Beer Styles based on counts in the dataset that I had. Following is the distribution of the same:

![image](https://user-images.githubusercontent.com/32137335/116932101-da400080-ac2f-11eb-943e-071f17a04704.png)

### Top 10 States for Breweries:

As per the number of beer counts, next I wanted to determine the top 10 States:

![image](https://user-images.githubusercontent.com/32137335/116932213-f80d6580-ac2f-11eb-9475-e8095841819d.png)

### Serving Size:

This was the distribution of the serving size:

![image](https://user-images.githubusercontent.com/32137335/116932297-0fe4e980-ac30-11eb-8def-5b2bd838b2c8.png)

We can clearly see the two main serving portions are 12 Oz. and 16 Oz.


### IBU vs Serving Size:

Going by the following boxplot, it is fairly safe to assume that serving size does not determine the IBU of a beer.

![image](https://user-images.githubusercontent.com/32137335/116932673-8da8f500-ac30-11eb-9d76-2bf3933838d4.png)


### ABV vs Serving Size:

Similarly, looks like serving size does not determine the alcohol by volume as well of a particular beer.

### Serving Size in Top 10 States:

Having established the top 10 states, we now look at the serving size in the top 10 states by count. Following is the distribution of the same.

![image](https://user-images.githubusercontent.com/32137335/116932855-c9dc5580-ac30-11eb-9017-747775a58e13.png)

It seems like some state prefer 16 Oz. over 12 Oz.. States like Indiana specifically show this kind of behaviour.

### Serving Size for Top 10 Beer Styles:

Having previously established the top 10 beer styles, we now see the serving size of these beers:

![image](https://user-images.githubusercontent.com/32137335/116933215-3e16f900-ac31-11eb-9e39-45aa3dd30f7a.png)

One interesting finding here is that the American Porter is preferred in a 16 Oz. serving vs. a 12 Oz. serving.

## Key Insights:

### Relation between ABV and IBU (ABV vs. IBU):

ABV and IBU seem to be highly correlated, i.e. if one increases the other increases as well. This is looking at the overall population.

![image](https://user-images.githubusercontent.com/32137335/116932508-5c302980-ac30-11eb-8d81-498362e7a6b6.png)

### ABV vs. IBU for Top 10 Beers:

What was interesting here is that the ABV and IBU composition changes based on the beer style. This is evident when we look at the distribution of the ABV vs. IBU of American Pale Wheat Ale. The IBU is constant even when the ABV is increasing.

![image](https://user-images.githubusercontent.com/32137335/116933568-b67dba00-ac31-11eb-948d-d1571eb38d39.png)

We can say that Beer Style is one of the key factors in defining the composition of IBU and ABV.

### ABV vs. IBU for Top 3 Beers:

Reiterating the above finding, we can clearly see the differing composition of IBU and IBV when we consider the top 3 beers. This does not even consider the American Pale Wheat Ale, whose composition was again very different.

![image](https://user-images.githubusercontent.com/32137335/116933705-e9c04900-ac31-11eb-8bc1-74f35bdf9687.png)

### ABV vs. IBU for Top 10 Beer States:

Interstingly, the origin of the beer also makes a slight difference in the composition of the beer. The type of beer doesn't matter here. 

![image](https://user-images.githubusercontent.com/32137335/116933899-3146d500-ac32-11eb-8583-91952b749f1f.png)







