# 🚕 NYC Taxi Trip Duration — Exploratory Data Analysis & ML Data Preparation

## 📌 Project Overview

Comprehensive exploratory data analysis project based on the 2016 NYC Yellow Cab dataset published by the NYC Taxi and Limousine Commission (TLC).

The main objective of the project was to validate data consistency, identify corrupted or unrealistic observations, explore transportation behavior patterns, and prepare a coherent dataset for machine learning regression focused on taxi trip duration prediction.

---

## 🧠 Main Areas of Analysis

- 🌍 Geographic validation and NYC boundary sanity checks
- ⏱️ Datetime validation and trip duration consistency analysis
- 📏 Haversine distance calculation and transportation feature engineering
- 🚦 Speed-based anomaly detection
- 🧹 Outlier detection and corrupted ride filtering
- 📈 Relationship analysis between spatial and temporal features
- 🚕 Passenger and vendor behavior exploration
- 🔗 Correlation analysis for ML preparation

---

## 🎯 Main Goal

The primary goal of the project was not only to clean the dataset, but also to better understand how transportation behavior emerges from spatial and temporal relationships within large-scale urban mobility data.

Special attention was given to preserving realistic NYC traffic variability while removing physically implausible or corrupted observations.

---

## ⚙️ Final Outcome

The final dataset was cleaned, validated, and prepared for machine learning regression tasks focused on taxi trip duration prediction.

The project ultimately evolved into a combination of:
- exploratory data analysis,
- transportation behavior analysis,
- data validation,
- and practical ML-oriented preprocessing.

---

## 📦 Dataset Availability

The original dataset was not included directly in the repository due to its large size.

Please download the dataset manually from Kaggle:

<a href="https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration" class="md-button md-button--primary">Orginal dataset</a>

After downloading, place the dataset inside the project's `data/` directory before running the notebook.

**Created on 17.05.2026**

<a href="NYC_EDA.ipynb" download class="md-button md-button--primary">Download Notebook</a>

<a href="https://www.linkedin.com/in/krzysztof-zakrzewski-206554258/" class="md-button md-button--primary">My linkedin</a>

<a href="https://github.com/KrzysztofZakrzewski/NYC_Taxi_Trip_Duration_ML" class="md-button md-button--primary">Project GitHub</a>


<iframe
    id="content"
    src="NYC_EDA.html"
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