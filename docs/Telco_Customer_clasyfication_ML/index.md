## 📊 Customer Churn Prediction

Built an end-to-end machine learning model to predict customer churn in a telecom dataset.

### 🔧 Approach
- Logistic Regression with L1 regularization
- Threshold tuning to balance recall and precision
- Feature importance analysis for interpretability

### 📈 Results
- ROC AUC: **0.86**
- Recall (churn): **0.68**
- Precision (churn): **0.61**

### 💡 Key Insight
Customers with short tenure and high monthly charges are significantly more likely to churn.

### 🔍 Focus
Interpretability and real-world usability over raw accuracy.

### 🧠 Learning Outcome

While tools like PyCaret are useful for quick model comparison, building the pipeline manually provided a deeper understanding of:

- feature engineering  
- threshold tuning  
- model interpretability  
- trade-offs between recall and precision  

This allowed for more control over model behavior and better alignment with business objectives.

**Created on 03.05.2026**

<a href="https://www.kaggle.com/code/emineyetm/telco-customer-churn/input" class="md-button md-button--primary">Ogrinal data set</a>
<a href="https://www.kaggle.com/emineyetm" class="md-button md-button--primary">Author of dataset</a>
<a href="https://krzysztofzakrzewski.github.io/portfolio/Telco_Customer_clasyfication_EDA/" class="md-button md-button--primary">Previus EDA Analis</a>
<a href="https://github.com/KrzysztofZakrzewski/Telco_Customer_clasyfication_ML" class="md-button md-button--primary">GitHub</a>
<br>
<br>
<a href="Telco_Customer_clasyfication_ML.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="data/telco_churn_clean.csv" download class="md-button md-button--primary">Download CSV Data</a>
<a href="clasyfication_model/churn_model_final.pkl" download class="md-button md-button--primary">Download Final Model</a>

<iframe
    id="content"
    src="Telco_Customer_clasyfication_ML.html"
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