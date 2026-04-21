# Coffee Sales Clustering Analysis

This project presents the application of clustering techniques to coffee sales data in order to identify patterns in customer behavior.

The main objectives of the analysis were:

1. to identify customer segments based on purchasing behavior,
2. to examine whether the data contains distinct groups of transactions related to purchase time and price level,
3. to identify key sales hours and recurring purchasing patterns.

Reflections:

The analysis was conducted on data that had previously undergone exploratory data analysis (EDA), which allowed for initial preparation of the dataset for further modeling.

During the earlier analysis, it was observed that the data most likely does not originate from the US market. In particular, the analysis of sales on days corresponding to major US holidays and days off did not show significant deviations compared to other days.

It is therefore possible that the data is synthetic in nature. Nevertheless, clear patterns of customer behavior were identified, especially in the context of time of day and product price levels.

Based on my previous experience in the gastronomy industry, the observed patterns appear to be realistic and consistent with actual customer behavior.

**Created 21.04.2026**

<a href="coffee_ML_EN.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="data/Coffe_sales_ML.csv" download class="md-button md-button--primary">Modified dataset</a>

<a href="https://krzysztofzakrzewski.github.io/portfolio/coffee/" class="md-button md-button--primary">Explore EDA analysis ☕</a>


<a href="https://www.kaggle.com/datasets/navjotkaushal/coffee-sales-dataset" class="md-button md-button--primary">Link to orginal DataSet</a>
<a href="https://www.kaggle.com/navjotkaushal" class="md-button md-button--primary">Link to author of Data</a>

<iframe
    id="content"
    src="coffee_ML_EN.html"
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
