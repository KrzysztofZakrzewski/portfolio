# Data Analysis EDA related to the "The 500 richest businessmen in the world"

I invite you to my analysis of the 500 richest people in the world.
The data pertains to the year 2024.

The purpose of this analysis was not just curiosity about how the richest people get wealthy. Honestly, I care little about that.
The goals outlined in the analysis may seem fairly standard, but they can prompt some reflection.
The sums presented in the analysis are extremely unbelievable, even absurd.

This can provoke thought. In my opinion, money is a certain kind of driving force, and the amounts shown here are simply incredible.
Let’s start with an observation that not everyone might realize:

**1,000,000** seconds equals approximately **11.57 days**.  
**1,000,000,000** seconds is roughly **31 years and 8.5 months**!!!


While I can roughly predict what I’ll be doing in two weeks down to the minute, predicting what I’ll be doing in 31 years…  
I can only hope that I’ll still be healthy, young, wealthy, and living my life in a certain way—e.g., training on a mook yan jong. 😊

While I can imagine the legendary “first million,” the “first billion” is quite abstract. It’s not a house with a backyard and a car. It’s infrastructure and ecosystem. It’s on a completely different scale.

Regarding the regions, the original dataset did not meet my expectations. Division into individual countries was too detailed, while a simple division into continents seemed incomplete. It did not give full control over the data.

I divided the countries not only into continents but also into China and India, because, in my opinion, these countries are not only huge, but in their vastness they also represent separate cultures and ecosystems. In China alone, according to the dataset, the number of billionaires is almost equal to the rest of Asia, while in India it is about half compared to China or Asia. You could divide both of these large countries into districts, but they are still vast national agglomerations, in a sense even civilizational. Their populations can already be counted in billions.

I am providing both the original dataset and the version modified by me for analysis. As we can observe, some of the values presented in the data are extreme.

**Created 20.08.2025**  

<a href="top_rich2024_ready.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="top_rich2024_ready.csv" download class="md-button md-button--primary">Dowland Dataset</a>

Author of orginal dataset:

<a href="https://www.kaggle.com/mahmoudredagamail/datasets" download class="md-button md-button--primary">Author of dataset</a> 
<a href="https://www.kaggle.com/datasets/mahmoudredagamail/the-worlds-500-most-powerful-businessmen" download class="md-button md-button--primary">Orginal Dataset</a>




<iframe
    id="content"
    src="top_rich2024_ready.html"
    width="100%"
    style="border:1px solid black;overflow:hidden;"
></iframe>
<script>
function resizeIframeToFitContent(iframe) {
    iframe.style.height = (iframe.contentWindow.document.documentElement.scrollHeight + 50) + "px";
    iframe.contentDocument.body.style["overflow"] = 'hidden';
}
window.addEventListener('load', function() {
    var iframe = document.getElementById('content');
    resizeIframeToFitContent(iframe);
});
window.addEventListener('resize', function() {
    var iframe = document.getElementById('content');
    resizeIframeToFitContent(iframe);
});
</script>