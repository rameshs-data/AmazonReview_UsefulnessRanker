# Amazon Book Reviews Analysis and Helpfulness Prediction

## Overview
This project involves analyzing the Amazon Book Reviews Dataset and creating a model to predict the likelihood of a review being helpful. The dataset is filtered to include reviews from the last two years available (2003-2005).

## Table of Contents
1. [Dataset](#dataset)
2. [Data Processing](#data-processing)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Memory Optimization](#memory-optimization)
5. [Modeling](#modeling)
6. [Evaluation](#evaluation)
7. [Conclusion](#conclusion)

## Dataset
The Amazon Book Reviews Dataset includes various features such as customer ID, review ID, product ID, star rating, helpful votes, total votes, review headline, review body, and review date.

**Data Dictionary:**
- `marketplace`: Country code where the review was written.
- `customer_id`: Random identifier for the customer.
- `review_id`: Unique identifier for each review.
- `product_id`: Unique identifier for the product being reviewed.
- `product_parent`: Identifier to aggregate reviews for the same product.
- `product_title`: Title of the product.
- `product_category`: Category under which the product falls.
- `star_rating`: Star rating given by the reviewer (1 to 5 stars).
- `helpful_votes`: Number of votes indicating how many customers found the review helpful.
- `total_votes`: Total number of votes the review received.
- `vine`: Indicates if the review was part of the Vine program.
- `verified_purchase`: Indicates if the review is based on a verified purchase.
- `review_headline`: Title or headline of the review.
- `review_body`: Main text of the review.
- `review_date`: Date on which the review was written.

## Data Processing
1. **Filtering Data:** Extracted reviews from 2003 to 2005.
2. **Handling Missing Values:** Identified and handled missing values appropriately.
3. **Feature Engineering:** Created new features such as `helpfulness_ratio` (helpful_votes/total_votes) to be used as the target variable.

## Exploratory Data Analysis (EDA)
- Analyzed distributions of star ratings, helpful votes, and total votes.
- Explored correlations between different features.
- Visualized trends and patterns in the data.

## Memory Optimization
To optimize memory usage:
- **Data Types Conversion:** Converted data types to more memory-efficient types where applicable. For example, converted `review_id` and `product_id` to categorical types.
- **Chunk Processing:** Processed the dataset in chunks to avoid memory overload.
- **Removing Redundant Data:** Dropped unnecessary columns after feature extraction.

## Modeling
Converted the problem into a regression task where the target variable is the `helpfulness_ratio`.

1. **Model Selection:** Experimented with various regression models including Linear Regression, Random Forest Regressor, and Gradient Boosting Regressor.
2. **Text Processing:** Employed NLP techniques such as TF-IDF to convert text data into numerical features.

## Evaluation
Evaluated the models using metrics such as Mean Squared Error (MSE) and R-squared (R²).

- **Baseline Model:** Established a baseline model for comparison.
- **Model Performance:** Reported on the performance of each model and selected the best-performing model based on evaluation metrics.

## Conclusion
- Summarized findings from the EDA and model evaluation.
- Highlighted the importance of specific features in predicting review helpfulness.
- Discussed potential improvements and future work.

## How to Run the Project
1. **Install Dependencies:** Ensure you have all the required libraries installed. You can install them using:
   ```bash
   pip install -r requirements.txt
