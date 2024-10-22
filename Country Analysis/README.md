# Clustering the Countries using Unsupervised Learning

### Problem
HELP International, a humanitarian NGO dedicated to fighting poverty, has raised $10 million to provide aid to countries in need. The challenge is for the CEO to allocate these funds strategically and effectively, focusing on the countries in the most urgent need of assistance. The complexity lies in determining which countries should be prioritized based on their socio-economic and health factors.

### Objective
The objective is to use unsupervised learning techniques to categorize countries based on socio-economic and health indicators, which reflect their overall development. By doing so, the CEO will have data-driven insights to help allocate the funds to the countries in the direst need of aid.

### Dataset Description
The dataset contains socio-economic and health indicators for various countries, reflecting their overall level of development. These features provide insights into the living conditions and well-being of the populations. The key variables in the dataset include:
- Country (`country`): The name of the country.
- Child Mortality (`child_mort`): The number of deaths of children under 5 years of age per 1,000 live births, indicating the level of healthcare for young children.
- Exports (`exports`): Exports of goods and services per capita, expressed as a percentage of the GDP per capita, reflecting the country's economic output through trade.
- Health Spending (`health`): Total health expenditure per capita, expressed as a percentage of GDP per capita, showing the investment in the country's healthcare system.
- Imports (`imports`): Imports of goods and services per capita, expressed as a percentage of the GDP per capita, indicating the country's reliance on foreign goods and services.
- Income (`income`): The average net income per person, a measure of individual wealth in the country.
- Inflation (`inflation`): The annual growth rate of the total GDP, indicating the economic stability and purchasing power within the country.
- Life Expectancy (`life_expec`): The average number of years a newborn child is expected to live under the current mortality patterns, reflecting the overall health of the population.
- Fertility Rate (`total_fer`): The average number of children a woman is expected to have during her lifetime, based on current fertility rates.
- GDP per Capita (`gdpp`): The total GDP divided by the population, measuring the economic productivity per person.

Dataset source: https://kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data/data

### Approach

#### 1. Data Ingestion
The first step in the process involved reading and loading the dataset into the environment for analysis and further processing. The dataset was thoroughly inspected to ensure that all relevant data was included.

#### 2. Data Quality
Ensuring the quality of the data is crucial to building an effective model. Several checks and processes were performed:
- **Summary Statistics**: Generated to provide insights into the distribution of the data and its key features.
- **Missing Data**: Identified any missing values that could affect the performance of the model, and appropriate steps were taken to handle them.
- **Duplicate Data**: Checked for and removed any duplicate records to ensure that the analysis was not skewed by repeated entries.

#### 3. Exploratory Data Analysis (EDA)
A comprehensive exploration of the dataset was conducted to uncover underlying patterns and trends:
- **Auto-EDA Report**: Automated exploratory data analysis was generated to quickly summarize the data's characteristics.
- **Distribution of Variables**: Analyzed the distribution of key socio-economic and health indicators, identifying any potential outliers or unusual patterns.
- **Correlation Analysis**: Explored the relationships between different variables to understand how they relate to one another.

#### 4. Preprocessing
Before modeling, the data underwent preprocessing to ensure that it was in the right format for analysis:
- **Feature Scaling**: Applied to normalize the data and prevent any one feature from disproportionately affecting the results.
- **Dimensionality Reduction**: Techniques were used to reduce the number of features while preserving the underlying structure of the data, optimizing the performance of the model.

#### 5. Modelling
The modeling process involved several steps to categorize the countries based on socio-economic and health indicators:
- **Optimal Number of Clusters**: Determined using methods such as the Elbow Method or Silhouette Score, ensuring the most appropriate clustering structure for the data.
- **Building the Model**: Clustering algorithms, such as K-Means, were applied to group the countries into distinct categories.
- **Evaluate the Model**: The clustering model's performance was evaluated to ensure the groupings were meaningful and provided actionable insights.
- **Cluster Characterization**: Once the clusters were formed, they were analyzed and characterized based on their socio-economic and health attributes, allowing for clear insights into which countries should be prioritized for aid.

### Libraries   
Scikit-Learn, Pandas, Matplotlib, Seaborn, Plotly, NumPy, Pandas Profiling


