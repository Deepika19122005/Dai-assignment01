# Dai-assignment01
Indian Airlines Dataset Analysis Report
1. Overview
The dataset Indian Airlines.csv contains flight-related data, including information on duration, days left before departure, ticket prices, and city names. The notebook focuses on data preprocessing, cleaning, and standardization before further analysis.

2. Reading the Dataset
The dataset is loaded using pandas (pd.read_csv()), and its initial structure is examined using:

df.head() to preview the first few rows.
df.shape to check the number of rows and columns.
3. Exploring Data Structure
The structure of the dataset is explored to understand its contents:

df.info(): Provides an overview of column names, data types, and missing values.
df.describe(): Generates summary statistics for numerical columns.
df.columns: Lists all column names in the dataset.
4. Handling Missing Values
The dataset contains missing values, which are handled as follows:

Numeric columns: Missing values are replaced with the mean.
Categorical columns: Missing values are replaced with the mode.
5. Handling Duplicates
Duplicate rows are identified and removed using df.drop_duplicates(inplace=True).
6. Outlier Detection & Removal
The Interquartile Range (IQR) method is used to detect and remove outliers in key numerical columns:
duration
days_left
price
Outliers falling outside the calculated lower and upper bounds are removed to improve data quality.
7. Standardizing Categorical Data
City names in source_city and destination_city are standardized using a function that ensures proper capitalization.
8. Data Visualization (Recommended for Further Analysis)
Although the notebook does not currently include data visualization, the following approaches could be used:

Histograms: To analyze the distribution of duration, days_left, and price.
Box Plots: To check for remaining outliers in numerical features.
Scatter Plots: To explore relationships between price and other features.
Correlation Heatmap: To examine relationships between numerical variables.
9. Analyzing Relationships and Patterns (Potential Insights)
Flight Price Analysis: Understanding how days_left before departure affects pricing.
City Trends: Identifying the most frequent source_city and destination_city.
Duration vs. Price: Examining if longer flights tend to have higher prices.
10. Conclusion
This notebook effectively cleans and preprocesses the Indian Airlines dataset, ensuring data quality for further analysis. The next steps could include:

Adding data visualizations to uncover trends.
Performing feature engineering for predictive modeling.
Building machine learning models for price prediction
