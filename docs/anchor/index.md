# 📦 Invoice OCR Inventory Scanner

A modular inventory management application that automatically extracts products and quantities from invoice or order images using OCR and updates warehouse stock levels.

The system was designed to process photographed documents, transform unstructured text into structured inventory data, and maintain product quantities in a database.

---

## 🚀 Project Overview

The application allows users to upload invoice or order images, extract product information using OCR, match extracted product names against a predefined product catalog, and update inventory records automatically.

The architecture follows a modular design, making it easy to replace individual components without affecting the rest of the system.

For example:

* Tesseract OCR can be replaced with an LLM-based extraction engine.
* SQLite can be replaced with PostgreSQL.
* The current matching engine can be replaced with more advanced NLP solutions.

---

## 🏗️ Architecture

The application is divided into independent layers:

```text
Image Upload
      │
      ▼
Image Preprocessing
      │
      ▼
OCR Extraction
      │
      ▼
Text Cleaning
      │
      ▼
Product Matching
      │
      ▼
ETL Processing
      │
      ▼
Database Update
      │
      ▼
User Interface
```

This separation allows each component to be developed, tested, and replaced independently.

---

## 📂 Project Structure

```text
.
├── src
│   ├── config
│   │   └── config.py
│   │
│   ├── database
│   │   ├── baza_probna.db
│   │   ├── connection.py
│   │   ├── operations.py
│   │   └── schema.py
│   │
│   ├── etl
│   │   ├── pipeline.py
│   │   ├── products_etl_ocr.py
│   │   └── products_etl.py
│   │
│   ├── procesing_jpg
│   │   ├── extract_text_ocr.py
│   │   ├── preprocess_ocr.py
│   │   └── text_modification.py
│   │
│   ├── product_matching
│   │   ├── correct_products_names.py
│   │   └── fuzzy_match.py
│   │
│   └── ui
│       └── sidebar.py
│
├── app.py
└── README.md
```

---

## ⚙️ Modules

### 🖥️ app.py

Main Streamlit application responsible for:

* image upload
* user interaction
* displaying results
* triggering the OCR pipeline

---

### ⚙️ config

#### config.py

Stores application settings and configuration values such as:

* database paths
* environment variables
* application constants

---

### 🗄️ database

Database layer responsible for inventory persistence.

#### connection.py

Creates and manages database connections.

#### schema.py

Defines database structure and table schemas.

#### operations.py

Handles database operations:

* loading inventory
* updating quantities
* saving processed records

---

### 🖼️ procesing_jpg

Image processing and OCR layer.

#### preprocess_ocr.py

Prepares images for OCR by:

* grayscale conversion
* contrast enhancement
* image cleanup

#### extract_text_ocr.py

Extracts raw text using OCR.

The OCR layer is designed to be replaceable and can be upgraded to use LLM-based document extraction.

#### text_modification.py

Cleans OCR output by:

* removing OCR artifacts
* normalizing text
* preparing text for parsing

---

### 🔄 etl

Responsible for transforming raw OCR results into structured inventory data.

#### pipeline.py

Coordinates the complete processing workflow.

#### products_etl_ocr.py

Converts OCR output into structured product records.

#### products_etl.py

Performs additional transformations and inventory calculations.

---

### 🎯 product_matching

Product name normalization and matching.

#### correct_products_names.py

Maintains the master list of valid products.

#### fuzzy_match.py

Uses fuzzy matching techniques to map OCR output to known product names.

This layer improves OCR robustness when documents contain spelling errors or OCR artifacts.

---

### 🎨 ui

#### sidebar.py

Contains reusable Streamlit user interface components.

---

## 📈 Processing Workflow

1. User uploads an invoice or order image.
2. The image is preprocessed to improve OCR quality.
3. OCR extracts raw text from the document.
4. Text is cleaned and normalized.
5. Product names are matched against the product catalog.
6. Structured inventory data is generated.
7. Database records are updated.
8. Results are displayed in the user interface.

---

## 🛠️ Technologies

* Python
* Streamlit
* OpenCV
* Tesseract OCR
* Pandas
* SQLite
* RapidFuzz
* Pydantic

---

## 🔮 ## 🔮 Possible Future Improvements

* User authentication and authorization
* Audit logging
* OCR confidence monitoring
* LLM-based document extraction
* Multi-user inventory management
* Advanced reporting and analytics

---

## 🎥 Demo

A video presentation of the application can be found in the project portfolio.

The demo showcases:

* image upload
* OCR processing
* product extraction
* inventory updates
* application workflow


**Created 7.06.2026**

<a href="https://youtu.be/GEt1dHeC6sQ" taget="_blank" class="md-button md-button--primary">Demo</a>

