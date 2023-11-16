## US_State_Power_Outage


### Introduction to the Dataset

The dataset under analysis contains comprehensive information regarding power outages across different states in the United States. Our analysis aims to explore the factors contributing to severe outages and their impact on different states.



### Question:

 Out of the various states, which are most likely to experience the most severe power outages, and what are the primary causes?

This analysis centers around understanding the severity of power outages in different states within the United States and uncovering the root causes behind these outages. By identifying states prone to severe outages and the key contributing factors, stakeholders can develop targeted strategies to enhance infrastructure resilience and minimize outage impacts.

### Data Cleaning and EDA (Exploratory Data Analysis)

**Combining Date and Time Columns**

In data processing and cleaning, it's often necessary to merge separate date and time columns into a single datetime column for better analysis. Here's a function that achieves this using Pandas in Python:

```py
def combine_times(date_col_name, time_col_name, new_col_name, df):
    # Creating a copy of the DataFrame to avoid modifying the original data
    df = df.copy()
    
    # Combining date and time columns to create a new datetime column
    df[new_col_name] = df[date_col_name] + pd.to_timedelta(df[time_col_name].astype(str))
    
    return df
```


**Reading and Cleaning** 

Because the data was in an excel format, we used `pd.read_excel()` to read into the data. Afterwords, we called the `combine_times` function on the time columns we wanted to combine.
```py
import pandas as pd

# Read data from the Excel file, skipping unnecessary rows and columns
data = pd.read_excel("outage.xlsx", skiprows=[0, 1, 2, 3, 4, 6], index_col=1).iloc[:, 1:]

# Combine start date and time columns into a new datetime column
data = combine_times("OUTAGE.START.DATE", 'OUTAGE.START.TIME', 'OUTAGE.START.DATETIME', data)

# Combine restoration date and time columns into another new datetime column
data = combine_times("OUTAGE.RESTORATION.DATE", "OUTAGE.RESTORATION.TIME", "OUTAGE.RESTORATION.DATETIME", data)

```

### Univariant Graph
Embed at least one plotly plot you created in your notebook that displays the distribution of a single column (see Part 2: Report for instructions). Include a 1-2 sentence explanation about your plot, making sure to describe and interpret any trends present. (Your notebook will likely have more visualizations than your website, and that’s fine. Feel free to embed more than one univariate visualization in your website if you’d like, but make sure that each embedded plot is accompanied by a description.)

<iframe src="static/uni-plot.html" width=800 height=600 frameBorder=0></iframe>


### Bivariant Graph

Embed at least one plotly plot that displays the relationship between two columns. Include a 1-2 sentence explanation about your plot, making sure to describe and interpret any trends present. (Your notebook will likely have more visualizations than your website, and that’s fine. Feel free to embed more than one bivariate visualization in your website if you’d like, but make sure that each embedded plot is accompanied by a description.)


<iframe src="static/bi-plot.html" width=800 height=600 frameBorder=0></iframe>


### Interesting Aggregate
Found which states had the most outages

<!-- <details>
<summary>Click to expand table</summary> -->

```py
data.groupby('U.S._STATE')['YEAR'].count().sort_values()
```

| U.S. State           | YEAR |
|----------------------|------|
| California           | 210  |
| Texas                | 127  |
| Washington           | 97   |
| Michigan             | 95   |
| New York             | 71   |
| Maryland             | 58   |
| Pennsylvania         | 57   |
| Illinois             | 46   |
| Florida              | 45   |
| Indiana              | 43   |
| Ohio                 | 43   |
| Utah                 | 41   |
| Delaware             | 41   |
| North Carolina       | 40   |
| Louisiana            | 40   |
| Virginia             | 37   |
| New Jersey           | 35   |
| Tennessee            | 34   |
| Arizona              | 28   |
| Oregon               | 26   |
| Arkansas             | 25   |
| Oklahoma             | 24   |
| Wisconsin            | 20   |
| Maine                | 19   |
| Connecticut          | 18   |
| Massachusetts        | 18   |
| Georgia              | 17   |
| Missouri             | 17   |
| Colorado             | 15   |
| Minnesota            | 15   |
| New Hampshire        | 14   |
| Kentucky             | 13   |
| District of Columbia | 10   |
| Kansas               | 9    |
| Idaho                | 9    |
| Vermont              | 9    |
| Iowa                 | 8    |
| New Mexico           | 8    |
| South Carolina       | 8    |
| Nevada               | 7    |
| Wyoming              | 6    |
| Alabama              | 6    |
| Hawaii               | 5    |
| Nebraska             | 4    |
| West Virginia        | 4    |
| Mississippi          | 4    |
| Montana              | 3    |
| North Dakota         | 2    |
| South Dakota         | 2    |
| Alaska               | 1    |

<!-- </details> -->

## Assessment Of Missingness

## NMAR
State whether you believe there is a column in your dataset that is NMAR. Explain your reasoning and any additional data you might want to obtain that could explain the missingness (thereby making it MAR). Make sure to explicitly use the term “NMAR.”

**CAUSE CATEGORY DETAIL**: CAUSE.CATEGORY.DETAIL
All the NAN values in CLIMATE.CATEGORY.DETAIL could be NMAR because the type of disaster may affect whether or not the data could be collected. For instance, a severe weather event like heavy rain and hail could occur at the same time and obscure the real cause of the damage. Because of this uncertaintity, this data may not have been collected for certain types of causes which may have coincided. This would cause the missingness of the data to be dependent on what kind of event was occuring and thus it would depend on itself making it NMAR.



## MAR
Present and interpret the results of your missingness permutation tests with respect to your data and question. Embed a plotly plot related to your missingness exploration; ideas include:
• The distribution of column 
Y
 when column 
X
 is missing and the distribution of column 
Y
 when column 
X
 is not missing, as was done in Lecture 12.
• The empirical distribution of the test statistic used in one of your permutation tests, along with the observed statistic.

<iframe src="static/mar-plot.html" width=800 height=600 frameBorder=0></iframe>



## Hypothesis Testing

**Question:** COW

Clearly state your null and alternative hypotheses, your choice of test statistic and significance level, the resulting 
p
-value, and your conclusion. Justify why these choices are good choices for answering the question you are trying to answer.

Optional: Embed a visualization related to your hypothesis test in your website.

Tip: When making writing your conclusions to the statistical tests in this project, never use language that implies an absolute conclusion; since we are performing statistical tests and not randomized controlled trials, we cannot prove that either hypothesis is 100% true or false.

