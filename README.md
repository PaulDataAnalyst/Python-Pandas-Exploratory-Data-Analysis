# Exploratory Data Analysis (EDA) Project

## Overview

This project documents my initial steps in learning and practicing Exploratory Data Analysis (EDA) with the guidance of ALEX The DATA ANALYST BOOTCAMP. The primary goal was to gain hands-on experience in understanding a dataset by identifying patterns, exploring relationships between different features, and detecting potential outliers. This process is crucial for gaining initial insights into the data before more advanced analysis or modeling.

## Objectives

In this project, I aimed to:

* Practice fundamental EDA techniques using Python libraries.
* Identify potential patterns and trends within the dataset.
* Understand the correlation between different features.
* Detect and visualize potential outliers.
* Gain familiarity with data inspection and summary statistics.

## Steps Undertaken

The following steps were taken to perform the Exploratory Data Analysis:

1.  **Import Libraries:**
    ```python
    import pandas as pd
    import matplotlib.pyplot as plt
    import seaborn as sns
    ```

2.  **Initial Data Exploration:**
    * Took a first look at the raw data to understand its structure and content.

3.  **Setting Float Display Options:**
    ```python
    pd.set_option('display.float_format', lambda x: '%.2f' % x)
    ```
    * Set Pandas option to display floating-point numbers with two decimal places for better readability.

4.  **Getting Data Information:**
    ```python
    df.info()
    ```
    * Used the `info()` method to get a concise summary of the DataFrame, including data types and non-null values.

5.  **Generating Descriptive Statistics:**
    ```python
    df.describe()
    ```
    * Utilized the `describe()` method to generate descriptive statistics of the numerical columns, such as count, mean, standard deviation, minimum, maximum, and quartiles.

6.  **Identifying Null Values:**
    ```python
    df.isnull().sum()
    ```
    * Found and counted the number of null (missing) values in each column.

7.  **Counting Unique Values:**
    ```python
    df['column_name'].nunique() # Example
    ```
    * Determined the number of unique values in specific columns to understand the variety within those features.

8.  **Sorting Data:**
    ```python
    df.sort_values(by='column_name') # Example
    ```
    * Sorted the DataFrame based on the values of specific columns to identify trends or extremes.

9.  **Exploring Column Correlation:**
    ```python
    df.corr()
    ```
    * Calculated the pairwise correlation between all numerical columns to understand linear relationships.

10. **Learning Heatmaps for Correlation Visualization:**
    * Used the Seaborn library to create heatmaps for visualizing the correlation matrix.
    ```python
    import seaborn as sns
    import matplotlib.pyplot as plt

    plt.rcParams['figure.figsize'] = (10, 8) # Example figure size

    sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
    plt.title('Correlation Heatmap')
    plt.show()
    ```
    * Learned to customize the heatmap using `sns.heatmap()`, including displaying annotation (`annot=True`) and choosing a color map (`cmap='coolwarm'`).
    * Utilized `plt.rcParams` to adjust figure size and `plt.show()` to display the plot.

11. **Grouping Data:**
    ```python
    grouped_data = df.groupby('grouping_column')['target_column'].mean() # Example
    ```
    * Grouped the data based on specific columns to analyze aggregated statistics for different categories.

12. **Visualizing Grouped Data:**
    ```python
    grouped_data.plot(kind='bar') # Example: Bar chart
    plt.title('Average Target by Group')
    plt.xlabel('Grouping Column')
    plt.ylabel('Average Target')
    plt.show()
    ```
    * Created visualizations (e.g., bar charts) to represent the aggregated data from the grouping step.

13. **Transposing Data (Example):**
    ```python
    df.head().T
    ```
    * Used the transpose (`.T`) method to switch rows and columns, which can be helpful for viewing many columns with fewer rows.

14. **Identifying Outliers using Boxplots:**
    ```python
    sns.boxplot(x='column_name', data=df) # Example
    plt.title('Boxplot for Outlier Detection')
    plt.show()
    ```
    * Created boxplots using Seaborn to visually identify potential outliers in numerical columns.

15. **Checking Column Data Types:**
    ```python
    df.dtypes
    ```
    * Examined the data types of each column to ensure they are appropriate for analysis.

## Conclusion

This project provided a valuable hands-on experience in performing Exploratory Data Analysis. Through these steps, I gained a better understanding of the dataset's structure, identified initial patterns and relationships between features, and learned how to detect potential outliers. This foundational knowledge is essential for any further data analysis or modeling tasks.

