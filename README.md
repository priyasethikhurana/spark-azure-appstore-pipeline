# Big-Data-Analysis-of-App-Store-Applications-Using-Azure-and-Apache-Spark

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Major Steps Followed](#major-steps-followed)
- [Insights and Findings](#insights-and-findings)
- [Conclusion and Further Scope](#conclusion-and-further-scope)

---

## Project Overview
This is a **scalable end-to-end big data pipeline** to analyze **Apple App Store applications** using **Apache Spark**, **Azure Blob Storage**, and **PostgreSQL**.  

The goal was to extract insights about **application categories, pricing strategies, update cadence, and popularity trends**. The entire workflow is **cloud-ready** and can be automated through a batch script.  

![Workflow](Workflow.png)

---

## Data Source
- **Dataset:** Apple App Store Dataset (~1.2M+ rows)  
- **Source:** Kaggle (public dataset)  
- **Format:** CSV uploaded into **Azure Blob Storage**  
- **Features:** App name, category, size, price, ratings, last update, etc.  

![Azure Blob Storage](Azure%20Blobstorage.png)

---

## Major Steps Followed
1. **Dataset Upload** – Uploaded the Apple App Store dataset into **Azure Blob Storage**.  
2. **Spark Ingestion** – Initialized a Spark session and retrieved data directly from Blob.  
   ![Spark Session](Retrived%20Data%20back%20in%20spark%20session.png)  
3. **Data Preprocessing** – Cleaned null values, standardized types, handled outliers.  
4. **Database Storage** – Loaded the curated data into **PostgreSQL** for structured persistence.  
   ![PostgreSQL](Postgres%20SQL.png)  
5. **Data Export** – Extracted PostgreSQL tables into CSV for downstream analysis.  
6. **Exploratory Visualizations** – Created plots using Python/Seaborn and Tableau dashboards.  
7. **Automation** – Built an automated ETL pipeline triggered by a batch script.

---

## Insights and Findings

### 1. Application Size by Category
- **Games, Business, and Education** apps are much larger in size.  
- **Weather and Magazines** are the lightest.  

![App by Size](App%20by%20size.png)

---

### 2. Popularity by Category
- **Weather, Games, and Photo/Video** apps are most popular.  
- **Developer Tools and Food & Drink** apps show the least popularity.  

![App Popularity](App%20popularity%20by%20category.png)

---

### 3. Free vs Paid Applications
- **Free apps** have slightly higher ratings than **Paid apps**.  
- Pricing is not the sole determinant of satisfaction — UX plays a big role.  

![Free vs Paid](Avg%20user%20ratings.png)

---

### 4. Update Cadence by Category
- **Games and Shopping apps** update frequently.  
- **Weather, Magazines, and News apps** update much less often.  

![Update Frequency](Avg%20day%20between%20updates%20.png)

---

## Conclusion and Further Scope
This project demonstrated how **Spark + Azure Blob + PostgreSQL** can handle large-scale app data efficiently. It revealed insights into **app size, pricing, update patterns, and user ratings**.  

**Key Takeaways:**  
- App category and size strongly affect usage and ratings.  
- Free apps attract slightly better ratings than paid ones.  
- Update frequency varies widely across categories.  

**Future Enhancements:**  
- Perform **sentiment analysis** of app reviews with NLP models (BERT, RoBERTa).  
- Extend pipeline to **real-time streaming** using Kafka/Spark Structured Streaming.  
- Add **predictive modeling** for ratings and churn detection.  
- Containerize and orchestrate with **Docker + Airflow** for production.  

---

 **Author:** Priya Sethi Khurana  

