# GitHub AI Repositories Analysis

## Krzysztof Zakrzewski

This project explores the open-source Artificial Intelligence ecosystem by analyzing repositories collected directly from the GitHub REST Search API. The objective was to build a complete data analysis workflow—from automated data collection to data validation, preprocessing, and exploratory data analysis (EDA).

To create the dataset, I developed a custom data collection pipeline that queried 20 AI-related GitHub topics, including Machine Learning, Deep Learning, Large Language Models (LLMs), Computer Vision, Natural Language Processing (NLP), PyTorch, TensorFlow, Generative AI, and Retrieval-Augmented Generation (RAG). Up to 1,000 repositories were collected for each topic before removing duplicate repositories based on their unique GitHub repository ID.

During the project, I identified and resolved several real-world data quality issues, including duplicate repositories, inconsistent API responses, missing values, and schema inconsistencies. The final dataset was cleaned, standardized, and prepared for exploratory data analysis.

The analysis investigates programming language trends, repository popularity, software licenses, repository ownership, GitHub Discussions, and AI topic distributions through statistical summaries and visualizations.

## Key Skills Demonstrated

* Data collection using the GitHub REST API
* REST API integration
* Data validation and preprocessing
* Data cleaning
* Handling missing values and duplicate records
* Feature engineering
* Exploratory Data Analysis (EDA)
* Data visualization
* Git and GitHub workflow
* Technical documentation

## Technologies

* Python
* Pandas
* Requests
* Matplotlib
* Seaborn
* Plotly
* GitHub REST API
* Jupyter Notebook


**Created 7.07.2026**

<a href="Github_clean_EDA.ipynb" download class="md-button md-button--primary">Download Notebook</a>
<a href="data/processed/github_ai_repositories_clean.csv" download class="md-button md-button--primary">Download Clen Data</a>

The GitHub repository contains both the custom data collection scraper and the pre-analysis notebook used to prepare the dataset for exploratory data analysis as well as analysis.

<a href="https://github.com/KrzysztofZakrzewski/github-ai-analusis" class="md-button md-button--primary">GitHub</a>


<iframe
    id="content"
    src="Github_clean_EDA.html"
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