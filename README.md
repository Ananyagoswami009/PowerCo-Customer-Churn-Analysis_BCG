# PowerCo-Customer-Churn-Analysis_BCG

## Overview

This project focuses on analyzing and predicting customer churn for PowerCo, a major gas and electricity utility provider. The key objective is to investigate the factors influencing customer churn, specifically examining the role of price sensitivity in customer retention. The work is part of my role as a Junior Data Scientist at **BCG X**, where we leverage data science to transform businesses and help them achieve a competitive advantage through data-driven decision-making.

### Role and Responsibilities

As a Junior Data Scientist at **BCG X**, I am involved in various stages of the data science methodology, including business understanding, exploratory data analysis (EDA), feature engineering, modeling, and providing actionable insights. In this project, I worked closely with Estelle Altazin, a Senior Data Scientist, and the broader BCG X team to address PowerCo’s churn problem. This project provided me with hands-on experience in data analysis, problem-solving, programming, and communication—critical skills for my career growth as a data scientist.

## About the Client

**PowerCo** is a leading utility company that provides gas and electricity to small and medium-sized enterprises. Recently, PowerCo has faced increasing competition in the energy market, where customers have more options than ever before. As a result, PowerCo has noticed a higher rate of customer churn, particularly as customers switch to competitors offering better deals. The company engaged BCG X to help diagnose the reasons behind customer churn and identify actionable insights to improve customer retention.

### Problem Statement

PowerCo’s key concern is customer churn. Specifically, PowerCo suspects that **price sensitivity** is a major factor influencing customers' decisions to leave the service. However, PowerCo is uncertain about the exact role of price in customer retention. 

Our task is to:
- Investigate the impact of price sensitivity on customer churn.
- Identify other factors contributing to churn.
- Provide actionable insights for PowerCo to improve customer retention strategies.

### Methodology

To tackle this problem, we applied the **5-step data science methodology**:
1. **Business Understanding & Problem Framing**: Understanding the context of the problem and hypothesizing potential causes of churn (e.g., price sensitivity, customer service, etc.).
2. **Exploratory Data Analysis (EDA)**: Investigating the available data to identify patterns, trends, and potential features related to churn.
3. **Feature Engineering**: Enhancing the dataset by creating new features that improve the model's predictive power.
4. **Modeling & Evaluation**: Building and testing predictive models to understand the factors driving churn and their respective influences.
5. **Insights & Recommendations**: Translating the model's results into actionable insights for PowerCo.

---

## Datasets

The following datasets were provided by PowerCo and were used throughout the analysis:

- **`client_data.csv`**: Contains details about PowerCo’s customers, including industry, electricity consumption, and date of joining.
- **`price_data.csv`**: Contains historical price data for electricity and gas, including prices charged to customers over time.
- **`data_for_prediction.csv`**: A final dataset with all features prepared for predictive modeling to test churn likelihood.
- **`clean_data_after_eda.csv`**: A cleaned version of the data after exploratory analysis, with unnecessary columns removed and missing data handled.

---

# Files & Folder Structure
/PowerCo_Churn_Analysis
├── /Data
│ ├── client_data.csv
│ ├── price_data.csv
│ ├── clean_data_after_eda.csv
│ └── data_for_prediction.csv
├── /Notebooks
│ ├── Task_2_EDA.ipynb
│ ├── Task_3_Feature_Engineering.ipynb
│ └── Task_4_Modeling.ipynb
├── /Slides
│ └── Executive_Summary.pdf
├── /Readme
│ └── README.md (This file)/
---



### Task 1: Business Understanding & Hypothesis Framing

**Objective**: Formulate PowerCo’s issue using the 5-step data science process and lay out the steps needed to test the hypothesis of price sensitivity driving churn.

- **Client Problem**: PowerCo is concerned about losing customers due to better offers from competitors. The hypothesis is that **price sensitivity** plays a major role in customer churn.
- **Data Requirements**:
  - **Customer Data**: Industry, electricity consumption, customer join date, etc.
  - **Churn Data**: Whether a customer has churned.
  - **Price Data**: Historical pricing information for electricity and gas.

