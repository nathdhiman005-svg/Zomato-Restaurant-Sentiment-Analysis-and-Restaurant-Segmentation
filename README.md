# 🍽️ Zomato Restaurant Sentiment Analysis and Restaurant Segmentation

## 📌 Project Overview

This project focuses on analyzing restaurant reviews and restaurant metadata from Zomato to extract meaningful business insights using Data Analysis, Natural Language Processing (NLP), Machine Learning, and Clustering techniques.

The project consists of two major components:

### 1. Restaurant Sentiment Analysis

A Natural Language Processing (NLP) based classification model that predicts whether a customer review is:

* Positive
* Neutral
* Negative

### 2. Restaurant Segmentation

An Unsupervised Machine Learning model that groups restaurants into meaningful business segments based on restaurant characteristics such as:

* Cost for Two
* Cuisine Diversity
* Collection Count

The project includes complete data preprocessing, exploratory data analysis (EDA), feature engineering, sentiment classification, clustering analysis, model evaluation, and deployment-ready machine learning pipelines.

---

## 🎯 Objectives

### Restaurant Sentiment Analysis

* Analyze customer reviews and feedback.
* Classify reviews into Positive, Neutral, and Negative sentiments.
* Understand customer satisfaction patterns.
* Build a production-ready sentiment prediction model.

### Restaurant Segmentation

* Identify different restaurant segments.
* Understand pricing and cuisine diversity patterns.
* Group similar restaurants together using clustering techniques.
* Build a deployment-ready clustering model.

---

## 📊 Dataset Information

The project uses two datasets:

### 1. Zomato Restaurant names and Metadata.csv

Contains restaurant-level information such as:

* Restaurant Name
* Cost for Two
* Cuisine Types
* Collections
* Timings
* Other restaurant metadata

### 2. Zomato Restaurant reviews.csv

Contains customer review information such as:

* Review Text
* Rating
* Review Time
* Reviewer Information
* Other review-related metadata

These datasets are used for:

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Sentiment Analysis
* Restaurant Segmentation

---

## 🔍 Exploratory Data Analysis (EDA)

The project includes extensive exploratory data analysis covering:

### Univariate Analysis

* Distribution of Restaurant Cost
* Distribution of Cuisine Types
* Distribution of Ratings
* Distribution of Review Lengths
* Distribution of Reviewer Followers
* Distribution of Sentiment Labels

### Bivariate Analysis

* Cost vs Average Rating
* Top Cuisines by Average Rating
* Collection Count vs Average Rating
* Top Restaurants by Average Rating
* Review Length vs Rating
* Reviewer Influence Analysis
* Additional Restaurant Performance Comparisons

### Multivariate Analysis

* Correlation Heatmap
* Restaurant Segmentation using Clustering

---

## ⚙️ Feature Engineering

### Restaurant Features

* Cost_log
* cuisine_count
* collection_count_log

### Review Features

* review_length
* reviewer_follower_count
* reviewer_review_count

### Text Processing

* Text Cleaning
* Lowercasing
* Tokenization
* Stopword Removal
* TF-IDF Vectorization

---

## 🤖 Machine Learning Models

### 1. Restaurant Sentiment Analysis

#### Model Used

* Logistic Regression

#### Text Vectorization

* TF-IDF Vectorizer

#### Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score

#### Final Deployment Model

**RestaurantSentimentPipeline.joblib**

This pipeline combines:

* TF-IDF Vectorizer
* Logistic Regression Classifier

into a single deployment-ready file.

#### Example

Input:

"The food was amazing and the service was excellent."

Output:

"Positive"

---

### 2. Restaurant Segmentation

#### Clustering Algorithm

* K-Means Clustering

#### Input needed for this ML model
* cost
* collection_count
* cuisine_count

it will automatically convert it into desired input for model.
#### Features Used

* Cost_log
* cuisine_count
* collection_count_log

#### Cluster Evaluation

* Elbow Method
* Silhouette Score

#### Final Number of Clusters

K = 4

#### Business Segments

**Cluster 0**

* Ultra Budget-Friendly Specialized Restaurants

**Cluster 1**

* Premium Diverse Restaurants

**Cluster 2**

* Premium High-Visibility Restaurants

**Cluster 3**

* Mid-Range Mainstream Restaurants

#### Final Deployment Model

**RestaurantClusteringPipeline.joblib**

The clustering pipeline automatically performs:

* Log Transformation
* Feature Scaling
* Cluster Prediction

and returns the appropriate business segment for new restaurants.

---

## 📈 Model Performance

### Sentiment Analysis Model

**Logistic Regression + TF-IDF**

Performance:

* Accuracy: ~81%
* Precision (Weighted): ~78%
* Recall (Weighted): ~81%
* F1 Score (Weighted): ~79%

The model demonstrated strong performance in classifying restaurant review sentiments.

---

### Clustering Model

**K-Means Clustering**

Performance:

* Number of Clusters: 4
* Silhouette Score: ~0.365

K-Means performed slightly better than Hierarchical Clustering and was selected as the final restaurant segmentation model.

---

## 📂 Repository Structure

```text
.
├── Zomato Restaurant names and Metadata.csv
├── Zomato Restaurant reviews.csv
├── RestaurantClusteringPipeline.joblib
├── RestaurantSentimentPipeline.joblib
├── Zomato_Restaurant_Sentiment_Analysis_and_Restaurant_Segmentation.ipynb
├── requirements.txt
└── README.md
```

---

## 🚀 Quick Start

### Clone Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 💡 Using the Pretrained Models

This repository already includes trained machine learning models.

You do not need to run the notebook to use them.

### Sentiment Analysis Model

```python
import joblib

sentiment_model = joblib.load("RestaurantSentimentPipeline.joblib")
```

### Restaurant Segmentation Model

```python
import joblib

clustering_model = joblib.load("RestaurantClusteringPipeline.joblib")
```

---

## 📒 Notebook

The notebook:

```text
Zomato_Restaurant_Sentiment_Analysis_and_Restaurant_Segmentation.ipynb
```

contains:

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Hypothesis Testing
* Sentiment Analysis
* Restaurant Segmentation
* Model Evaluation
* Pipeline Creation
* Deployment Testing

Running the notebook from start to finish will recreate:

```text
RestaurantSentimentPipeline.joblib
RestaurantClusteringPipeline.joblib
```

using:

```text
Zomato Restaurant names and Metadata.csv
Zomato Restaurant reviews.csv
```

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* NLP
* TF-IDF Vectorization
* Logistic Regression
* K-Means Clustering
* Joblib

---

## 👨‍💻 Author

**Dhiman Nath**

Machine Learning | Data Science | Python Development

---

## 📜 License

This project is intended for educational, academic, and portfolio purposes.
