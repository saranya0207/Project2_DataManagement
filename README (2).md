# 🎬 MovieLens Analytics Pipeline with Apache Spark & Cassandra

> A scalable big data analytics pipeline built using **Apache Spark** and **Apache Cassandra** to process and analyze the MovieLens 100K dataset.

## 📌 Project Overview

This project was developed for **STQD6324 Data Management (Semester 2, 2025/2026)**.

The objective is to design and implement a distributed data processing pipeline capable of ingesting, transforming, storing, and analyzing movie rating data using modern big data technologies.

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

## 🎯 Analytical Tasks

### 1. Average Rating for Each Movie
Calculate the mean rating received by every movie in the dataset.

### 2. Top 10 Highest-Rated Movies
Identify the ten movies with the highest average ratings based on user reviews.

### 3. Favourite Genre Analysis
Determine users who:
- Rated at least 50 movies
- Identify their favourite genre based on the genre they rated most frequently

### 4. Users Below 20 Years Old
Retrieve all users whose age is less than 20.

### 5. Scientists Aged 30–40
Retrieve users:
- Occupation = Scientist
- Age between 30 and 40 years

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Programming Language |
| Apache Spark | Distributed Data Processing |
| Spark SQL | Analytical Queries |
| Apache Cassandra | NoSQL Database |
| HDFS | Distributed Storage |
| Jupyter Notebook | Development Environment |

---

## 📂 Repository Structure

```text
MovieLens-Spark-Cassandra/
│
├── notebook/
│   └── movielens_report.ipynb
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

- Python 3.x
- Apache Spark
- Apache Cassandra
- Java JDK 8+
- Hadoop / HDFS

---

## 🚀 Running the Project

```bash
spark-submit movielens.py
```

Or run the notebook:

```bash
jupyter notebook movielens_report.ipynb
```

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

| Task | Description |
|--------|------------|
| Task 1 | Average rating of every movie |
| Task 2 | Top 10 highest-rated movies |
| Task 3 | Favourite genre analysis for active users |
| Task 4 | Users below age 20 |
| Task 5 | Scientists aged 30–40 |

---

## 🎓 Learning Outcomes

- Distributed data processing using Apache Spark
- RDD and DataFrame transformations
- Spark SQL analytics
- Cassandra integration
- Big data workflow development
- Reproducible data engineering practices

---

## 📚 References

- MovieLens Dataset: https://grouplens.org/datasets/movielens/
- Apache Spark Documentation: https://spark.apache.org/docs/latest/
- Apache Cassandra Documentation: https://cassandra.apache.org/doc/latest/

---

## 👨‍💻 Author

**Sara**  
STQD6324 Data Management  
Semester 2, 2025/2026

⭐ If you find this project useful, feel free to explore further enhancements such as MongoDB or HBase integration.
