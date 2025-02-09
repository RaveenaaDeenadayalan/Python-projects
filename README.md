# IMDB Analysis

## Overview
This project involves cleaning and analyzing the IMDb dataset to gain insights into movie ratings and features while developing regression and classification models. The dataset initially contained several issues such as duplications, missing values, and non-numeric data types that required extensive preprocessing before effective model development.

## Objectives
- Clean the dataset and remove unnecessary columns.
- Handle missing values and standardize data types.
- Perform exploratory data analysis (EDA).
- Create and evaluate regression and classification models.
- Implement clustering models for anomaly detection.

---

## Model Development

### Regression Models
The following regression models were evaluated:

| Model                | CV RMSE Mean | Test RMSE | Test R-squared |
|----------------------|--------------|-----------|----------------|
| AdaBoost             | 1.432999     | 1.422942  | 0.112355       |
| Lasso                | 1.520080     | 1.510355  | -0.000054      |
| Ridge                | 1.368617     | 1.363798  | 0.184611       |
| Bayesian Ridge       | 1.368613     | 1.363789  | 0.184622       |
| Polynomial Regression| 1.354126     | 1.343972  | 0.208145       |

#### Insights
- The regression models did not perform well, indicating the need for additional features such as gross sales, director ratings, and more detailed movie information.
- Polynomial Regression showed the best performance, though it remained insufficient for practical use.

### Classification Models
- Gradient Boosting emerged as the best model, but the scores were still shallow, suggesting limited predictive power due to feature insufficiency.

---

## Clustering and Anomaly Detection

### Birch Clustering
- Identified seven clusters, with almost half of the rows in cluster 0.
- The clusters had similar average and median ratings.

### DBSCAN Clustering
- Found 36 clusters, with 214,944 rows in a single cluster.
- Identified 2,602 rows as anomalies or outliers, requiring further investigation.
- The anomalies had runtime minutes in thousands, which made them distinct.

### GMM Clustering
- Produced clusters with similar averages and medians as Birch but with different row distributions.

---

## Conclusion and Recommendations
- The current dataset lacks sufficient features for effective regression and classification models.
- Adding features such as movie gross sales, detailed director information, and audience demographics could significantly improve model performance.
- Parameter tuning and feature engineering could further optimize the models.
- Clustering models highlighted runtime anomalies, which could be valuable for further data investigation.
- This analysis confirms that data quality and feature richness are critical for building accurate predictive models.

---


