# Inverted Index Search Engine

## Overview

This project is a scalable **Search Engine** designed to index large document collections using the **MapReduce** framework. It supports real-time querying through a **REST API** and ranks results using **TF-IDF** and **PageRank** scoring algorithms. The goal is to provide fast, relevant, and ranked search results across a large corpus of documents, such as a Wikipedia dataset.

---

## Key Features

- **Scalable Indexing with MapReduce**  
  Uses distributed processing to build inverted indexes efficiently from large datasets. This allows the system to scale beyond the limitations of single-machine processing.

- **TF-IDF Based Ranking**  
  Ranks documents based on term frequency-inverse document frequency (TF-IDF) to prioritize the most relevant results for user queries.

- **PageRank Scoring**  
  Enhances ranking by incorporating link-based popularity using the PageRank algorithm, which improves the relevance of authoritative documents.

- **REST API for Querying**  
  Provides a simple HTTP API to handle search queries and return ranked results, making it easy to integrate into web interfaces or other applications.

- **Web-Based Search Interface**  
  Includes a user-friendly web interface where users can submit queries and view ranked search results in real-time.

---

## Architecture

1. **Document Ingestion**  
   Documents are processed to extract textual content, tokenize terms, and prepare them for indexing.

2. **Inverted Index Construction**  
   The MapReduce framework processes tokenized documents to create an inverted index, mapping each term to the list of documents containing it.

3. **TF-IDF and PageRank Calculation**  
   - **TF-IDF** quantifies the importance of terms in documents relative to the entire corpus.  
   - **PageRank** scores documents based on their link structure to boost authoritative content.

4. **Query Processing**  
   User queries are matched against the inverted index. Relevant documents are scored using TF-IDF and PageRank and then returned in ranked order.

5. **REST API & Web Interface**  
   A Flask-based API serves the ranked results. The web interface connects to this API, allowing users to perform searches and view results interactively.

---

## Intended Use Cases

- Building custom search solutions for document-heavy platforms.
- Academic or research projects exploring information retrieval techniques.
- Educational demonstration of scalable indexing and ranking algorithms.
- Prototyping search-based features for web or data applications.

---

## How It Works 

1. **Prepare Data**  
   Load your document collection (e.g., Wikipedia pages).

2. **Run Indexing Pipeline**  
   Process the data using MapReduce to build the inverted index and calculate rankings.

3. **Start the Search Server**  
   Launch the REST API and web interface to begin accepting search queries.

4. **Search and Retrieve Results**  
   Users enter queries through the web interface and receive ranked results based on content relevance and link authority.

---

## Technologies Used

- **Python** – Core language for processing and server logic.
- **MapReduce Framework** – Distributed processing model for building the inverted index.
- **Flask** – Lightweight web framework for the REST API and search interface.
- **TF-IDF and PageRank Algorithms** – Industry-standard ranking methods.
- **HTML/CSS** – User-facing web interface.

---

## Limitations

- Designed as a prototype; not optimized for production-scale deployment without further performance tuning.
- Ranking quality depends on dataset size, structure, and completeness.
- Requires pre-processing of documents to strip unwanted content
