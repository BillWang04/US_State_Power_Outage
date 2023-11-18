___

## Introduction to the Dataset
___
Due to recent large power outages like the Texas power crisis of 2021, we wanted to investigate the causes and trends in power outages across the United States. The dataset under analysis contains comprehensive information regarding power outages across different states in the United States. Our analysis aims to explore the factors contributing to severe outages, their impact on different states, and the locations where sever outages most often occur. This would give us a better understanding of how power outages occur and how to possibly prevent them in the future.

### Description of Variables

The dataset contains 1534 rows and 55 columns. For this analysis, we decided to only use a few relevent columns. The main variables used and their descriptions are detailed below.

| Variable Name                    | Description |
|-----------------------------------|-------------|
| `U.S._STATE`                        | Represents all the states in the continental U.S. |
| `CLIMATE.CATEGORY`                  | Represents the climate episodes corresponding to the years. The categories are “Warm”, “Cold” or “Normal” episodes of the climate based on a threshold of ± 0.5 °C for the Oceanic Niño Index (ONI) |
| `OUTAGE.START.DATE`                 | This variable indicates the day of the year when the outage event started (as reported by the corresponding Utility in the region) |
| `OUTAGE.START.TIME`                 | This variable indicates the time of the day when the outage event started (as reported by the corresponding Utility in the region) |
| `OUTAGE.RESTORATION.DATE`           | This variable indicates the day of the year when power was restored to all the customers (as reported by the corresponding Utility in the region) |
| `OUTAGE.RESTORATION.TIME`           | This variable indicates the time of the day when power was restored to all the customers (as reported by the corresponding Utility in the region) |
| `CAUSE.CATEGORY.DETAIL`             | Detailed description of the event categories causing the major power outages |
| `CUSTOMERS.AFFECTED`                | Number of customers affected by the power outage event |
| `OUTAGE.DURATION`                   | Duration of outage events (in minutes) |

We have also included the definitions of the 55 various variables/columns that were included in the data below.

<details markdown="1">
<summary>&#187; Click here to see all Variable Descriptions</summary>

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

>Out of the various states, which states experience the most severe power outages?

This analysis centers around understanding the severity of power outages in different states within the United States and uncovering the root causes behind these outages. By identifying states prone to severe outages, stakeholders can develop targeted strategies to enhance infrastructure resilience and minimize outage impacts. 

A key thing to define is what a severe power outage is. We decided to define the severity of a power outage by the duration it lasted. This was because we reasoned that worse power outages would be harder to fix and thus take longer to fix. As well, this allowed us to control for things like the population of a state which may affect the number of people affected by an outage.

## Data Cleaning and EDA (Exploratory Data Analysis)

___

### Data Cleaning

**Combining Date and Time Columns**

In data processing and analysis, there are situations where information related to date and time is stored separately in distinct columns. To facilitate more efficient analysis and computations, it's often beneficial to merge these separate date and time columns into a single datetime column. This combined datetime column provides a unified representation of both date and time, enhancing the clarity and usefulness of the data.

1. Opening and Reading the Data:
We started by accessing the information stored in an Excel file named "outage.xlsx." Using Python along with Pandas, we imported this data into our program. This allowed us to view and manipulate the data within Python for analysis purposes.

2. Identifying and Removing Unnecessary Information:
Within the Excel file, there were some rows and columns that weren't needed for our analysis. Using Python, we removed these unnecessary rows and columns to focus only on the relevant data.

3. Merging Separate Date and Time Columns:
The data contained separate columns for the start date and start time of power outages. To make this information more manageable and useful for analysis, we combined these separate date and time columns into a new single column called "OUTAGE.START.DATETIME." This merging process allowed us to have a complete timestamp for the beginning of each outage event.

4. Similar Procedure for Restoration Timestamp:
Similarly, there were separate columns for the restoration date and time of each outage event. Using the same approach, we merged these columns into a new combined column called "OUTAGE.RESTORATION.DATETIME." This provided a unified timestamp for when power was restored after each outage.

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


<iframe src="static/uni-plot.html" width=800 height=600 frameBorder=0></iframe>


### Bivariant Graph

This bar chart plots the total cumilative sum of outage time in minutes per state. You can see that Michigan and New York have a large cumalitve sum of outage time compared to the other states. 


<iframe src="static/bi-plot.html" width=800 height=600 frameBorder=0></iframe>


### Interesting Aggregate
The table provides a comprehensive overview of power outages across various U.S. states, highlighting the frequency of occurrences.

<details markdown="1">
<summary>&#187; Click to expand table</summary>


| U.S. State           | COUNT |
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

If we would want to collect data that would make this column MAR, what we could do is audit precise conditions of weather, and if there are a lot of weather observations, this could mean that the data collecters couldn't categorize what caused the outage. 

### MAR

**Null Hypothesis:**

The missingness of data in the "Customers Affected" column is random with respect to the US states.

**Interpetation of Results** 