**Data Science Process**:
1. **Define Price Sensitivity**: Understand how sensitive customers are to price fluctuations and how this affects churn.
2. **Prepare Data**: Clean, transform, and engineer features.
3. **Test Hypothesis**: Use a binary classification model (e.g., Logistic Regression, Random Forest) to test the impact of price sensitivity on churn.

**Deliverable**: An email to the Associate Director outlining the hypothesis, required data, and approach (included in the project as Task 1 Email).

### Task 2: Exploratory Data Analysis (EDA)

**Objective**: Investigate the data to uncover trends, correlations, and anomalies that could help in understanding the factors influencing churn.

- **Key Steps**:
  1. **Initial Data Exploration**: Analyzed the `client_data.csv` and `price_data.csv` for missing values, correlations, and distribution of key variables.
  2. **Data Cleaning**: Removed irrelevant columns, handled missing data, and corrected any anomalies.
  3. **Visualizations**: Created visualizations to understand price trends, consumption patterns, and churn rates.

- **Output**: A cleaned and preprocessed dataset (`clean_data_after_eda.csv`) and Jupyter notebook (`Task_2_EDA.ipynb`).

### Task 3: Feature Engineering & Data Preparation

**Objective**: Enhance the dataset by creating new features that could improve the model's ability to predict churn.

- **Key Features Engineered**:
  1. **Price Sensitivity Features**: Calculated average and maximum price differences across periods.
  2. **Date Transformation**: Converted date columns into more meaningful features like month, day, and year.
  3. **Categorical Variables**: Converted categorical data into dummy variables and binary flags for easier use in modeling.
  4. **Normalization**: Applied logarithmic transformation to skewed columns for a more normal distribution.

- **Output**: A new dataset (`clean_data_after_eda.csv`) and a Jupyter notebook (`Task_3_Feature_Engineering.ipynb`) for further analysis.

### Task 4: Model Building & Evaluation

**Objective**: Build predictive models to understand the likelihood of customer churn based on various factors, particularly price sensitivity.

- **Modeling Steps**:
  1. **Model Selection**: Chose models such as Logistic Regression, Random Forest, and Gradient Boosted Machines.
  2. **Model Training**: Trained models using the `data_for_prediction.csv` dataset.
  3. **Model Evaluation**: Evaluated models based on metrics like accuracy, precision, recall, and AUC-ROC.
  4. **Model Tuning**: Fine-tuned models using hyperparameter optimization to improve performance.

- **Output**: Trained models and evaluation results saved in `Task_4_Modeling.ipynb`.

### Task 5: Findings & Recommendations

**Objective**: Synthesize the findings from the analysis and model results, and provide actionable insights to PowerCo.

- **Key Insights**:
  - **Price Sensitivity**: Customers with higher sensitivity to price fluctuations were more likely to churn.
  - **Customer Service**: Poor customer service also correlated with higher churn rates.
  - **Energy Plan Fit**: Mismatch between customer consumption patterns and their energy plan was a contributing factor.

- **Recommendations**:
  - Offer more competitive pricing for price-sensitive customers.
  - Improve customer service to enhance retention.
  - Tailor energy plans more closely to customer usage patterns.

- **Deliverable**: A slide presentation summarizing findings, insights, and recommendations (`Executive_Summary.pdf`).

---

## How to Run the Code

1. **Install Dependencies**:
   To run the Jupyter notebooks, first install the necessary Python libraries by running:
   ```bash
   pip install -r requirements.txt

2. Run the Notebooks:
  Navigate to the Notebooks folder and run the Jupyter notebooks sequentially:

  Task_2_EDA.ipynb

  Task_3_Feature_Engineering.ipynb

  Task_4_Modeling.ipynb

Future Work
Model Improvement: Explore additional machine learning models and fine-tune them for better performance.
Real-time Deployment: Implement the final churn prediction model into a production environment for real-time customer churn analysis.

Conclusion
This project provided a deep dive into analyzing customer churn for PowerCo, with a focus on understanding the role of price sensitivity in customer retention. Through exploratory data analysis, feature engineering, and machine learning, we developed a robust predictive model that will help PowerCo take proactive steps to retain at-risk customers.
