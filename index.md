---
layout: default

title: Beer Reviews
subtitle: A data-driven story told by Group 15

authors:
  - name: Martin Nguyen - 
    affiliations:
      name: s194378
  - name: Asbjørn H. Petersen - 
    affiliations:
      name: s204084
  - name: Sarah Hecht Petersen - 
    affiliations:
      name: s240440
---      

* * *

## Introduction
Humans consume many different kinds of beverages through life, where the alcoholic beverage, beer, is among the top 10 most consumed beverages across the world. A diverse beverage that brings many people pleasure through life, comes in different colors and offers different tastes. [[1]](#ref1) Besides being a top consumed beverage, it is also known for being one of the oldest human-produced beverages, originating more than 5000 years ago and was done by the Sumerians of the ancient Mesopotamia. [[2]](#ref2) While it originates many years back, the commercial brewing as known today, began in the 13th century in Germany, England and Austria. [[3]](#ref3) Looking at modern times, beer is being brewed in almost every country and therefore gives a variety of beers to choose and results in many opinions, which leads to mutliple questions: *Which beer is the best?”,* *Which country has the best reviews?"*, *_Which beer do people like the most; local or overseas?_*" and many more. [[4]](#ref4) To try and answer some of these questions, in this article, the beer review dataset from **RateBeer** will be examined by looking at ratings and reviews of beers across breweries and countries.

Here, we will review the reviews of the brews, and condense all of the information contained within the data, to give you a story of how people enjoy their beers internationally, and which country seemingly enjoys beer the very most. We also urge you to explore on your own, draw your own conclusions and enjoy taking a deeper dive into reviews from RateBeer with us.

## Beer Reviews from Data
The journey of the beer review investigation begins with a dataset from [RateBeer](https://www.ratebeer.com/) provided from the data website [Snap](https://snap.stanford.edu/data/web-RateBeer.html). A dataset containing ~3 million reviews, ~40K users, ~110K beers and more, which has a timespan from April 2000 to November 2011. With multiple attributes and text reviews containing ratings with five aspects, a data story will be developed by investigations of many different aspects across the provided data, to see if locations, breweries sizes, user profiles and many other variables has a connection regarding the final ratings of different beers. Naturally, this makes us unable to make solid comments on which beers are enjoyed the most in year of 2024, though there will still be plenty of ideas one can get about how we all enjoy beer around the world. After all, beer has existed for quite a while!
As RateBeer is an american forum, the dataset only contains the names and entries of breweries that users have actually given reviews. This is imperative to keep in mind, as the countries of Asia are misrepresented in this data story. While we keep them close to heart, let’s dive in.

As to get a better ideas of what beers the common man is likely to drink, we have filtered the data sets to only contain the beers which has been reviewed more than 200 times. This takes away some of the more unique, special beers, but it makes for more interesting analysis later on, as we will not be caught up in a single person having reviewed their favorite, special, niché beer. As we want to give a chance for you to know some of the beers highlighted later on. Don't be discouraged if there are none, though; treat it like a recommendation instead or perhaps a warning. 

## The Breweries
Firstly, we want to scratch the surface of the data, and show which countries are the most active on the beer-reviewing forum and give an idea of how the beer landscape looks like. Scroll through figure [scroller fig] to see some of the surface level statistics, regarding the user base.
<html>
  <head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/bxslider/4.2.12/jquery.bxslider.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
    <script src="https://cdn.jsdelivr.net/bxslider/4.2.12/jquery.bxslider.min.js"></script>
    <script>
      $(document).ready(function(){
        $(".bxslider").bxSlider(); 
      });
    </script>
  </head>
  <body>
    <ul class="bxslider">
        <li><img src="/assets/plotly/Top30LocationsRating.png" /></li>
        <li><img src="/assets/plotly/Top30LocationsBreweries.png" /></li>
        <li><img src="/assets/plotly/Top30LocationsUsers.png" /></li>
    </ul>
    <div id="figure1" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 1: Top Locations by Average Beer Rating.
    </div>
    <div id="figure2" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 2: Top Locations with the Most Active Breweries.
    </div>
    <div id="figure3" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 3: Top Locations with the Most Active Users.
    </div>
  </body>
</html>

Now, looking at the overall, average beer ratings for some of the countries, we see that Norway comes out slightly on top, though they have only won two international awards from the World Beer cup in 2008. In contrast a country such as Germany and and the second place runner up Belgium amass 136 and 58 awards respectively, in the years the data set spans over. And they both continue to win plenty awards even to todays date, so perhaps the overall ratings have been skewed now[https://www.worldbeercup.org/winners/award-winners/]. From this it is clear that the majority of the reviews are made by amateur beer connoisseurs, and that the reviews do not reflect all of the individuals from the different countries. They definitely do not follow the actual experts. But there must be a reason for why Norway edges out to the top of the leaderboards, and it can be understood better, when we realise, that for example Germany also produces a lot of beers, with the largest amount of breweries in Europe. While they both have the capability of producing world-class beer, Norway might simply produce less, that are of consistently high quality without anything being particularly award winning.
<div class="l-page">
  <iframe src="{{ '/assets/plotly/NorwayAndGermanyBeerRatings.png' | relative_url }}" frameborder='0' scrolling='no' height="650px" width="1100px" style="border: 0px;"></iframe>
</div>
<div id="figure4" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 4: Norway and Germany Global Beer Ratings.
</div>
This can be seen in the two histograms on Figure [####] where we have shown the distribution of ratings for Norway and Germany. When looking at Norway, we do indeed see this consistent rating, without much divergence from the mean value. Germany however has a thicker and longer tail in its distribution towards the lower ratings, which solidifies the fact that if you produce a lot of different beer, you also risk producing some that are of lower quality. Sometimes this is a necessary evil for breweries to find the next big thing.

<div class="l-page">
  <iframe src="{{ '/assets/plotly/breweries_per_area.html' | relative_url }}" frameborder='0' scrolling='no' height="700px" width="1100px" style="border: 0px;"></iframe>
</div>
<div id="figure5" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 5: Ratios of Breweries Per Area [KM2].
</div>

If we want to get a more fair depiction of the brewery landscape, we should  take a look at figure [blob plot] in which we have taken a ration between the amount of breweries and the area of the country. This gives us an idea of how many breweries each country has built, and gives us more insight in which country comes out on top in terms of enthusiastically producing this amazing beverage. From looking and hovering over the bubbles, you can notice that it is indeed the size of the country, which makes USA stand out on top, while countries such as Belgium, The Netherlands, Germany and Denmark start to become more fairly depicted. We are still missing something, though, and we don’t get the full picture. While this may show enthusiasm and a desire to innovate new brews; in terms of beer produce in liters Germany is by far the leading producer in all of Europe and China is the largest producer in globally. [# https://www.statista.com/statistics/270269/leading-10-countries-in-worldwide-beer-production/ #].


## The Beer Ratings
To continue the story, we want to dive deeper into the opinions from different countries towards eachother and themselves. This is where, things get more interesting as you can unearth some of the sentiments we have towards beers from our own country and beers overseas. On Figure [## geo map 1 ##] you can more easily see which countries has different ratings, and we see the central part of Europe being mostly in the green, while the southern part of eastern europe are below what would be considered average. Additionally the US are well considered, while South America seems to be mostly in the red. 

<div class="l-page">
  <iframe src="{{ '/assets/plotly/choropleth_globalrating.html' | relative_url }}" frameborder='0' scrolling='no' height="800px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure6" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 6: Average Ratings of Beers Based on Location of Brewery.
</div>

<div class="l-page">
  <iframe src="{{ '/assets/plotly/choropleth.html' | relative_url }}" frameborder='0' scrolling='no' height="800px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure7" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 7: Average Ratings of Beers Based on Location of Brewery.
</div>

## The Beer Reviews

<div class="l-page">
  <iframe src="{{ '/assets/plotly/Tree_plot.html' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure8" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 8: Top 10 Words in Reviews on Countries' Best and Worst Beers
</div>

## Conclusion

* * *

## References
<a name="ref1">1</a>: Top 10 consumed beverages [https://nawon.com.vn/top-10-worlds-most-consumed-beverage/](https://nawon.com.vn/top-10-worlds-most-consumed-beverage/)

<a name="ref2">2</a>: Who invented beer [https://www.history.com/news/who-invented-beer](https://www.history.com/news/who-invented-beer)

<a name="ref3">3</a>: Where did beer originate from [https://www.brewscruise.com/blog/where-did-beer-originate-from/](https://www.brewscruise.com/blog/where-did-beer-originate-from/)

<a name="ref4">4</a>: Beer in different countries [https://craftbeerme.com/beer-in-different-countries/](https://craftbeerme.com/beer-in-different-countries/)

