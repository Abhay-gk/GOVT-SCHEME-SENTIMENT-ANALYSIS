# 📊 Tracking Public Pulse on Indian Government Schemes through Social Media Data

## 📝 Introduction
In the digital age, citizens frequently share opinions on government schemes via **social media** and **news platforms**.  
These sources produce large amounts of unstructured text that, when analyzed, can reveal **public sentiment** and **key discussion themes**.

This project implements a **scalable Big Data pipeline** to:
- Extract news and social media data on major Indian government initiatives like **Digital India**, **PM-KUSUM**, **Ayushman Bharat**, and more.
- Process and classify sentiment using **PySpark** and **pretrained deep learning models**.
- Store, analyze, and visualize the results for **policy feedback**, **media analytics**, and **research purposes**.

---

## 🎯 Objectives
- Build a scalable pipeline for analyzing public sentiment on Indian government schemes.
- Extract real-time data from **NewsAPI** and **Reddit API**.
- Preprocess and clean text using **Spark NLP** (tokenization, lemmatization).
- Classify sentiment (Positive, Negative, Neutral) using **pretrained deep learning models**.
- Perform analytics: word cloud generation, clustering, and **topic modeling** (LDA).
- Store data in **MongoDB Atlas** and **HDFS** for efficient access.
- Visualize sentiment distribution and trends.

---

## 🔍 Methodology

### 1️⃣ Data Collection
- **NewsAPI**: Fetch English-language news articles for each scheme via keywords.
- **Reddit**: Scrape posts and top-level comments from subreddits like `r/India`, `r/indianews`, `r/politics` using **AsyncPRAW**.

### 2️⃣ Text Preprocessing & Sentiment Classification
- Clean text: remove stopwords, URLs, and special characters.
- Tokenize and lemmatize with **Spark NLP**.
- Convert text to vectors using **Universal Sentence Encoder (USE)**.
- Classify sentiment using **sentimentdl_use_twitter** pretrained model.

### 3️⃣ Storage & Processing
- Store cleaned & labeled data in **MongoDB Atlas** for query & dashboard access.
- Save preprocessed text in **HDFS** for batch analysis.
- Apply **MapReduce** to compute word frequencies for **word clouds**.

### 4️⃣ Analytics & Visualization
- **K-Means Clustering** to group schemes by sentiment trends.
- **LDA Topic Modeling** to extract discussion themes.
- Visualize results using **Matplotlib**, **Seaborn**, and **WordCloud**.

---

## 📊 Key Outcomes
- Processed **1000+ news articles** and **900+ Reddit comments**.
- **Sentiment Distribution**:
  - **News**: ~67% Positive → highlighting digital growth & reforms.
  - **Reddit**: ~71% Negative → reflecting public concerns on implementation gaps.
- Generated **word clouds** for positive and negative sentiments per scheme.
- Clustered schemes into **three sentiment-based categories**.
- Extracted and labeled top discussion topics such as:
  - *Digital Economy*
  - *Government Schemes Implementation*
  - *Government Schemes and Budget*

---

## 🛠 Tools & Technologies
**Programming:** Python 3.10+, Shell scripting  
**Big Data:** PySpark, Spark ML, Spark NLP, Apache Hadoop (HDFS, MapReduce)  
**Databases:** MongoDB Atlas (NoSQL), HDFS  
**APIs:** NewsAPI.org, Reddit API (AsyncPRAW)  
**Visualization:** Matplotlib, Seaborn, WordCloud  
**NLP Models:** Universal Sentence Encoder, sentimentdl_use_twitter  
**ML Algorithms:** K-Means, LDA (Latent Dirichlet Allocation)  
**Environment:** Google Colab (cloud-based development)

---


