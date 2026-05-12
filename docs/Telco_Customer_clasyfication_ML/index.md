## 📊 Customer Churn Prediction

Built and compared two end-to-end machine learning models — Logistic Regression and Gradient Boosting — for customer churn prediction in a telecom dataset, focusing on both interpretability and predictive performance.

## 🔧 Approach

- Logistic Regression with L1 regularization
- Gradient Boosting Classifier
- Threshold tuning to balance recall and precision
- Feature importance analysis and feature reduction experiments
- Cross-validation for model stability evaluation

## 📈 Results

Logistic Regression (L1)

- ROC AUC: ~0.85
- Recall (churn): ~0.68
- Precision (churn): ~0.61

Gradient Boosting

- ROC AUC: ~0.86
- Recall (churn): ~0.68
- Precision (churn): ~0.64

## 💡 Key Insights

Customers with short tenure and month-to-month contracts were significantly more likely to churn.
Gradient Boosting improved the balance between recall and precision while maintaining strong generalization performance.
Removing low-importance features had minimal impact on results, suggesting effective handling of weak predictors by the ensemble model.

## 🔍 Focus

Balancing interpretability, predictive performance, and real-world business usability rather than optimizing for raw accuracy alone.

## 🧠 Learning Outcomes

While tools like PyCaret were useful for rapid experimentation and model comparison, manually building and tuning the pipeline provided a much deeper understanding of:

- feature engineering
- threshold optimization
- ROC AUC interpretation
- business-oriented model evaluation
- ensemble learning and boosting
- trade-offs between recall and precision

This approach provided greater control over model behavior and allowed the final solution to better align with practical business objectives.

🧪 Interactive Playground

The notebook includes a commented testing section that allows running predictions on custom customer profiles.

This makes it possible to:

- modify customer attributes
- compare Logistic Regression and Gradient Boosting predictions
- observe probability changes
- experiment with different churn scenarios

The playground was designed to better understand how model behavior changes depending on customer characteristics and classification thresholds.

**Created on 03.05.2026**

<a href="https://www.kaggle.com/code/emineyetm/telco-customer-churn/input" class="md-button md-button--primary">Ogrinal data set</a>
<a href="https://www.kaggle.com/emineyetm" class="md-button md-button--primary">Author of dataset</a>
<a href="https://krzysztofzakrzewski.github.io/portfolio/Telco_Customer_clasyfication_EDA/" class="md-button md-button--primary">Previus EDA Analis</a>
<a href="https://github.com/KrzysztofZakrzewski/Telco_Customer_clasyfication_ML" class="md-button md-button--primary">GitHub</a>
<br>
<br>
<a href="Telco_Customer_clasyfication_ML.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="data/telco_churn_clean.csv" download class="md-button md-button--primary">Download CSV Data</a>
<a href="clasyfication_model/churn_model_final.pkl" download class="md-button md-button--primary">Download LR Model</a>
<a href="clasyfication_model/gradient_boosting_model.pkl" download class="md-button md-button--primary">Download GB Model</a>

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