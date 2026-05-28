## 🚕 NYC Taxi Trip Duration Predictor

Interactive Streamlit application for predicting NYC taxi trip duration using trained Random Forest regression models.

The app allows users to select popular NYC landmarks or enter custom coordinates, automatically generates transportation-related features such as trip distance and directional movement, and predicts estimated trip duration in real time.

## 🎥 Demo

- The underlying Random Forest models range from approximately 900 MB to 1.3 GB, making lightweight public deployment impractical for this project. The video demonstrates the complete application workflow and prediction process.

- The demo also includes a comparison between model predictions and Google Maps travel estimates for selected NYC routes.

<a href="https://youtu.be/XkpqzY4AuDw" class="md-button md-button--primary">
▶️ Watch Demo
</a>

## Features:

- 🗺️ Interactive map of popular NYC locations
- 📍 Predefined landmark selection with automatic coordinate filling
- ✏️ Custom pickup and dropoff coordinate input
- 📏 Haversine distance calculation
- 🧭 Bearing calculation
- ⏰ Temporal feature generation
- 🤖 Real-time trip duration prediction

The application was developed as the deployment and demonstration layer for the NYC Taxi Trip Duration machine learning project.

## ⚠️ Note

- The trained models are not distributed with this repository due to their size. To run the application locally, the EDA and ML pipelines must be executed first to generate the required model artifacts.

- Due to model size limitations, trained model files are not distributed with the repository.

- Please refer to the project README for setup and execution instructions.

**Created on 22.05.2026**

<a href="https://www.linkedin.com/in/krzysztof-zakrzewski-206554258/" class="md-button md-button--primary">LinkedIn Profile</a>

<a href="https://github.com/KrzysztofZakrzewski/NYC_Taxi_app" class="md-button md-button--primary">Project GitHub</a>

<a href="https://krzysztofzakrzewski.github.io/portfolio/NYC_EDA/" class="md-button md-button--primary">EDA</a>

<a href="https://krzysztofzakrzewski.github.io/portfolio/NYC_ML/" class="md-button md-button--primary">ML Project<</a>

<a href="https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration" class="md-button md-button--primary">Orginal Dataset</a>