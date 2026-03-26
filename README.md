# Customer Churn Prediction & Sentiment Analysis | ABCTelco Case Study

This project explores why customers leave a telecommunications company, combining traditional statistical analysis with Natural Language Processing (NLP). It was developed as a comprehensive case study to predict churn and extract actionable insights from customer feedback.

## 🎯 The Goal
The objective was to build a predictive model using a dataset of **7,043 clients** and **1,605 written complaints**. Instead of looking only at numbers (like monthly charges), we integrated the "voice of the customer" by analyzing the sentiment of their actual complaints.

## 💡 Key Features & Methodology
What makes this project stand out is the integration of two different data sources:

* **Feature Engineering:** Beyond basic data, I created specific indicators like a `streaming` service index and a `phonelines` variable to better capture customer behavior.
* **Sentiment Analysis:** I used the **Bing lexicon** to transform raw text complaints into numerical scores. This allowed us to quantify just how "frustrated" or "satisfied" a customer was.
* **Topic Modeling (LSA):** I performed a Latent Semantic Analysis to identify the core themes in customer complaints, discovering that 54 topics explained 70% of the issues raised.
* **Advanced Modeling:** I didn't just run one model. I compared **Logistic Regression, Lasso, Random Forest, and Boosting** using 5-fold cross-validation to ensure the results were reliable and not just due to luck.

## 🛠️ Tech Stack
* **Language:** R
* **Libraries:** `tidyverse` (dplyr/ggplot2), `tidytext` (NLP), `glmnet` (Lasso), `randomForest`, and `gbm` (Boosting).

## 📊 Results
After testing multiple algorithms, the **Lasso model** came out on top with the lowest misclassification error.

| Model | Misclassification Error |
| :--- | :--- |
| **Lasso** | **0.1846** |
| **Logistic** | **0.1857** |
| **Boosting** | 0.1870 |
| **Random Forest** | 0.1892 |

The analysis confirmed that while "tenure" and "contract type" are huge factors, the **sentiment score** from complaints is a powerful predictor that companies often overlook.

## 📂 What's Inside
* `final-report.pdf`: The complete, formatted report with all my visualizations and conclusions.
* `final report.Rmd`: The source code. Everything from data cleaning to final model tuning is here for full transparency.
* `ABCTelco_clients`: data
* `ABCTelco_complaints`: complaints
