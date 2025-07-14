# Cancer Tumor Board Information Detection

This project contains an algorithm designed to analyze HTML pages and determine if they contain information related to cancer tumor boards. The goal is to classify web pages into categories based on the relevance of tumor board discussions.

## Project Overview

The core task is to build a classification algorithm that takes an HTML page as input and predicts whether it discusses cancer tumor boards. A "tumor board" is defined as a consilium of doctors from different disciplines discussing cancer cases.

The project outputs a `submission.csv` file for test data with document IDs and predictions, along with a Jupyter notebook detailing the methodology.

## Project Structure
.
├── Keyword_Detection.ipynb

├── datasets/

│   ├── train.csv

│   ├── test.csv

│   ├── keyword2tumor_type.csv

│   └── htmls/

│       ├── 0.html

│       ├── 1.html

│       └── ... (other html files)

├── requirements.txt

└── README.md

└── .gitignore

## Features

* **HTML Parsing:** Extracts text content from raw HTML files.
* **Text Preprocessing:** Cleans and normalizes text data, including lowercasing, punctuation removal, stopword removal, and stemming.
* **Feature Engineering:** Utilizes TF-IDF (Term Frequency-Inverse Document Frequency) vectorization to convert text into numerical features.
* **Machine Learning Models:** Explores various classification algorithms, including:
    * Logistic Regression
    * Complement Naive Bayes
    * Random Forest Classifier
    * Support Vector Machine (SVM)
* **Model Evaluation:** Provides insights into model performance through metrics like accuracy and classification reports.

## Data

The project utilizes the following datasets:
* `train.csv`: Training data containing document URLs, IDs, and labels indicating tumor board relevance.
* `test.csv`: Test data for making predictions.
* `keyword2tumor_type.csv`: A mapping of keywords to tumor types.
* `htmls/`: A directory expected to contain raw HTML files referenced by `doc_id`.

The training dataset consists of 100 documents, and the test set contains 48 documents. Tumor board labels are categorized as:
* **Label 1 (No Tumor Board mention):** 32 documents
* **Label 2 (Tumor Board mentioned but not main focus):** 59 documents
* **Label 3 (Document dedicated to tumor boards):** 9 documents

## Usage

Place your train.csv, test.csv, keyword2tumor_type.csv files, and the htmls directory within a datasets/ folder in the project root.

Open the Keyword_Detection.ipynb Jupyter notebook.

Run all cells in the notebook to preprocess data, train models, evaluate their performance, and generate the submission.csv file for the test data.

The notebook also provides detailed answers to questions regarding data handling, feature engineering, model selection, validation, metrics, expected performance, and potential improvements.

## Installation

To set up the project environment, clone the repository and install the required dependencies:

```bash
git clone <repository-url>
cd <repository-name>
pip install -r requirements.txt
