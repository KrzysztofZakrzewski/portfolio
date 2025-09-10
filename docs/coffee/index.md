# Data Analysis EDA of Coffee: Domain Exploration

I present an EDA analysis based on coffee-related data.

My personal goal in this small project, besides performing the analysis itself, was to carry it out on a **Linux** system. The experience had its challenges, but it was not exceptionally difficult.

During this analysis, I explored the differences between time in Python and time in pandas. It can really give you a headache—time is not always equal to time.

Additionally, I decided to answer the question of whether the data comes from the USA, by comparing the results with the expected sales increases or decreases.

It turned out that the data is either synthetic or comes from another region of the world. Where exactly? I don’t know—maybe someday I’ll find the time to find out. 🙂

Enjoy the ☕!

**Created 09.09.2025**

<a href="coffee_eda.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="https://www.kaggle.com/datasets/navjotkaushal/coffee-sales-dataset" download class="md-button md-button--primary">Link to DataSet</a>
<a href="https://www.kaggle.com/navjotkaushal" download class="md-button md-button--primary">Link to author of Data</a>

<iframe
    id="content"
    src="coffee_eda.html"
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
