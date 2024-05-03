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
Humans consume many different kinds of beverages through life, where the alcoholic beverage, beer, is among the top 10 most consumed beverages across the world. A diverse beverage that brings many people pleasure through life, comes in different colors and offers different tastes. [[1]](#ref1) Besides being a top consumed beverage, it is also known for being one of the oldest human-produced beverages, originating more than 5000 years ago and was done by the Sumerians of the ancient Mesopotamia. [[2]](#ref2) While it originates many years back, the commercial brewing as known today, began in the 13th century in Germany, England and Austria. [[3]](#ref3) Looking at modern times, beer is being brewed in almost every country and therefore gives a variety of beers to choose and results in many opinions, which leads to the question: *”Which beer is the best?”*. [[4]](#ref4) To answer this question, in this article, the beer review dataset from **RateBeer** will be examined by looking at ratings and reviews of beers across breweries and countries. 

## Beer Reviews from Data
*Insert text here*

## Top Rated Beer
*Insert text here*

<div class="l-page" style="max-width: 100%;">
  <img src="{{ '/assets/plotly/Top10RatedBeers.png' | relative_url }}" frameborder='0' scrolling='yes' height="600px" width="100%" style="border: 0px">
</div>
<div id="figure1" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 1: Top 10 rated beers based on average rating.
</div>


## The Countries
*Insert text here*

<div class="l-page" style="max-width: 100%;">
  <img src="{{ '/assets/plotly/Top10Locations.png' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px">
</div>
<div id="figure2" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 2: Top 10 locations based on number of beer reviews.
</div>

<div class="l-page" style="max-width: 100%;">
  <img src="{{ '/assets/plotly/Bottom10Locations.png' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px">
</div>
<div id="figure3" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 3: Bottom 10 locations based on number of beer reviews.
</div>

## The Breweries 
*Insert text here*

<div class="l-page" style="max-width: 100%;">
  <img src="{{ '/assets/plotly/Top10Breweries.png' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px">
</div>
<div id="figure4" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 4: Top 10 locations based on number of active breweries.
</div>

<div class="l-page" style="max-width: 100%;">
  <img src="{{ '/assets/plotly/Bottom10Breweries.png' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px">
</div>
<div id="figure4" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 5: Bottom 10 locations based on number of active breweries.
</div>

## Test for image slider

<ul class="bxslider">
  <li><img src="/assets/plotly/Bottom10Breweries.png" /></li>
  <li><img src="/assets/plotly/Top10Breweries.png" /></li>
  <li><img src="/assets/plotly/Bottom10Locations.png" /></li>
  <li><img src="/assets/plotly/Top10Locations.png" /></li>
</ul>

$(document).ready(function(){
  $('.bxslider').bxSlider();
});

## Test for HTML

<div class="l-page">
  <iframe src="{{ '/assets/plotly/XXXX.html' | relative_url }}" frameborder='0' scrolling='no' height="600px" width="100%" style="border: 0px;"></iframe>
</div>
<div id="figure6" class="caption" style="text-align: center; font-size: 0.8em;">
    Figure 6: Template
</div>

## Conclusion

* * *

## References
<a name="ref1">1</a>: Top 10 consumed beverages [https://nawon.com.vn/top-10-worlds-most-consumed-beverage/](https://nawon.com.vn/top-10-worlds-most-consumed-beverage/)

<a name="ref2">2</a>: Who invented beer [https://www.history.com/news/who-invented-beer](https://www.history.com/news/who-invented-beer)

<a name="ref3">3</a>: Where did beer originate from [https://www.brewscruise.com/blog/where-did-beer-originate-from/](https://www.brewscruise.com/blog/where-did-beer-originate-from/)

<a name="ref4">4</a>: Beer in different countries [https://craftbeerme.com/beer-in-different-countries/](https://craftbeerme.com/beer-in-different-countries/)

