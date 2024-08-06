# Community Crime Analysis

## Situation

In this analysis, you explored a dataset on community crime statistics in Calgary with the goal of forecasting future monthly crime counts. The dataset contains records of crime occurrences across different communities, categorized by type, year, and month. The task required cleaning and analyzing this data and then building a predictive model to forecast future crime counts.

## Task

The task involved several key steps:

- **Data Loading and Understanding**: Load the dataset and perform initial data checks.
- **Data Preprocessing**: Clean the data, handle missing values, and prepare the data for modeling.
- **Exploratory Data Analysis (EDA)**: Analyze crime distributions by community and category, visualize trends, and identify significant patterns.
- **Predictive Modeling**: Develop a neural network model using Long Short-Term Memory (LSTM) to forecast future crime counts.

## Action

1. Loading and Understanding the Data:

   - Imported necessary libraries and loaded the dataset from a provided URL.
   - Examined the first few rows to understand the structure and identified that the data needed to be sorted chronologically for accurate analysis.

2. Data Preprocessing:

   - Verified that the dataset had no missing values and confirmed correct data types.
   - Aggregated crime counts by community and category to facilitate analysis.
      Generated summary statistics to understand the distribution of crime counts.

3. Exploratory Data Analysis (EDA):

   - Visualized the top and bottom 10 communities by crime rate, revealing areas with high and low crime rates.
   - Analyzed crime categories to identify which types of crimes are most and least frequent.
   - Examined annual crime reports to observe trends and fluctuations over the years.
   - Focused on the top and bottom five communities to compare crime patterns and visualize differences in crime counts by category.

4. Predictive Modeling:

   - Prepared sequences of data for the LSTM model to handle the time series nature of the crime data.
   - Implemented a Long Short-Term Memory (LSTM) neural network to model the crime counts and forecast future values.
   - Split the data into training, validation, and test sets.
   - Trained the LSTM model with sequences of past data to predict future crime counts, optimizing performance through iterative epochs.

## Result

The analysis successfully provided insights into crime distribution and trends in Calgary. The visualizations highlighted key patterns such as:

- High-crime and low-crime communities.
- Crime categories with varying frequencies.
- Fluctuations in crime rates over time.

The LSTM model, trained on the processed data, is expected to offer reliable forecasts for future monthly crime counts. This forecasting capability will support community planning and resource allocation for crime prevention strategies.

This analysis not only provided a detailed view of current crime statistics but also equipped stakeholders with predictive insights. By understanding crime patterns and forecasting future trends, the analysis supports proactive measures to address crime in Calgary effectively.