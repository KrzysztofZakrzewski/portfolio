# 📊 Customer Churn – Exploratory Data Analysis (EDA)

## 🧠 Project Overview

This project focuses on performing **exploratory data analysis (EDA)** on a customer churn dataset.
The goal was to understand the structure of the data, identify key patterns, and uncover relationships between features and customer churn.

Rather than generating excessive visualizations, the analysis was focused on **extracting meaningful insights relevant for modeling and business decisions**.

---

## ⚙️ Analysis Scope

The analysis included:

* Data structure inspection
* Data cleaning and type correction
* Distribution analysis of key variables
* Feature engineering (binning)
* Relationship analysis between features and churn

---

## 🔍 Data Quality & Preparation

* Verified missing values
* Converted `TotalCharges` from object to numeric
* Identified a small number of missing values after conversion
* Confirmed overall data consistency

📌 Insight:

> The dataset was relatively clean and required minimal preprocessing.

**Created on 03.05.2026**

<a href="https://www.kaggle.com/code/emineyetm/telco-customer-churn/input" class="md-button md-button--primary">Ogrinal data set</a>
<a href="https://www.kaggle.com/emineyetm" class="md-button md-button--primary">Author of dataset</a>
<br>
<br>
<a href="Telco_Customer_clasyfication_EDA.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="data/WA_Fn-UseC_-Telco-Customer-Churn.csv" download class="md-button md-button--primary">Download CSV Data</a>

<iframe
    id="content"
    src="Telco_Customer_clasyfication_EDA.html"
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