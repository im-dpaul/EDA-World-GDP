# Global GDP Insights: Analyzing Economic Trends

This project conducts Exploratory Data Analysis (EDA) on a GDP dataset, examining GDP trends, growth rates, and comparisons between different countries. The analysis includes visualization of GDP values, growth rates, and comparative analyses to derive insights into global economic dynamics.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Analysis](#data-analysis)
  - [Data Loading and Inspection](#data-loading-and-inspection)
  - [Analysing Specific Country](#analysing-specific-country)
  - [Calculating GDP Growth for All Countries](#calculating-gdp-growth-for-all-countries)
  - [Analyzing GDP Trends](#analyzing-gdp-trends)
  - [Analyzing GDP Growth](#analyzing-gdp-growth)
- [Conclusion](#conclusion)

## Introduction
Exploratory Data Analysis is a fundamental step in understanding the structure and patterns present in datasets. This project focuses on analyzing GDP data to uncover trends, variations, and relationships between different economic indicators across various countries and time periods.

## Dataset
The dataset contains information on GDP values and growth rates for multiple countries over several years. It includes metrics such as GDP values, years, country codes, and country names. The dataset enables the analysis of GDP trends and comparisons between countries.

## Data Analysis
The analysis includes visualizations and statistical summaries to explore various aspects of GDP data.

### Data Loading and Inspection
   - Loaded the CSV data using pandas.
   - Displayed the first few rows (`df.head()`) to get an initial glimpse of the data structure.
   - Examined data types and descriptive summaries of columns like `Country Code`, `Country Name`, and `Year`.

### Analysing Specific Country
   - Extracted data for India (`df_pr = df[df['Country Code'] == 'IND']`)
   - Visualized India's GDP trend over the years using line plots (`df_pr.plot(kind='line')`).
   - Calculated and displayed India's annual GDP growth rate as a new column named "GDP".

### Calculating GDP Growth for All Countries
   - Iterated through each unique country code to extract data for that country.
   - Calculated annual GDP growth rate for each country and added it as a new "GDP" column.
   - This resulted in a comprehensive dataset with GDP growth information for all countries.

### Analyzing GDP Trends
   - **Global GDP Analysis:**
     - Created a line plot to visualize the global GDP trend (`df_pr[df['Country Name'] == 'World']`).
     - Saved the interactive plot as an HTML file (`'World GDP Analysis.html'`).
   - **Country-Specific GDP Analysis:**
     - Created line plots for India (`'Indian GDP'`) and India with a limited Y-axis range (`'Indian GDP'`) to focus on details.
     - Saved the interactive plots as separate HTML files.
   - **All Countries GDP Comparison:**
     - Created a line plot comparing the GDP trends of all countries (`'Countries GDP.html'`).
   - **Customized Country Comparisons:**
     - Defined a function `compare_gdp` that takes a list of country codes and a boolean flag (`isopen`) as arguments.
     - The function creates a line plot comparing the GDPs of the specified countries and saves it as an interactive HTML file. The `isopen` flag controls whether the plot is automatically opened in the web browser.
     - Examples of function usage are provided for comparing GDPs between India and USA, and a group of countries (Japan, India, USA, and China).

### Analyzing GDP Growth
   - Analyzed the GDP growth column ("GDP") for all countries.
   - Created a line plot to visualize the GDP growth trends (`'GDP Growth.html'`).
   - Optionally, filtered the data to include only countries with complete data for all years (1960-2016) for a more focused analysis (`'GDP Growth.html'`).

## Conclusion
The EDA provides valuable insights into GDP trends, growth rates, and comparative analyses across different countries. The `compare_gdp` function to create custom visualizations comparing GDPs of specific country groups It enhances our understanding of global economic dynamics and can inform decision-making processes in various sectors such as finance, policy-making, and investment.
