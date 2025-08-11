# Wings R Us – Personalized Add-On Recommendation System

![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-11%20221324.png)

# Overview
Wings R Us is a US-based quick service restaurant chain specializing in chicken wings.
The goal of this project was to boost average order value and enhance the digital checkout experience by providing personalized last-minute add-on recommendations across mobile app, website, and self-service kiosks.

This system leverages historical purchase data to predict relevant add-on items, ensuring varied, non-repetitive, and highly relevant suggestions for customers ranging from first-time visitors to loyal regulars.

# Problem Statement
The recommendation engine needed to:

Predict relevant add-ons based on customer purchase history.

Adapt to a diverse customer base.

Keep suggestions fresh and non-repetitive.

Perform consistently across platforms (app, web, kiosks).

Support a fast, low-risk pilot before full rollout.

# Our Approach
## 1. Data Preprocessing
Data Cleaning: Removed inconsistencies and standardized raw datasets.

Date Standardization: Unified formats to capture seasonal and time-based patterns.

Label Encoding: Converted item names into numeric IDs for ML compatibility.

Case Filtering: Excluded single-item orders where recommendations are not applicable.

## 2. Exploratory Data Analysis (EDA)
Identified top-selling items and purchase trends.

Analyzed customer behavior patterns.

Discovered key predictive signals for recommendations.

![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-10%20211531.png)
![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-10%20211612.png)
![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-10%20223749.png)
![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-10%20223830.png)
![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-10%20223904.png)
![Alt text](https://github.com/sanskriti111-j/Recommendation-Algorithm-for-a-Quick-Service-Restaurant/blob/main/Screenshot%202025-08-10%20224032.png)


## 3. Order Structuring
Transformed orders into a fixed schema:
item1 | item2 | item3 | target_item
The target_item is the add-on item to be predicted.

## 4. Model Development
Algorithm: XGBoost – chosen for:

High accuracy

Fast training

Strong performance on sparse/tabular data

Evaluation Metric: Multi-Class Log Loss (MLogLoss) for probability ranking.

Output: Top-3 ranked item predictions for each cart.

## 5. Training & Validation
Stratified Train-Test Split to maintain target distribution across datasets.

Generated Top-3 predictions to improve Recall@3 and increase basket size.

# Results
Recall@3: 0.45 → Correct add-on included in top 3 recommendations 45% of the time.

Increased probability of upselling relevant items.

Provided a scalable solution for expansion across all ordering platforms.


