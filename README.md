us_state_power_outage

## Introduction to the Dataset
___
Due to recent large power outages like the Texas power crisis of 2021, we wanted to investigate the causes and trends in power outages across the United States. The dataset under analysis contains comprehensive information regarding power outages across different states in the United States. Our analysis aims to explore the factors contributing to severe outages, their impact on different states, and the locations where sever outages most often occur. This would give us a better understanding of how power outages occur and how to possibly prevent them in the future.

### Description of Variables

The dataset contains 1534 rows and 55 columns. For this analysis, we decided to only use a few relevent columns. Namely, these were U.S._State, OUTAGE.START.DATE, OUTAGE.START.TIME, OUTAGE.RESTORATION.DATE, OUTAGE.RESTORATION.TIME, CAUSE.CATEGORY.DETAIL, CUSTOMERS.AFFECTED, and OUTAGE.DURATION . We have included the definitions of the 55 various variables/columns that we used in the analysis below.


<details markdown="1">
<summary>&#187; Click here to see Variable Descriptions</summary>

| Variable Name                    | Description |
|-----------------------------------|-------------|
| YEAR                              | Indicates the year when the outage event occurred |
| MONTH                             | Indicates the month when the outage event occurred |
| U.S._STATE                        | Represents all the states in the continental U.S. |
| POSTAL.CODE                       | Represents the postal code of the U.S. states |
| NERC.REGION                       | The North American Electric Reliability Corporation (NERC) regions involved in the outage event |
| CLIMATE.REGION                    | U.S. Climate regions as specified by the National Centers for Environmental Information |
| ANOMALY.LEVEL                     | Represents the oceanic El Niño/La Niña (ONI) index referring to the cold and warm episodes by season |
| CLIMATE.CATEGORY                  | Represents the climate episodes corresponding to the years. The categories are “Warm”, “Cold” or “Normal” episodes of the climate based on a threshold of ± 0.5 °C for the Oceanic Niño Index (ONI) |
| OUTAGE.START.DATE                 | This variable indicates the day of the year when the outage event started (as reported by the corresponding Utility in the region) |
| OUTAGE.START.TIME                 | This variable indicates the time of the day when the outage event started (as reported by the corresponding Utility in the region) |
| OUTAGE.RESTORATION.DATE           | This variable indicates the day of the year when power was restored to all the customers (as reported by the corresponding Utility in the region) |
| OUTAGE.RESTORATION.TIME           | This variable indicates the time of the day when power was restored to all the customers (as reported by the corresponding Utility in the region) |
| CAUSE.CATEGORY                    | Categories of all the events causing the major power outages |
| CAUSE.CATEGORY.DETAIL             | Detailed description of the event categories causing the major power outages |
| HURRICANE.NAMES                   | If the outage is due to a hurricane, then the hurricane name is given by this variable |
| OUTAGE.DURATION                   | Duration of outage events (in minutes) |
| DEMAND.LOSS.MW                   | Amount of peak demand lost during an outage event (in Megawatt) [but in many cases, total demand is reported] |
| CUSTOMERS.AFFECTED                | Number of customers affected by the power outage event |
| RES.PRICE                         | Monthly electricity price in the residential sector (cents/kilowatt-hour) |
| COM.PRICE                         | Monthly electricity price in the commercial sector (cents/kilowatt-hour) |
| IND.PRICE                         | Monthly electricity price in the industrial sector (cents/kilowatt-hour) |
| TOTAL.PRICE                       | Average monthly electricity price in the U.S. state (cents/kilowatt-hour) |
| RES.SALES                         | Electricity consumption in the residential sector (megawatt-hour) |
| COM.SALES                         | Electricity consumption in the commercial sector (megawatt-hour) |
| IND.SALES                         | Electricity consumption in the industrial sector (megawatt-hour) |
| TOTAL.SALES                       | Total electricity consumption in the U.S. state (megawatt-hour) |
| RES.PERCEN                        | Percentage of residential electricity consumption compared to the total electricity consumption in the state (in %) |
| COM.PERCEN                        | Percentage of commercial electricity consumption compared to the total electricity consumption in the state (in %) |
| IND.PERCEN                        | Percentage of industrial electricity consumption compared to the total electricity consumption in the state (in %) |
| RES.CUSTOMERS                     | Annual number of customers served in the residential electricity sector of the U.S. state |
| COM.CUSTOMERS                     | Annual number of customers served in the commercial electricity sector of the U.S. state |
| IND.CUSTOMERS                     | Annual number of customers served in the industrial electricity sector of the U.S. state |
| TOTAL.CUSTOMERS                   | Annual number of total customers served in the U.S. state |
| RES.CUST.PCT                      | Percent of residential customers served in the U.S. state (in %) |
| COM.CUST.PCT                      | Percent of commercial customers served in the U.S. state (in %) |
| IND.CUST.PCT                      | Percent of industrial customers served in the U.S. state (in %) |
| PC.REALGSP.STATE                  | Per capita real gross state product (GSP) in the U.S. state (measured in 2009 chained U.S. dollars) |
| PC.REALGSP.USA                    | Per capita real GSP in the U.S. (measured in 2009 chained U.S. dollars) |
| PC.REALGSP.REL                    | Relative per capita real GSP as compared to the total per capita real GDP of the U.S. (expressed as fraction of per capita State real GDP & per capita US real GDP) |
| PC.REALGSP.CHANGE                 | Percentage change of per capita real GSP from the previous year (in %) |
| UTIL.REALGSP                      | Real GSP contributed by Utility industry (measured in 2009 chained U.S. dollars) |
| TOTAL.REALGSP                     | Real GSP contributed by all industries (total) (measured in 2009 chained U.S. dollars) |
| UTIL.CONTRI                       | Utility industry׳s contribution to the total GSP in the State (expressed as percent of the total real GDP that is contributed by the Utility industry) (in %) |
| PI.UTIL.OFUSA                     | State utility sector׳s income (earnings) as a percentage of the total earnings of the U.S. utility sector׳s income (in %) |
| POPULATION                        | Population in the U.S. state in a year |
| POPPCT_URBAN                      | Percentage of the total population of the U.S. state represented by the urban population (in %) |
| POPPCT_UC                         | Percentage of the total population of the U.S. state represented by the population of the urban clusters (in %) |
| POPDEN_URBAN                      | Population density of the urban areas (persons per square mile) |
| POPDEN_UC                         | Population density of the urban clusters (persons per square mile) |
| POPDEN_RURAL                      | Population density of the rural areas (persons per square mile) |
| AREAPCT_URBAN                     | Percentage of the land area of the U.S. state represented by the land area of the urban areas (in %) |
| AREAPCT_UC                        | Percentage of the land area of the U.S. state represented by the land area of the urban clusters (in %) |
| PCT_LAND                          | Percentage of land area in the U.S. state as compared to the overall land area in the continental U.S. (in %) |
| PCT_WATER_TOT                     | Percentage of water area in the U.S. state as compared to the overall water area in the continental U.S. (in %) |
| PCT_WATER_INLAND                  | Percentage of inland water area in the U.S. state as compared to the overall inland water |

