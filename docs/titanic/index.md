# Data Analysis EDA related to the Titanic disaster: Domain Exploration

Welcome to explore my second project of exploratory data analysis (EDA) related to the Titanic disaster.
In this project, besides the data analysis itself, you will also find several technical aspects.

Enjoy!

**Created on 28.08.2025**

<a href="titanic.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="26__titanic.csv" download class="md-button md-button--primary">Download CSV Data</a>

<iframe
    id="content"
    src="titanic.html"
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