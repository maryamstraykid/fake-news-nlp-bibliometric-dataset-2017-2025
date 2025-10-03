# fake-news-nlp-bibliometric-dataset-2017-2025

This dataset contains 1625 bibliographic records on fake news and misinformation detection research, collected and cleaned for bibliometric analysis. The data covers the period 2017–2025 and was sourced from Scopus, Web of Science, and Google Scholar. Each entry includes detailed metadata such as document type, publication year, authors, title, conference or journal name, DOI, abstract, source database, citation count, keywords, and author affiliations. The dataset spans 8 years of research output and includes a diverse range of document types (journal articles, conference papers, book chapters, and reviews) across multiple disciplines.

The dataset was cleaned to remove incomplete records in essential fields, unify column structures across sources, standardize years, and ensure consistency in keyword fields. Citation counts were retrieved and harmonized using the CrossRef API.
Note: Some non-essential metadata fields may remain incomplete due to variations in source coverage, which is common in aggregated bibliometric datasets.


---

## 📊 Google Colab Notebooks

Two Colab notebooks are included in this repository to make the dataset fully reproducible and easy to explore:  

1. **Data Cleaning & Merging (`data_cleaning_and_merge.ipynb`)**  
   - Adds citation counts to each record  
   - Performs data cleaning depending on the source (Scopus, Web of Science, Google Scholar, IEEE)  
   - Drops unnecessary columns and standardizes column names  
   - Defines a consistent column order and merges all sources using an outer join  
   - Filters incomplete records (missing authors, conference/journal name, abstract, DOI)  
   - Converts the `Year` field into integer format  

2. **Bibliometric Analysis & Visualizations (`bibliometric_analysis_and_visualization.ipynb`)**  
   - Removes duplicates and filters out years with only one publication  
   - Provides descriptive statistics, including:  
     - Total number of publications, unique authors, average docs per author  
     - Time span of the dataset  
     - Compound Annual Growth Rate (CAGR)  
   - Creates bibliometric visualizations such as:  
     - Top authors and most cited authors  
     - Top institutions by publications and citations  
     - Country and city collaborations  
     - Keyword co-occurrence networks and thematic maps  
     - Temporal publication and citation trends  

Both notebooks are designed to run on **Google Colab** with Python 3.11, making them easy to replicate or extend for further analysis.  