</details>



### Question:

>Out of the various states, which are most likely to experience the most severe power outages, and what are the primary causes?

This analysis centers around understanding the severity of power outages in different states within the United States and uncovering the root causes behind these outages. By identifying states prone to severe outages and the key contributing factors, stakeholders can develop targeted strategies to enhance infrastructure resilience and minimize outage impacts. 

A key thing to define is what a severe power outage is. We decided to define the severity of a power outage by the duration it lasted. This was because we reasoned that worse power outages would be harder to fix and thus take longer to fix. As well, this allowed us to control for things like the population of a state which may affect the number of people affected by an outage.

## Data Cleaning and EDA (Exploratory Data Analysis)

___

### Data Cleaning

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

<details markdown = "1"> 
<summary>&#187; The First Few Rows of the Cleaned Data</summary>

| OBS | YEAR | MONTH | U.S._STATE | POSTAL.CODE | NERC.REGION | CLIMATE.REGION | ANOMALY.LEVEL | CLIMATE.CATEGORY | OUTAGE.START.DATE | OUTAGE.START.TIME | ... | POPDEN_URBAN | POPDEN_UC | POPDEN_RURAL | AREAPCT_URBAN | AREAPCT_UC | PCT_LAND | PCT_WATER_TOT | PCT_WATER_INLAND | OUTAGE.START.DATETIME | OUTAGE.RESTORATION.DATETIME |
|-----|------|-------|------------|-------------|-------------|----------------|---------------|------------------|-------------------|-------------------|-----|--------------|-----------|--------------|----------------|------------|----------|---------------|-----------------|-----------------------|-----------------------------|
| 1   | 2011 | 7.0   | Minnesota  | MN          | MRO         | East North Central | -0.3          | normal           | 2011-07-01        | 17:00:00          | ... | 2279.0       | 1700.5    | 18.2         | 2.14           | 0.60       | 91.592666| 8.407334      | 5.478743        | 2011-07-01 17:00:00   | 2011-07-03 20:00:00         |
| 2   | 2014 | 5.0   | Minnesota  | MN          | MRO         | East North Central | -0.1          | normal           | 2014-05-11        | 18:38:00          | ... | 2279.0       | 1700.5    | 18.2         | 2.14           | 0.60       | 91.592666| 8.407334      | 5.478743        | 2014-05-11 18:38:00   | 2014-05-11 18:39:00         |
| 3   | 2010 | 10.0  | Minnesota  | MN          | MRO         | East North Central | -1.5          | cold             | 2010-10-26        | 20:00:00          | ... | 2279.0       | 1700.5    | 18.2         | 2.14           | 0.60       | 91.592666| 8.407334      | 5.478743        | 2010-10-26 20:00:00   | 2010-10-28 22:00:00         |
| 4   | 2012 | 6.0   | Minnesota  | MN          | MRO         | East North Central | -0.1          | normal           | 2012-06-19        | 04:30:00          | ... | 2279.0       | 1700.5    | 18.2         | 2.14           | 0.60       | 91.592666| 8.407334      | 5.478743        | 2012-06-19 04:30:00   | 2012-06-20 23:00:00         |
| 5   | 2015 | 7.0   | Minnesota  | MN          | MRO         | East North Central | 1.2           | warm             | 2015-07-18        | 02:00:00          | ... | 2279.0       | 1700.5    | 18.2         | 2.14           | 0.60       | 91.592666| 8.407334      | 5.478743        | 2015-07-18 02:00:00   | 2015-07-19 07:00:00         |


