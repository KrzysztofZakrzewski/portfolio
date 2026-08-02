# 📦 Inventory OCR Scanner

A modular OCR-based inventory management system built with Python and Streamlit.

The application automatically extracts products and quantities from invoice or warehouse document images using Optical Character Recognition (OCR), transforms unstructured text into structured inventory data, matches recognized products against a reference catalog, and synchronizes warehouse stock levels.

The project was designed with a modular architecture so that individual components can be easily maintained, extended, or replaced.

---

# 🚀 Project Overview

The application automates inventory updates from photographed documents.

Instead of manually entering products into a warehouse system, the application performs the following steps:

* preprocesses uploaded images
* extracts text using OCR
* cleans and normalizes OCR output
* identifies products and quantities
* matches extracted names against a reference database using fuzzy matching
* transforms extracted data into structured inventory records
* updates inventory quantities stored in SQLite
* presents the results through a Streamlit user interface

The architecture separates business logic, OCR processing, ETL, data persistence, and user interface into independent modules.

---

# ✨ Features

* OCR-based product extraction
* Image preprocessing with OpenCV
* Text extraction using Tesseract OCR
* OCR text normalization and cleanup
* Fuzzy product name matching using RapidFuzz
* ETL pipeline for structured inventory data
* Automatic inventory synchronization
* SQLite-based persistence layer
* Modular application architecture
* Streamlit web interface

---

# 🏗 Architecture

```text
                Streamlit UI
                      │
                      ▼
            OCR Processing Pipeline
                      │
                      ▼
          Text Cleaning & Parsing
                      │
                      ▼
               ETL Processing
                      │
                      ▼
           Product Name Matching
                      │
                      ▼
            Inventory Service Layer
                      │
                      ▼
               SQLite Database
```

Each layer is responsible for a single part of the application, making the project easier to maintain and extend.

---

# 📂 Project Structure

```text
.
├── app.py
├── README.md
│
└── src
    ├── auth
    │   ├── auth.py
    │   ├── password.py
    │   └── session.py
    │
    ├── config
    │   └── config.py
    │
    ├── database
    │   ├── connection.py
    │   ├── inventory_operations.py
    │   ├── inventory_schema.py
    │   ├── reference_schema.py
    │   └── users_schema.py
    │
    ├── etl
    │   ├── etl_pipeline.py
    │   └── ocr_results_to_products_dataframe.py
    │
    ├── procesing_jpg
    │   ├── extract_text_ocr.py
    │   ├── invoice_ocr_pipeline.py
    │   ├── preprocess_ocr.py
    │   └── text_modification.py
    │
    ├── product_matching
    │   └── fuzzy_match.py
    │
    ├── services
    │   └── inventory_service.py
    │
    └── ui
        ├── sidebar.py
        └── upload.py
```

---

# ⚙ Processing Workflow

```text
Image Upload
      │
      ▼
Image Preprocessing
      │
      ▼
OCR Text Extraction
      │
      ▼
Text Cleaning
      │
      ▼
Invoice Parsing
      │
      ▼
ETL Transformation
      │
      ▼
Product Matching
      │
      ▼
Inventory Update
      │
      ▼
SQLite Database
      │
      ▼
Streamlit Interface
```

---

# 📦 Module Overview

### UI

Provides the Streamlit user interface responsible for:

* uploading images
* displaying inventory
* managing user interactions

---

### OCR Pipeline

Responsible for:

* image preprocessing
* OCR execution
* text cleaning
* invoice parsing

The OCR layer has been designed to be replaceable. Tesseract can be substituted with another OCR engine or an LLM-based document extraction pipeline without affecting the remaining application.

---

### ETL

Transforms OCR output into structured inventory records.

Responsibilities include:

* extracting products
* quantity normalization
* duplicate merging
* preparing inventory updates

---

### Product Matching

Maps extracted product names to the reference product database using fuzzy matching.

This improves OCR robustness when invoices contain spelling mistakes, formatting inconsistencies, or OCR artifacts.

---

### Services

Contains business logic separating application behavior from database implementation.

---

### Database

Responsible for:

* inventory persistence
* reference product storage
* user database
* database schema initialization
* inventory synchronization

SQLite is currently used as the storage engine but can be replaced with another relational database.

---

# 🛠 Technologies

* Python
* Streamlit
* OpenCV
* Tesseract OCR
* Pandas
* NumPy
* SQLite
* RapidFuzz

---

# 🚀 Running the Project

```bash
git clone <repository>

cd <repository>

conda env create -f environment.yml

conda activate <environment>

streamlit run app.py
```

---

# 🎯 What I Learned

This project allowed me to gain practical experience with:

* modular Python application architecture
* OCR preprocessing techniques
* image processing with OpenCV
* ETL pipeline design
* fuzzy string matching
* SQLite database integration
* separation of business logic from UI
* Streamlit application development

---

# 🔮 Possible Future Improvements

* PostgreSQL support
* Docker deployment
* REST API using FastAPI
* User authentication and authorization
* Inventory operation history
* Audit logging
* OCR confidence monitoring
* Unit and integration tests
* CI/CD pipeline
* LLM-based document extraction

---

# 🎥 Demo

The project portfolio includes a demonstration presenting:

Part 3 (last):

https://youtu.be/jb9vZLLzAJ4

* image upload
* OCR processing
* product extraction
* inventory synchronization
* application workflow
* modular architecture
