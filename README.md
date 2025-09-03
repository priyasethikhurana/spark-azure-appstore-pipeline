# Big-Data-Analysis-of-App-Store-Applications-Using-Azure-and-Apache-Spark

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Major Steps Followed](#major-steps-followed)
- [Insights and Findings](#insights-and-findings)
- [Conclusion and Further Scope](#conclusion-and-further-scope)

---

## Project Overview
This project builds a **scalable end-to-end big data pipeline** to analyze **Apple App Store applications** using **Apache Spark** integrated with **Azure Blob Storage** and **PostgreSQL**.  

The main aim was to extract insights on **application characteristics, pricing strategies, update patterns, and popularity trends** at scale. By leveraging distributed processing, the pipeline is **automated and cloud-ready**.  

![Pipeline Architecture](assets/pipeline_architecture.png)

---

## Data Source
- **Dataset:** Apple App Store Dataset (~1.2M+ rows)  
- **Source:** Kaggle (public dataset)  
- **Format:** CSV stored in **Azure Blob Storage**  
- **Features:** App name, category, size, price, ratings, last update, etc.  

![Azure Storage](assets/azure_blob_storage.png)

---

## Major Steps Followed
1. Upload raw dataset to **Azure Blob Storage**.  
2. Initialize a **Spark session** with required JARs for Azure and PostgreSQL.  
3. Ingest raw CSV from Blob into Spark DataFrames.  
4. Perform **data preprocessing**: null handling, type casting, outlier detection.  
5. Store curated datasets into **PostgreSQL** tables.  
6. Export PostgreSQL tables into CSV format for downstream tasks.  
7. Use **Python (matplotlib/seaborn)** for exploratory visualizations.  
8. Build an interactive **Tableau dashboard** for combined insights.  
9. Automate the entire ETL pipeline using a batch script (`.sh` / `.bat`).  

![PostgreSQL Database](assets/postgres_query.png)  
![Azure <-> Spark](assets/azure_spark_connection.png)

---

## Insights and Findings

### 1. Application Size by Category
- Games, Business, and Education apps are significantly larger in size.  
- Weather and Magazines apps tend to be lightweight.  

![App Size Treemap](assets/app_size_treemap.png)

---

### 2. Popularity by Category
- Weather, Games, and Photo/Video apps are among the most popular.  
- Developer Tools and Food-related apps see lower engagement.  

![Category Popularity](assets/app_popularity.png)

---

### 3. Free vs Paid Applications
- Free apps generally receive **slightly higher ratings** than paid apps.  
- Indicates that **pricing is not the only determinant** of user satisfaction.  

![Free vs Paid Ratings](assets/free_vs_paid.png)

---

### 4. Update Cadence Across Categories
- Games and Shopping apps are updated more frequently.  
- Weather, News, and Magazines show longer gaps between updates.  

![Update Frequency](assets/update_frequency.png)

---

## Conclusion and Further Scope
This project successfully deployed a **cloud-based, automated big data pipeline** for analyzing App Store applications. By combining **Azure Blob Storage, Apache Spark, PostgreSQL, Python, and Tableau**, it demonstrated scalable data engineering in action.  

**Key Takeaways:**  
- App size and category strongly influence usage and ratings.  
- Free apps enjoy higher ratings, but user experience matters more than cost.  
- Update frequency varies widely — stability and engagement differ by category.  

**Future Enhancements:**  
- Integrate **NLP-based sentiment analysis** of app reviews.  
- Extend pipeline with **real-time streaming** (Kafka, Spark Structured Streaming).  
- Add **predictive modeling** for rating forecasts or churn detection.  
- Deploy with **Docker + Airflow** for production orchestration.  

---

👩‍💻 **Author:** Priya Sethi Khurana  
🎓 MSc Data Analytics — National College of Ireland  
