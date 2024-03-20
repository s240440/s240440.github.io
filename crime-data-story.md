---
layout: page
title: "The Changing Face of Crime in San Francisco"
permalink: /crime-data-story/
---

<header>
  <h1>{{ page.title }}</h1>
  <p class="byline">An in-depth look at crime trends and their impact on the city.</p>
</header>

<section class="introduction">
  <p>Your introduction goes here. It should hook the reader and provide context for what the article will cover.</p>
</section>

<section class="background">
  <h2>Background</h2>
  <p>This section should provide background information about the SF Crime Data, why it matters, and any relevant details that set the stage for your analysis.</p>
</section>

<section class="main-content">
  <h2>Main Analysis</h2>
  <p>Present the core of your story. Detail the insights you've discovered from the data and what they mean for the reader and the community.</p>

  <!-- Visualization 1: Time-Series or Bar Chart -->
  ![Time Series Chart of Crime Trends](/assets/Calendar.png)

  <!-- Visualization 2: Map -->
  ![Map of Crime in San Francisco](/assets/crime-map.png)

  <!-- Interactive Visualization: Embedding will depend on how you export your Bokeh plot. -->
  <div class="bokeh-plot">
    {{ bokeh.html }}
  </div>

  <p>More narrative, analysis, insights, or stories to elaborate on the data and visuals presented above.</p>
</section>

<section class="conclusion">
  <h2>Conclusion</h2>
  <p>Wrap up your article with a strong conclusion. Summarize your main points and perhaps suggest areas for future research or action.</p>
</section>

<footer class="references">
  <h3>References</h3>
  <ul>
    <li>[Link to data source or related research](#)</li>
    <!-- More references -->
  </ul>
</footer>

<footer class="author-info">
  <h3>About the Author</h3>
  <p>A short bio about you, the author. Include any relevant background and how readers can contact you if they have questions or want to discuss the topic further.</p>
</footer>


