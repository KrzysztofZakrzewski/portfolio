# 📦 OCR Inventory Scanner

A modular inventory management system based on OCR technology, built in Python and Streamlit.

The application automatically extracts products and quantities from invoice images or warehouse documents using optical character recognition (OCR), converts unstructured text into structured inventory data, matches recognized products to a reference catalog, synchronizes inventory levels, and saves order history.

The project was designed based on a modular architecture, allowing individual components to be easily maintained, expanded, or replaced.

--

# 🚀 Project Description

The application automates inventory updates based on photographed documents.

Instead of manually entering products into the inventory system, the application performs the following steps:

* Preprocessing uploaded images
* Text extraction using OCR
* Cleansing and normalizing OCR results
* Identifying products and quantities
* Matching extracted names to a reference database using fuzzy matching
* Transforming extracted data into structured inventory records
* Updating inventory quantities stored in a SQLite database
* Presenting results via the Streamlit user interface

The architecture separates business logic, OCR processing, ETL, data persistence, and the user interface into independent modules.

---

# 🏗 Architecture

Each layer is responsible for a single part of the application, making the project easier to maintain and extend.

---

# 📂 Project Structure

```text
.
├── app.py
└── src
    ├── auth
    │   ├── auth.py
    │   ├── password.py
    │   └── session.py
    ├── config
    │   └── config.py
    ├── customer_matching
    │   └── fuzzy_match_customer.py
    ├── database
    │   ├── baza_probna.db
    │   ├── connection.py
    │   ├── inventory.db
    │   ├── inventory_operations.py
    │   ├── inventory_schema.py
    │   ├── reference.db
    │   ├── reference_operations.py
    │   ├── reference_schema.py
    │   ├── users.db
    │   └── users_schema.py
    ├── etl
    │   ├── etl_pipeline.py
    │   └── ocr_results_to_products_dataframe.py
    ├── procesing_jpg
    │   ├── extract_text_ocr.py
    │   ├── invoice_ocr_pipeline.py
    │   ├── preprocess_ocr.py
    │   └── text_modification.py
    ├── product_matching
    │   └── fuzzy_match.py
    ├── services
    │   ├── analytics_service.py
    │   └── inventory_service.py
    └── ui
        ├── sidebar.py
        └── upload.py

11 directories, 27 files
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
Invoice Section Parsing
      │
      ├─────────────────────┐
      ▼                     ▼
Customer Extraction     Product Line Extraction
      │                     │
      ▼                     ▼
Customer Matching       Text Cleaning
      │                     │
      │                     ▼
      │                Product Extraction
      │                     │
      │                     ▼
      │                Product Matching
      │                     │
      └──────────┬──────────┘
                 ▼
          ETL Transformation
                 │
        ┌────────┴────────┐
        ▼                 ▼
 Inventory Update    Order Creation
        │                 │
        ▼                 ▼
                     Order Items
        └────────┬────────┘
                 ▼
          SQLite Database
                 │
                 ▼
        Streamlit Interface
```


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

# 🎯 What I Learned

This project allowed me to gain practical experience with:

* modular Python application architecture
* OCR preprocessing techniques
* image processing with OpenCV
* ETL pipeline design
* fuzzy string matching
* SQLite database integration
* separation of business logic from UI
* Database preview using LLM
* Inventory operation history

---

# 🔮 Possible Future Improvements

* PostgreSQL support
* Docker deployment
* REST API using FastAPI
* User authentication and authorization
* Audit logging
* OCR confidence monitoring
* Unit and integration tests
* CI/CD pipeline

---

# 🎥 [Demo](https://youtu.be/jb9vZLLzAJ4)  ← Part 4 (last)