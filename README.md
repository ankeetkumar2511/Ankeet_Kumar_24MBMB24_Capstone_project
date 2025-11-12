OTT Platform Analytics: Harnessing PySpark for User Behavior Insights

Project Overview

This capstone project is a deep dive into user behavior analytics within the Over-The-Top (OTT) streaming industry, similar to platforms like Netflix and JioHotstar. The primary goal was to leverage the advanced capabilities of the **PySpark MLlib** library to derive actionable business insights across multiple use cases

The project successfully applied machine learning to critical business problems: identifying users at risk of churning, segmenting the customer base for targeted marketing, and forecasting key metrics.

Technology Stack & Methodology

| Category | Tools/Libraries Used | Rationale/Context |
| :--- | :--- | :--- |
| **Big Data Framework** | **PySpark** & **MLlib** | Chosen to demonstrate scalability and proficiency in handling large datasets, using a robust framework suitable for production environments. |
| **Analysis** | [span_3](start_span)Exploratory Data Analysis (EDA)[span_3](end_span) | [span_4](start_span)Performed to understand user demographics, subscription trends, and engagement patterns[span_4](end_span). |
| **Models** | Random Forest, Decision Tree, Linear Regression, GBT Regressor | [span_5](start_span)A variety of models were tested to address both Classification (e.g., Churn) and Regression (e.g., Revenue) use cases[span_5](end_span). |

## 📊 Dataset Overview

[span_6](start_span)The analysis is based on a dataset of **1,000 user records** from a fictional OTT streaming service[span_6](end_span).

**Key Features Included:**
* **[span_7](start_span)Demographics:** Age, Gender, Region[span_7](end_span)
* **[span_8](start_span)Subscription:** Plan, Monthly Spend[span_8](end_span)
* **[span_9](start_span)Engagement:** Watch Hours, Sessions[span_9](end_span)
* **Feedback:** Avg. [span_10](start_span)Rating, Sentiment[span_10](end_span)

## 💡 Key Findings from Exploratory Data Analysis (EDA)

[span_11](start_span)The initial analysis revealed a critical pattern we termed the **"Value Ladder"**[span_11](end_span):
* **Engagement-Tier Correlation:** Higher subscription tiers correlate directly with higher engagement. [span_12](start_span)Users on the **Premium** plan averaged **80.1 hours** of watch time, while the **Free** tier averaged only **33.7 hours**[span_12](end_span).
* **Churn Risk:** The churn rate drops significantly as the subscription tier increases. [span_13](start_span)The **Free tier** has a high churn rate of **20.4%**, compared to only **2.3%** for the **Premium** tier[span_13](end_span).

## ✅ Primary Use Cases & Successes

| Use Case | Model Used | Key Metric | Result / Key Insight |
| :--- | :--- | :--- | :--- |
| **1. [span_14](start_span)Customer Churn Prediction**[span_14](end_span) | **[span_15](start_span)Random Forest Classifier**[span_15](end_span) | [span_16](start_span)F1-Score[span_16](end_span) | **[span_17](start_span)Strong F1-Score of 88.8%**[span_17](end_span). [span_18](start_span)The model is effective at correctly identifying at-risk users, which is crucial given the data imbalance (913 non-churners vs. 87 churners)[span_18](end_span). |
| **2. [span_19](start_span)User Segmentation**[span_19](end_span) | **[span_20](start_span)Decision Tree Classifier**[span_20](end_span) | Accuracy | **[span_21](start_span)89.4% Accuracy**[span_21](end_span). [span_22](start_span)Identified the **'Engaged Low Spender'** segment (Low spend, high watch time) as a key business opportunity for targeted upsell campaigns[span_22](end_span). |

## ❌ Secondary Use Cases & Learning Points (Regression Analysis)

[span_23](start_span)Attempts were made to forecast continuous values, which proved highly complex, providing valuable lessons on feature requirements for these tasks[span_23](end_span).

| Use Case | Model Used | Key Metric | Result (R-squared) | Learning / Conclusion |
| :--- | :--- | :--- | :--- | :--- |
| **3. [span_24](start_span)Revenue Prediction**[span_24](end_span) | [span_25](start_span)Linear Regression[span_25](end_span) | R-squared | **[span_26](start_span)R-squared of 0.09**[span_26](end_span). | [span_27](start_span)The lack of predictive power suggests revenue is determined by the **fixed subscription plan** rather than behavioral features[span_27](end_span). |
| **4. [span_28](start_span)Watch Time Prediction**[span_28](end_span) | [span_29](start_span)GBT Regressor[span_29](end_span) | R-squared | **[span_30](start_span)R-squared of -0.28**[span_30](end_span). | [span_31](start_span)A negative R-squared indicates the model performed worse than simply using the average[span_31](end_span). [span_32](start_span)Predicting future watch time requires more sophisticated time-series data and features[span_32](end_span). |

**[span_33](start_span)Overall Conclusion:** Classification models were highly successful in this project, whereas Regression models require more advanced, time-dependent, and external features for effective prediction[span_33](end_span).

## 📂 Repository Structure

* `OTT Platform Analytics.ipynb`: The primary Jupyter Notebook containing the code for EDA, PySpark preprocessing, and all four model implementations.
* `OTT Platform Analytics (1).pptx`: Project presentation slides.
* `dataset/`: Folder containing the user record data file.
