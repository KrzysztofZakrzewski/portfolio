# 🚕 NYC Taxi Trip Duration Prediction ML

## 🤖 Machine Learning Regression Project

### 📌 Project Overview

Developed an end-to-end machine learning regression pipeline for predicting NYC taxi trip duration using the 2016 NYC Yellow Cab dataset published by the NYC Taxi and Limousine Commission (TLC).

The project combined:

* Exploratory Data Analysis (EDA)
* Spatial and temporal validation
* Feature engineering
* Regression modeling with PyCaret and Scikit-learn
* Model evaluation and feature importance analysis

The repository contains two separate notebook workflows:

* Full-scale workflow using the original 1.4 million record dataset
* Optimized workflow using a representative 200k subset for faster experimentation and improved reproducibility

Both workflows produced highly similar predictive performance and feature importance distributions.

---

## 🛠️ Key Responsibilities

* Performed large-scale EDA and transportation pattern analysis
* Validated geographic consistency of NYC taxi coordinates
* Removed outliers, corrupted rides, and data leakage sources
* Engineered spatial and temporal machine learning features
* Built and compared multiple regression models using PyCaret
* Implemented and tuned a final Random Forest regression pipeline
* Evaluated feature importance and model stability across datasets
* Created an interactive prediction playground for custom inference testing

---

## ⚙️ Feature Engineering

Implemented several domain-oriented features to improve predictive performance:

### 🗺️ Spatial Features

* Haversine trip distance (`distance_km`)
* Directional movement (`bearing`)

### ⏰ Temporal Features

* `pickup_hour`
* `pickup_weekday`
* `pickup_month`
* `is_weekend`

### 🔄 Cyclic Time Encoding

* `hour_sin`
* `hour_cos`

These features allowed the model to better capture traffic cycles, congestion patterns, and directional transportation behavior within NYC.

---

## 📈 Machine Learning Results

### 🚀 Baseline Models

Initial regression models achieved approximately:

* `R² ≈ 0.13`

### 🏆 Final Random Forest Model

After feature engineering and tuning:

* MAE ≈ 184 seconds
* RMSE ≈ 273 seconds
* R² ≈ 0.80

The difference between the original 1.4M dataset and the optimized 200k subset remained minimal, confirming strong statistical consistency and dataset representativeness.

---

## 🔍 Key Findings

* Spatial features were significantly more important than categorical transportation variables
* `distance_km` was the dominant predictive feature
* Directional movement (`bearing`) substantially improved prediction quality
* Temporal cyclic encoding greatly improved model interpretability
* Feature engineering contributed more to model performance than increasing model complexity alone (should be uncommented)

---

## 🧰 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* PyCaret
* Jupyter Notebook

---

## 🖥️ Computational Considerations

Large-scale experiments on the full 1.4 million record dataset achieved strong predictive performance but were highly resource-intensive.

The optimized 200k workflow maintained nearly identical model quality while significantly improving experimentation speed, reproducibility, and computational efficiency.


## 📦 Dataset Availability

The repository includes my custom cleaned and optimized 200k dataset version instead of the original 1.4 million record dataset in order to improve reproducibility and reduce repository size.

<a href="https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration" class="md-button md-button--primary">Orginal dataset</a>


<a href="data_sample/NYC_200K_sampled.csv" class="md-button md-button--primary">Modified sample data set</a>

After downloading, place the dataset inside the project's `data_sample/` directory before running the notebook.

**Created on 22.05.2026**

<a href="NYC_ML_200K_sample.ipynb" download class="md-button md-button--primary">Download Notebook</a>

<a href="https://www.linkedin.com/in/krzysztof-zakrzewski-206554258/" class="md-button md-button--primary">My linkedin</a>

<a href="https://github.com/KrzysztofZakrzewski/NYC_Taxi_Trip_Duration_ML" class="md-button md-button--primary">Project GitHub</a>


<iframe
    id="content"
    src="NYC_ML_200K_sample.html"
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