</details>




### Univariant Graph

This histogram describes what Outage duration times are most common. It seems that most outage durations are often fairly short, around 0 - 1000 minutes long. 

```py
univariant_plot = px.histogram(data['OUTAGE.DURATION'])
univariant_plot.update_layout(xaxis_title = 'OUTAGE.DURATION in minutes', showlegend = False, title = 'Count of Duration of Outage')
```

<iframe src="static/uni-plot.html" width=800 height=600 frameBorder=0></iframe>


### Bivariant Graph

This bar chart plots the total cumilative sum of outage time in minutes per state. You can see that Michigan and New York have a large cumalitve sum of outage time compared to the other states. 

```py
bivariant = data.groupby('U.S._STATE')['OUTAGE.DURATION'].sum().sort_values().reset_index().plot(kind = 'bar', x ='U.S._STATE' , y= 'OUTAGE.DURATION')

```

<iframe src="static/bi-plot.html" width=800 height=600 frameBorder=0></iframe>


### Interesting Aggregate
Found which states had the most outages

<details markdown="1">
<summary>&#187; Click to expand table</summary>

```py
bivariant = data.plot(kind = 'bar', x = 'U.S._STATE', y = 'OUTAGE.DURATION')
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

</details>

## Assessment Of Missingness

___

### NMAR

**CAUSE.CATEGORY.DETAIL**

All the NAN values in CAUSE.CATEGORY.DETAIL could be NMAR because the type of disaster may affect whether or not the data could be collected. For instance, a severe weather event like heavy rain and hail could occur at the same time and obscure the real cause of the damage. Because of this uncertaintity, this data may not have been collected for certain types of causes which may have coincided. This would cause the missingness of the data to be dependent on what kind of event was occuring and thus it would depend on itself making it NMAR.


### MAR

**Null Hypothesis:**

The missingness of data in the "Customers Affected" column is random with respect to the US states.

**Interpetation of Results** 

The MAR (Missing at Random) permutation test presented here aims to assess whether the "Customers Affected" column in a dataset related to US states is missing randomly or not. This test is crucial in understanding if the absence of data in this column is dependent on "U.S._STATES".

We wrote a function called `mar_permutation` that executes the permutation test to simulate randomness in the missingness of data. It first calculates the observed TVD using the `find_tvd` function. Then, it performs a permutation by shuffling the "Customers Affected" column randomly within the dataset numerous times (default 1000 iterations) and computes the TVD for each shuffled dataset. This creates a distribution of TVD values under the assumption that missingness is random.

We found that the p_value/alpha given was 0, meaning that we would reject the null and say that the missingess of the data "Customers Affected" is MAR with respect to the US States. 


<iframe src="static/mar-hist.html" width=800 height=600 frameBorder=0></iframe>


## Hypothesis Testing

___

**Question:**: What are the states with the worst outages?

To measure how bad an outage is, we used both the outage duration and customers affected as a way to measure how bad the outage is. To evaluate the relationship between power outage severity and specific states in the United States, we conducted a permutation test primarily focused on two variables: "OUTAGE.DURATION" and "CUSTOMERS.AFFECTED," aiming to determine if outage severity differs significantly across various states.

### For OUTAGE.DURATION:

**Null Hypothesis (H0):**
There is no significant difference in average outage durations across different states in the United States. 

**Alternative Hypothesis (H1):**
The alternative hypothesis counters the null hypothesis, suggesting that there exists a significant difference in average outage durations among various states.

### For CUSTOMERS.AFFECTED:

**Null Hypothesis (H0):**
There is no significant difference in the average number of affected customers across different states. 

**Alternative Hypothesis (H1):**
The alternative hypothesis counters the null hypothesis, suggesting that there exists a significant difference in average customers affected among various states in the country.


### Code Explanation

**Test Statistc:**

```py
def calculate_outage_severity(data, state, var):

    output = data.groupby(state).mean()
    
    return output.loc[True,var]