The MAR (Missing at Random) permutation test presented here aims to assess whether the "Customers Affected" column in a dataset related to US states is missing randomly or not. This test is crucial in understanding if the absence of data in this column is dependent on "U.S._STATES".

This is the distribution of Nan and Non -Nan for each state.

<iframe src="static/distr_nan-hist.html" width=800 height=600 frameBorder=0></iframe>

We wrote a function called `mar_permutation` that executes the permutation test to simulate randomness in the missingness of data. It first calculates the observed TVD using the `find_tvd` function. Then, it performs a permutation by shuffling the "Customers Affected" column randomly within the dataset numerous times (default 1000 iterations) and computes the TVD for each shuffled dataset. This creates a distribution of TVD values under the assumption that missingness is random.

We found that the p_value/alpha given was 0, meaning that we would reject the null and say that the missingess of the data "Customers Affected" is MAR with respect to the US States. 


<iframe src="static/mar-hist.html" width=800 height=600 frameBorder=0></iframe>

We also ran a permutation test for the missingness of `CUSTOMERS.AFFECTED` with respect to `CLIMATE.CATEGORY`. We found that `CUSTOMERS.AFFECTED` is likely not missing at random with respect to `CLIMATE.CATEGORY`. This is because the p-value of 0.348 for the observed value is greater than our significance cut-off of 0.05. Therefore it seems likely that `CUSTOMERS.AFFECTED` is MCAR with respect to `CLIMATE.CATEGORY`.

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


### Permutation Test Method

**Test Statistc:**

The `calculate_outage_severity` function computes the average severity of power outages, represented by the mean of a specific variable of interest, within a given state from the dataset. This calculated average serves as our test statistic.


**Data Preparation:**

1. Extracts columns relevant to "U.S._STATE" and the specific variable ("OUTAGE.DURATION" or "CUSTOMERS.AFFECTED").
2. Generates a boolean column indicating whether each data entry corresponds to a specific state.
Permutation Test Steps:
3. Computes the observed outage severity for the chosen state and variable.

**Permutation Test**

1. Repeatedly shuffles the values of the selected variable(either "OUTAGE.DURATION" or "CUSTOMRS.AFFECTED") and recalculates the severity, generating a distribution of possible severity values of the null.
2. Records the distribution of outage severity values obtained from the shuffling process of "OUTAGE.DURATION", "CUSTOMERS.AFFECTED".
3. Computes the proportion of shuffled values greater than or equal to the observed severity, resulting in the p-value for that specific state and variable.

**Conducting Permutation Tests for Each State:**
1. The provided code iterates through each unique state within the dataset, executing permutation tests for "OUTAGE.DURATION" and "CUSTOMERS.AFFECTED" separately.

2. The resulting p-values are stored separately in the dataframe corresponding to each state, enabling access to the p-values for each variable in each state for further analysis and interpretation.




**Conclusion**

| U.S._STATE     | Count of Outages | duration_p_value | customer_p_value |
|----------------|------------------|------------------|------------------|
| Texas          | 127              | 0.372            | 0.010            |
| California     | 210              | 1.000            | 0.015            |
| Florida        | 45               | 0.069            | 0.017            |
| New York       | 71               | 0.000            | 0.115            |
| West Virginia  | 4                | 0.049            | 0.212            |
| Michigan       | 95               | 0.001            | 0.367            |
| Wisconsin      | 20               | 0.005            | 0.994            |



<iframe src="static/p_value_bar.html" width=800 height=600 frameBorder=0></iframe>


A low p-value (typically < 0.05) indicates strong evidence against the null hypothesis, suggesting a significant difference in the mean of outage duration or number of customers affected.

Conversely, a high p-value suggests weaker evidence against the null hypothesis, indicating less significant differences or impacts.


#### Outage Duration and Customer Impact:

**Group 1** - States with Significant Customer Impact but Not on Outage Duration:

Texas, California, Florida

**Group 2** - States with Significant Impact on Outage Duration but Not on Customers:

New York, West Virginia, Michigan, Wisconsin

These groupings categorize states based on their statistical significance concerning outage duration and customer impact, providing insights into the varying impacts of power outages across different regions.


### Conclusion:

The analysis of power outage data across several U.S. states reveals intriguing insights into the varied impacts experienced within different regions. Statistical significance, as indicated by the p-values, offers valuable understanding regarding the effects on outage duration and the number of customers affected. Group 1, consisting of Texas, California, and Florida, demonstrates a significant impact on customers but not on outage duration. Conversely, Group 2, encompassing New York, West Virginia, Michigan, and Wisconsin, showcases a noteworthy impact on outage duration without a substantial effect on the number of affected customers. This distinction highlights the diverse nature of power outages across these states, signifying that certain regions may experience significant disruptions in customer service, while others face prolonged outage durations, regardless of the number of customers affected. Such findings underscore the necessity for tailored strategies in addressing power outage management and mitigation efforts based on the distinct challenges prevalent in different geographical areas. Further exploration and targeted interventions can enhance resilience and minimize disruptions in power supply, catering to the unique requirements of each state.

