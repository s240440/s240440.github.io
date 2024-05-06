---
layout: default

title: Exploring the Landscape of Beer Reviews
subtitle: A deep dive into inter- and cross-national opinions on beers
subsubtitle: Are some countries more opinionated than others?

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
Humans consume many different kinds of beverages through life, where the alcoholic beverage, beer, is among the top 10 most consumed beverages across the world. A diverse beverage that brings many people pleasure through life, comes in different colors and offers different tastes. [[1]](#ref1) Besides being a top consumed beverage, it is also known for being one of the oldest human-produced beverages, originating more than 5000 years ago and was done by the Sumerians of the ancient Mesopotamia. [[2]](#ref2) While it originates many years back, the commercial brewing as known today, began in the 13th century in Germany, England and Austria. [[3]](#ref3) Looking at modern times, beer is being brewed in almost every country and therefore gives a variety of beers to choose and results in many opinions, which leads to mutliple questions: *Which beer is the best?”,* *Which country has the best reviews?"*, *Which beer do people like the most; local or overseas?*" and many more. [[4]](#ref4) To try and answer some of these questions, in this article, the beer review dataset from [RateBeer](https://www.ratebeer.com/) will be examined by looking at ratings and reviews of beers across breweries and countries.

Here, we will review the reviews of the brews, and condense all of the information contained within the data, to give you a story of how people enjoy their beers internationally, and which country seemingly enjoys beer the very most. We also urge you to explore on your own, draw your own conclusions and enjoy taking a deeper dive into reviews from RateBeer with us.

The journey of the beer review investigation begins with a dataset from [RateBeer](https://www.ratebeer.com/) provided from the data website [Snap](https://snap.stanford.edu/data/web-RateBeer.html). A dataset containing ~7 million reviews, ~70K users, ~440K beers, ~24k breweries and more, which has a timespan from 1998 to 2011. With multiple attributes and text reviews containing ratings with five aspects, a data story will be developed by investigations of many different aspects across the provided data, to see if locations, breweries sizes, user profiles and many other variables has a connection regarding the final ratings of different beers. Naturally, this makes us unable to make solid comments on which beers are enjoyed the most in year of 2024, though there will still be plenty of ideas one can get about how we all enjoy beer around the world. After all, beer has existed for quite a while!

As [RateBeer](https://www.ratebeer.com/) is an american forum, the dataset only contains the names and entries of breweries that users have actually given reviews. This is imperative to keep in mind, as the countries of Asia are misrepresented in this data story. While we keep them close to heart, let’s dive in.

As to get a better ideas of what beers the common man is likely to drink, we have filtered the data sets to only contain the beers which has been reviewed more than 200 times. This takes away some of the more unique, special beers, but it makes for more interesting analysis later on, as we will not be caught up in a single person having reviewed their favorite, special, niché beer. As we want to give a chance for you to know some of the beers highlighted later on. Don't be discouraged if there are none, though; treat it like a recommendation instead or perhaps a warning. 

## The Breweries
Firstly, we want to scratch the surface of the data, and show which countries are the most active on the beer-reviewing forum and give an idea of how the beer landscape looks like. Scroll through the image slider that shows [Figure 1](#figure1), [Figure 2](#figure2) and [Figure 3](#figure3) to see some of the surface level statistics, regarding the user base.
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

Now, looking at the overall, average beer ratings for some of the countries on [Figure 1](#figure1), we see that Norway comes out slightly on top, though they have only won two international awards from the World Beer cup in 2008. In contrast a country such as Germany and the second place runner up Belgium amass 136 and 58 awards respectively, in the years the data set spans over. And they both continue to win plenty awards even to todays date, so perhaps the overall ratings have been skewed now. [[5]](#ref5) From this it is clear that the majority of the reviews are made by amateur beer connoisseurs, and that the reviews do not reflect all of the individuals from the different countries. They definitely do not follow the actual experts. But there must be a reason for why Norway edges out to the top of the leaderboards, and it can be understood better, when we realise, that for example Germany also produces a lot of beers, with the largest amount of breweries in Europe. While they both have the capability of producing world-class beer, Norway might simply produce less, that are of consistently high quality without anything being particularly award winning.

<div class="l-page" style="max-width: 100%;">
  <img src="{{ 'assets/plotly/NorwayAndGermanyBeerRatings.png' | relative_url }}" frameborder='0' scrolling='no' height="auto;" width="100%" style="border: 0px">
</div>
<div id="figure4" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 4: Norway and Germany Global Beer Ratings.
</div>

This can be seen in the two histograms on [Figure 4](#figure4) where we have shown the distribution of ratings for Norway and Germany. When looking at Norway, we do indeed see this consistent rating, without much divergence from the mean value. Germany however has a thicker and longer tail in its distribution towards the lower ratings, which solidifies the fact that if you produce a lot of different beer, you also risk producing some that are of lower quality. Sometimes this is a necessary evil for breweries to find the next big thing.

<div class="l-page">
  <iframe src="{{ '/assets/plotly/breweries_per_area.html' | relative_url }}" frameborder='0' scrolling='no' height="700px" width="1100px" style="border: 0px;"></iframe>
</div>
<div id="figure5" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 5: Ratios of Breweries Per Area [KM2].
</div>

If we want to get a more fair depiction of the brewery landscape, we should take a look at figure [Figure 5](#figure5) in which we have taken a ration between the amount of breweries and the area of the country. This gives us an idea of how many breweries each country has built, and gives us more insight in which country comes out on top in terms of enthusiastically producing this amazing beverage. From looking and hovering over the bubbles, you can notice that it is indeed the size of the country, which makes USA stand out on top, while countries such as Belgium, The Netherlands, Germany and Denmark start to become more fairly depicted. We are still missing something, though, and we don’t get the full picture. While this may show enthusiasm and a desire to innovate new brews; in terms of beer produce in liters Germany is by far the leading producer in all of Europe and China is the largest producer in globally. [[6]](#ref6)

## The Beer Ratings
To continue the story, we want to dive deeper into the opinions from different countries towards eachother and themselves. This is where things get more interesting as you can unearth some of the sentiments we have towards beers maybe from your own country and beers overseas. On [Figure 6](#figure6) you can more easily see which countries has different ratings, and we see the central part of Europe being mostly in the green, while the southern part of eastern europe are below what would be considered average. Looking at America, we see the northern and central part having higher average ratings than in the south.

<div class="l-page">
  <iframe src="{{ '/assets/plotly/choropleth_globalrating.html' | relative_url }}" frameborder='0' scrolling='no' height="800px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure6" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 6: Average Ratings of Beers Based on Location of Brewery.
</div>

It is no secret that beer changes during transport, [[7]](#ref7) and that the water conditions and local ingredients will determine the quality of the produce. An old saying says that “beer is best enjoyed in the shadows of the brewery”, and this likely has truth to it. Back then, the export of beer could have been significantly worse than it is today, which could leave a mark on these countries’ rating from back then. To truly dive into this aspect, we have averaged the ratings from users of different countries of interest towards other countries globally, to see how the ratings changes. Particularly interesting is the of the countries’ ratings of themselves; are they positive or negative? Who is the most positive about beer? Look at Italy for example. Are there countries whose ratings could be affected by outside circumstances? Look at for example China. Take a look on [Figure 7](#figure7) and use the dropdown menu to see how the landscape changes.

<div class="l-page">
  <iframe src="{{ '/assets/plotly/choropleth.html' | relative_url }}" frameborder='0' scrolling='no' height="800px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure7" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 7: Difference in Ratings based on the Location of the Reviewers.
</div>

With newfound knowledge we return back from that time capsule and we remember that it is exactly that. Today, the beer market has changed drastically, but our opinions of one anothers’ beer can easily have stayed the same. Of course, beer can not be condensed into a single number, as there is such a large variety with their own different nuances. So far we have only looked at these numbers and tried drawing conclusions, with some success. Based on the ratings themselves countries such as Germany and England seem quite critical, while the US generally forms a good opinion of many brews globally. Finally it is time to dive into what people say.


## The Beer Reviews
On [Figure 8](#figure8) we have chosen the english reviews from different countries on other, and their own, countries’ best and worst rated beer globally. You can see the top ten words used, and with the percentage of times that word is used in a positive context, when describing that beer.
With this beverage, it is hard to say what is positive and what is negative - sometimes you want a beer to be bitter, but not bitter, and sometimes you might want it to be sweeter but not sweet. Naturally, as we only look at the english reviews, the reviews made in their native languages are lost. Despite this, it manages to encapsulate most of the sentiment for most of the beers; so we urge you to take a good look, and see if you can discover some of the funny remarks.

<div class="l-page">
  <iframe src="{{ '/assets/plotly/Tree_plot.html' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure8" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 8: Top 10 Words in Reviews on Countries' Best and Worst Beers
</div>

## Conclusion
While everyone is different in their own way, we all form our own opinions of the things we enjoy, and this is no different. We can see that people from some nationalities can be quite critical of the things they enjoy, and making it known to the world, but we also see the enjoyment it brings. Whether a country has a large produce, many breweries or many users on a beer rating forum, every opinion is valid, and we can see that in the end; good beer is good no matter where you are from. Fantastically, even if beer is regarded as bad, it is often not because it is a bad beverage, it seems like sometimes, it is simply not good in the context of being a beer. Other times, however, you can safely trust the ratings, whether that is because of export or it being a bad brew. We provide a final reminder that the story told is within the confines of 1998 to 2011, though some opinions are of course hard to change.

* * *

## References
<a name="ref1">1</a>: Top 10 consumed beverages [https://nawon.com.vn/top-10-worlds-most-consumed-beverage/](https://nawon.com.vn/top-10-worlds-most-consumed-beverage/)

<a name="ref2">2</a>: Who invented beer [https://www.history.com/news/who-invented-beer](https://www.history.com/news/who-invented-beer)

<a name="ref3">3</a>: Where did beer originate from [https://www.brewscruise.com/blog/where-did-beer-originate-from/](https://www.brewscruise.com/blog/where-did-beer-originate-from/)

<a name="ref4">4</a>: Beer in different countries [https://craftbeerme.com/beer-in-different-countries/](https://craftbeerme.com/beer-in-different-countries/)

<a name="ref5">5</a>: Award winners [https://www.worldbeercup.org/winners/award-winners/](https://www.worldbeercup.org/winners/award-winners/)

<a name="ref6">6</a>: Leading 10 countries in worldwide beer production [https://www.statista.com/statistics/270269/leading-10-countries-in-worldwide-beer-production/](https://www.statista.com/statistics/270269/leading-10-countries-in-worldwide-beer-production/)

<a name="ref7">7</a>: Influence of transport and storage conditions on beer quality and flavour stability [https://onlinelibrary.wiley.com/doi/full/10.1002/jib.535](https://onlinelibrary.wiley.com/doi/full/10.1002/jib.535)