```

Function computes the average outage severity (mean of the variable of interest) for a given state within the dataset. We will use this as our test statistic. 

**Permutation Test Function:**

```py
def perm_test(data, state, var, n=1000):
    #1
    data = data.copy()[["U.S._STATE", var]]
    #2
    data[state] = data["U.S._STATE"] == state
    #3
    obs = calculate_outage_severity(data, state, var)
    test_stats = []
    #4
    for _ in range(n):
        value = np.random.permutation(data[var])
        shuffled = data.assign(**{var : value })
        trial = calculate_outage_severity(shuffled, state, var)
        #5
        test_stats.append(trial)
    #6
    return  (np.array(test_stats) >= obs).mean()

```

- *Data Preparation:*
    1. Extracts relevant columns ("U.S._STATE" and the specified variable) from the dataset.
    2. Creates a boolean column based on whether each row corresponds to a specific state.
- *Permutation Test:*

    3. Calculates the observed outage severity for the specified state and variable.
    4. Repeatedly shuffles the values of the chosen variable (using numpy's permutation function) and recalculates the outage severity for that state.
    5. Records the distribution of outage severity values obtained from shuffling the data.
    6. Computes the proportion of shuffled values greater than or equal to the observed severity, providing the p-value for that specific state.

**Conducting Permutation Tests for All States:**

```py
all_p_values_duration = {}
all_p_values_customers = {}
for i in data['U.S._STATE'].unique():
    all_p_values_duration[i] = perm_test(data, i, "OUTAGE.DURATION")
    all_p_values_customers[i] = perm_test(data, i , "CUSTOMERS.AFFECTED")
