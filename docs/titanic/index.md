# Analiza Danych EDA dotycząca katastrofy Titanica: Eksploracja Domenowa

Zapraszamy do zapoznania się z moim drógim projektem eksploracyjnej analizy danych EDA, dotyczący katastrofy Titanica. W tym projekcie oprócz samej analizy danych znajdóje się również kilka aspektów technicznych.

Zapraszam

**utworzono 28.08.2025**

<a href="titanic.ipynb" download class="md-button md-button--primary">Pobierz Notebook</a>
<a href="26__titanic.csv" download class="md-button md-button--primary">Pobierz dane</a>

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