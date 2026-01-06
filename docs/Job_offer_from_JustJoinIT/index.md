# Data Analysis EDA of JustJoinIt: Domain Exploration

This is an analysis I carried out as part of a project in the Data Scientist: From Zero to AI course. I have to admit—it really challenged me. It wasn’t exceptionally difficult, but it was demanding and required a lot of careful work.

Could it have been done better?

Yes.

Could the data have been analyzed in even greater detail?

Yes.

Does it still make an impression?

In my opinion—yes.

One of the most interesting things I learned during this project was Cramér’s V matrix. Since the Pearson correlation matrix and its variations did not provide satisfactory results, I was forced to look for an alternative solution.

That’s where Cramér’s V came in. It is used to measure the strength of association between two categorical variables. It is essentially the equivalent of Pearson’s correlation, but designed for categories rather than continuous numerical values.

**Created 06.01.2025**

<a href="justjoinit_old_data_eda.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="https://www.kaggle.com/datasets/jszafranqb/justjoinit-job-offers-data-2021-10-2023-09" download class="md-button md-button--primary">DataSet</a>
<a href="https://www.kaggle.com/jszafranqb" download class="md-button md-button--primary">DataSet Author</a>

<iframe
    id="content"
    src="justjoinit_old_data_eda.html"
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