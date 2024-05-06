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
Humans consume many different kinds of beverages through life, where the alcoholic beverage, beer, is among the top 10 most consumed beverages across the world. A diverse beverage that brings many people pleasure through life, comes in different colors and offers different tastes. [[1]](#ref1) Besides being a top consumed beverage, it is also known for being one of the oldest human-produced beverages, originating more than 5000 years ago and was done by the Sumerians of the ancient Mesopotamia. [[2]](#ref2) While it originates many years back, the commercial brewing as known today, began in the 13th century in Germany, England and Austria. [[3]](#ref3) Looking at modern times, beer is being brewed in almost every country and therefore gives a variety of beers to choose and results in many opinions, which leads to mutliple questions: *Which beer is the best?”,* *Which country has the best reviews?"* and many more. [[4]](#ref4) To try and answer some of these questions, in this article, the beer review dataset from **RateBeer** will be examined by looking at ratings and reviews of beers across breweries and countries. 

## Beer Reviews from Data
The journey of the beer review investigation begins with a dataset from [RateBeer](https://www.ratebeer.com/) provided from the data website [Snap](https://snap.stanford.edu/data/web-RateBeer.html). A dataset containing ~3 million reviews, ~40K users, ~110K beers and more, which has a timespan from April 2000 to November 2011. With multiple attributes and text reviews containing ratings with five aspects, a data story will be developed by investigations of many different aspects across the provided data, to see if locations, breweries sizes, user profiles and many other variables has a connection regarding the final ratings of different beers. Naturally, this makes us unable to make solid comments on which beers are enjoyed the most in year of 2024, though there will still be plenty of ideas one can get about how we all enjoy beer around the world. After all, beer has existed for quite a while!

As to get a better ideas of what beers the common man is likely to drink, we have filtered the data sets to only contain the beers which has been reviewed more than 200 times. This takes away some of the more unique, special beers, but it makes for more interesting analysis later on, as we will not be caught up in a single person having reviewed their favorite, special, niché beer. Firstly, we want to give you an idea of where you might have the best luck finding your new favorite beer and also what country seem most enthusiastic about rating new beer.

## The Breweries
*Insert text here*

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

<div class="l-page">
  <div class="image" id="figure4">
    <img src="/assets/plotly/BelgiumBeerRatings.png">
    <div class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 4: Ratios of Breweries Per Area [KM2].
    </div>
  </div>
  <div class="image" id="figure5">
    <img src="/assets/plotly/NorwayBeerRatings.png">
    <div class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 5: Ratios of Breweries Per Area [KM2].
    </div>
</div>


<div class="l-page">
  <iframe src="{{ '/assets/plotly/breweries_per_area.html' | relative_url }}" frameborder='0' scrolling='no' height="700px" width="1100px" style="border: 0px;"></iframe>
</div>
<div id="figure4" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 4: Ratios of Breweries Per Area [KM2].
</div>

## The Beer Ratings
*Insert text here*


<div class="l-page">
  <iframe src="{{ '/assets/plotly/choropleth_globalrating.html' | relative_url }}" frameborder='0' scrolling='no' height="800px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure5" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 5: Average Ratings of Beers Based on Location of Brewery.
</div>

<div class="l-page">
  <iframe src="{{ '/assets/plotly/choropleth.html' | relative_url }}" frameborder='0' scrolling='no' height="800px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure5" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 5: Average Ratings of Beers Based on Location of Brewery.
</div>

## The Beer Reviews

<div class="l-page">
  <iframe src="{{ '/assets/plotly/Tree_plot.html' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure6" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 6: Top 10 Words in Reviews on Countries' Best and Worst Beers
</div>

## Conclusion

* * *

## References
<a name="ref1">1</a>: Top 10 consumed beverages [https://nawon.com.vn/top-10-worlds-most-consumed-beverage/](https://nawon.com.vn/top-10-worlds-most-consumed-beverage/)

<a name="ref2">2</a>: Who invented beer [https://www.history.com/news/who-invented-beer](https://www.history.com/news/who-invented-beer)

<a name="ref3">3</a>: Where did beer originate from [https://www.brewscruise.com/blog/where-did-beer-originate-from/](https://www.brewscruise.com/blog/where-did-beer-originate-from/)

<a name="ref4">4</a>: Beer in different countries [https://craftbeerme.com/beer-in-different-countries/](https://craftbeerme.com/beer-in-different-countries/)