```

1. The code iterates through each unique state in the dataset.
For each state, it conducts permutation tests for both "OUTAGE.DURATION" and "CUSTOMERS.AFFECTED," generating p-values for each variable in each state.
2. The resulting p-values are stored in separate dictionaries (all_p_values_duration and all_p_values_customers).


**Conclusion**


```py
initial = pd.DataFrame({'duration_p_value' : pd.Series(all_p_values_duration),
              'customer_p_value' : pd.Series(all_p_values_customers)})

resulting_df = data.groupby('U.S._STATE')[['YEAR']].count().merge(initial, left_index = True, right_index = True).rename(columns = {'YEAR': 'Count of Outages'})

graph_df = resulting_df[(resulting_df['duration_p_value'] < 0.05) | (resulting_df['customer_p_value'] < 0.05 )].sort_values('customer_p_value')
```

| U.S._STATE      | Count of Outages | duration_p_value | customer_p_value |
|-----------------|------------------|------------------|------------------|
| Montana         | 3                | 0.979            | 0.000            |
| South Dakota    | 2                | 0.893            | 0.000            |
| Texas           | 127              | 0.372            | 0.010            |
| California      | 210              | 1.000            | 0.015            |
| Florida         | 45               | 0.069            | 0.017            |
| New York        | 71               | 0.000            | 0.115            |
| West Virginia   | 4                | 0.049            | 0.212            |
| Michigan        | 95               | 0.001            | 0.367            |
| Alaska          | 1                | 0.000            | 0.498            |
| Wisconsin       | 20               | 0.005            | 0.994            |



<iframe src="static/p_value_bar.html" width=800 height=600 frameBorder=0></iframe>



#### Outage Duration and Customer Impact:

1. **Montana and South Dakota**:
   - Despite non-significant differences in outage duration (p-values of 0.979 and 0.893, respectively), both states remarkably impact affected customers (p-value of 0.000 for both).
   - These findings highlight consistent customer impact despite minimal variation in outage durations.

2. **Texas**:
   - Texas exhibits moderately higher outage duration p-values (0.372) but significantly affects customers (p-value of 0.010).
   - This suggests notable implications for affected customers despite moderate variability in outage duration.

3. **California**:
   - Despite non-significant differences in outage duration (p-value of 1.000), California significantly impacts affected customers (p-value of 0.015).
   - This underscores the substantial customer impact despite minimal variations in outage durations.

4. **Florida and New York**:
    - Both states exhibit relatively smaller p-values for both outage duration and affected customers compared to other regions.

    

### Conclusion:

This analysis showcases a trend where states with non-significant differences in outage duration often present more notable impacts on affected customers. However, exceptions like Florida and New York challenge this pattern, displaying significant differences in both outage duration and affected customers. The variability observed across states underlines the intricate dynamics influencing outage durations and their corresponding impact on affected communities.











Clearly state your null and alternative hypotheses, your choice of test statistic and significance level, the resulting 
p
-value, and your conclusion. Justify why these choices are good choices for answering the question you are trying to answer.

Optional: Embed a visualization related to your hypothesis test in your website.

Tip: When making writing your conclusions to the statistical tests in this project, never use language that implies an absolute conclusion; since we are performing statistical tests and not randomized controlled trials, we cannot prove that either hypothesis is 100% true or false.





