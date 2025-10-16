# **Project: Customer Purchase Prediction Model: Decision Tree **  

This project focuses on building a highly accurate machine learning model to predict customer purchase decisions from an e-commerce dataset.

----------

## **Executive Summary**

This solution employs a  **Decision Tree Classifier**  enhanced by  **advanced Feature Engineering**  to forecast customer purchases with high confidence. The final model achieved a strong  **validation accuracy of 93.27%**, providing a reliable tool for targeted marketing and inventory management.

----------

## **1. Problem Statement**

The primary objective was to build a robust  **classification model**  that could predict the binary outcome (**YES/NO**) of a customer making a purchase. This required identifying complex, underlying patterns within various shopping and rating attributes.

----------

## **2. Data and Preprocessing**

-   **Data Source:**  E-commerce dataset containing over  **33,000 records**  of customer interactions, product details, and purchasing outcomes.
    
-   **Data Cleaning:**  Initial preprocessing involved cleaning and handling missing values in key columns like  `ratings`  and  `no_of_ratings`  (filling with the  **median**).
    
-   **Currency Standardization:**  To ensure consistent pricing data, all local currency values were converted to a uniform  **USD format**  using external conversion rates.
    

----------

## **3. Advanced Feature Engineering (Key Differentiator)**

The model's strong performance was driven by three engineered, high-value features:

| **Feature**         | **Description**                                                        | **Technical Rationale**                                                                 |
|---------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| `discount_percent`  | Relative percentage saved from the actual price.                       | Directly captures the **attractiveness** of the deal.                                    |
| `discount_amount`   | Absolute dollar amount saved.                                          | Captures the **tangible cost reduction**, regardless of the original price.              |
| `weighted_rating`   | Composite score for perceived product quality and social proof.        | Engineered using the formula: `X + A·Y²` (where `X` = ratings, `Y` = no_of_ratings) to **exponentially prioritize** products with higher rating volumes. 
----------
## 4.  Model and Performance

| **Component**         | **Detail**                                                                 |
|------------------------|---------------------------------------------------------------------------|
| **Model Type**         | Decision Tree Classifier (Scikit-learn)                                   |
| **Data Split**         | 80% Training / 20% Validation                                              |
| **Key Features Used**  | `discount_percent`, `ratings`, `no_of_ratings`, `discount_amount`, `weighted_rating` |
| **Final Accuracy**     |  **93.27%** on validation data                                           
---
## 5. Implications & Learnings

- **Feature Engineering** was the key driver of performance, particularly in capturing:
  - Non-linear interactions between product appeal and social proof.
  - Combined effects of price discounts and product trustworthiness.
- The **Decision Tree Classifier** effectively segmented customer intent based on:
  - **Price sensitivity**
  - **Product quality perception**
- This project reinforced the importance of **data preparation** (e.g., currency standardization, robust missing value handling) for building **production-ready models**.

---
