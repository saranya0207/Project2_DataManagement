# 🎬 MovieLens Analytics Pipeline with Apache Spark & Cassandra

## 📌 Project Overview

The objective is to design and implement a distributed data processing pipeline capable of ingesting, transforming, storing and analyzing movie rating data using modern big data technologies.

The pipeline leverages:

- Apache Spark for distributed data processing
- Apache Cassandra for NoSQL data storage
- Python for data engineering and analytics
- Spark SQL and Cassandra Query Language (CQL) for querying

Dataset: **MovieLens 100K**

Source: https://grouplens.org/datasets/movielens/

---

## 🏗️ System Architecture

```text
MovieLens Dataset
(u.user, u.data, u.item)
          │
          ▼
        HDFS
          │
          ▼
      Spark RDDs
          │
          ▼
   Spark DataFrames
          │
          ▼
 Data Cleaning & Processing
          │
          ▼
   Spark SQL Analytics
          │
          ▼
     Cassandra DB
          │
          ▼
 Validation & Reporting
```

---

## 📂 Repository Structure

```text
MovieLens-Spark-Cassandra/
├── scripts/
│   └── movielens.py
├── screenshots/
├── dataset/
│   ├── u.data
│   ├── u.item
│   └── u.user
└── README.md
```

---

## ⚙️ Environment Setup

### Prerequisites

| Component | Version |
|------------|------------|
| Python | 2.7.5 |
| Apache Spark | 2.3.0.2.6.5.0-292 |
| Apache Cassandra | 3.0.9 |
| Hadoop / HDFS | Hadoop Distributed File System (HDFS) |

---

## 🔄 Workflow

1. Load MovieLens data into HDFS
2. Create Spark RDDs from raw files
3. Convert RDDs into Spark DataFrames
4. Perform data cleaning and preprocessing
5. Execute analytical queries using Spark SQL
6. Store processed results in Cassandra
7. Validate data by reading Cassandra tables back into Spark
8. Present results and interpretations

---

## 📈 Results Summary

1. Task 1 : Average rating of every movie
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/5b4db88a-044d-4c15-8418-8de8c0992264" />

2. Task 2 : Top 10 highest-rated movies 
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/e90bfc50-75dd-4082-a265-d7d89df51dcc" />

3. Task 3 : Favourite genre analysis for active users
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/a22c7d0d-d715-440b-a06f-062de549bb8f" />

4. Task 4 : Users below age 20 
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/343428d5-0680-439e-a8fe-0f71013cd4f1" />

5. Task 5 : Scientists aged 30–40 
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/8249c34c-bb8d-46b3-999d-306f6b38a51c" />

---
## Conclusion

This project successfully demonstrated the use of Apache Spark and Apache Cassandra to build a scalable data analytics pipeline using the MovieLens 100K dataset. The dataset was loaded, transformed, and analyzed through Spark RDDs and DataFrames, while Cassandra was used for efficient storage and retrieval of processed data. The analytical tasks, including movie rating analysis, user profiling, and genre preference identification, were successfully completed. Overall, the project highlights the effectiveness of big data technologies in processing large datasets and generating meaningful insights from user and movie rating data.
