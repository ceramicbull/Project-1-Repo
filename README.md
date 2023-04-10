# Project 1
# Analysis of the Relationships Between the Federal Fund Rate, Average Mortgage Rates and Home Prices in the United States

## Introduction
  The US housing market makes up almost 20% of the US GDP. When the real estate market is impacted it has a large effect on the overall economy. This project analyzes the relationships and correlations between the the federal prime loan rate, average mortgage rates and several real estate market variables: median list price, median sales price and home inventory. This analysis should highlight which relationships are positively correlated, negatively correlated or not correlated at all. The results of this analysis could be used to develop market indicators, first phase results for more in-depth analysis of micro-markets and trends and a deeper dive into the impact that significant events over the last five years may have had on the real estate market. 
  
All code is available in the [Group Project Notebook.](https://github.com/ceramicbull/Project-1-Repo/blob/main/Group%20Project%20One%20Notebook.ipynb)
Images have been saved to the [images folder.](https://github.com/ceramicbull/Project-1-Repo/tree/main/images)

## Questions
  There were several questions that guided the first round of analysis for this topic. They were: 
- How does the federal fund rate impact the average home mortgage rate?
- How do home mortgage rates affect/impact median sale price?
- How do home mortgage rates affect/impact listing price?
- How does the mortgage interest rate correlate to days on the market?
- How does the mortgage interest rate correlate to housing inventory?

## Process
The following list categorizes the development of this project:
- Topic
   - Once the topic was chosen, data sources were identified. 
    - Data Sources: 
        - [Zillow Housing Data](https://www.zillow.com/research/data/)
        - [FRED economic data API](https://fred.stlouisfed.org/docs/api/fred/)
- Scope
  - Our scope was determined by our data sources and the length of time available to complete this project.
  - The Zillow data available (cost free) had a time span of five years, introducing a time scope constraint.
  - The FRED economic research data source provides thirty years of data for our chosen variables. 
- Gather data
  - CSV files for median sales price, median list price and home inventory were imported from the Zillow website.
  - An API call to the FRED website was made to extract the Federal Prime Loan Rate and the Average Mortgage Rate.
- Clean data
  - The CSV files and data from the FRED API call were reconfigured into similar dataframes to allow for easy plotting and comparisons.
- Analyze round 1
  - To answer the first set of questions, the prime rate was compared to the average mortgage rate and the avergage mortgage rate was compared to median list price, median sales price and home inventory in separate scatterplots. A correlation coefficient (R-value) was calculated and line graphs were created to visualize these comparisons and determine and correlations. 
- Adjust scope
  - The prime rate and average mortgage rate were to be analyzed for both a five year and 25 year time span to result in a more meaningful correlation between these       two factors. 
  - Median list price and median sales price were to be compared to discover and trends between the two in the five year time span.
  - Median sales price was to be compared to home inventory to gather more meaningful data.
  - Inventory data was to be examined with respect to separate markets rather than the national average.
  - Important dates and events were to be considered when analyzing graphs to speculate possible causations or correlations.
- Analyze Round 2
  - Multi-line graphs were created to compare prime loan rate and average mortgage rate for a five year and 25 year time span for analysis 
  - A multi-line graph was created to compare median list price and median sales price.
  - A scatterplot, r-value and line graph was created to analyze median sales price and home inventory.
  - A multi-line graph was created to compare the prime loan rate and average mortgage rate with respect to relevant dates to visualize. 
  - Multi-line graphs were created to look at the top 25 inventory markets to visualize. 
- Consider constraints
  - Although meaningful insights were a result of this analysis it is noted that the five year time span is a relevant constraint on this project.
  - The time constraint imposed on the project helped define the scope and it is noted that with more time, more analysis would be possible to result in a more             confident conclusion of the findings.
- Further Considerations
  - Looking more closely at significant dates in the last five years with respect to home inventory, median list and median sales price and prime loan and average mortgage rates could result in a causal analysis with a high degree of confidence. 

  
## Analysis
The first analysis of data made the following comparisons: 
- Prime Rate vs. Mortgage Rate
- Mortgage Rate vs. List Price
- Mortgage Rate vs. Sales Price
- Mortgage Rate vs. Inventory

For each consideration a scatter plot was created, a linear regression and correlation coefficient (r-value) was calculated. The results of this first analysis showed that the prime rate and average mortgage rate have a moderate to strong positive linear relationship. This is not surprising considering the interest rate on loans is affected by the prime rate. Of the comparisons made between the mortgage rate and real estate variables, none of them showed a strong linear relationship. 

![image](https://user-images.githubusercontent.com/120599626/230491078-2332ae07-ccc0-425f-9df4-63c56d75e7d5.png)
![prime_mortgae_5_yr](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/5line.png)

| Comparison | R-Value | Relationship |
|------------|---------|--------------|
| Prime Rate vs. Mortgage Rate | 0.67 | Strong positive linear relationship |
| Mortgage Rate vs. List Price | 0.24 | Weak positive linear relationship |
| Mortgage Rate vs. Sales Price | 0.10 | Very weak positive linear relationship |
| Mortgage Rate vs. Inventory   | 0.01 | No linear relationship |

A more appropriate regression line was needed to analyze the relationship between average mortgage rates, median sales price and median list price. A polynomial regresion line was calculated for average mortgage rate vs. median list price and average mortgage rate vs. median sales price. This regression calculation showed a much stronger correlation. Since the results of the inventory vs mortgage rate showed no correlation it was determined that inventory should be compared to other real estate variables to result in meaningful data analysis.  

![median_list_polynomial](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/lr_median_list_polynomial.png)
![MedianPricePolynomial](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/cp_MortgageRatevsMedianPricePolynomial.png)


| Comparison | R-Value | Relationship |
|------------|---------|--------------|
| Mortgage Rate vs. List Price | 0.83 | Very strong positive linear relationship |
| Mortgage Rate vs. Sales Price | 0.65 | Strong positive linear relationship |

It was noted that the r-values for sales price and list price were not as close as expected. A multiline plot was generated to compare list price and sales price to see if there were any obvious factors to explain the differences. The relationship between these two lines appears to be quite similar although a more consistent slope is observed for the sales price while list price ebbs and flows indicitive of micro-markets heavily affected by other external factors. It is notable that there is small period of time where the sales price and list price are almost identical, which points to a seller's market of historical merit. The list price remains high, although sales prices did not continue to increase at the same rate.

![sales_list_comparison](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/lr_sales_list_comparison.png)

Multiline plots were generated to further observe the relationship between average sales price and average mortgage rate. Notable observations about this graph show that from the beginning time point (July 2018) to the first vertical line (January 2021) there is a clear inverse relationship showing a steady increase in average home sales and a steady decrease in mortgage rates. Then follows a slow increase in mortgage rates accompanied by a positive linear increase in sales price until January 2022 when the sales price continues with a positive linear increase while mortgage rates increase sharply until July of 2022, the peak of the sales price. There is a steep decline in both lines for the two months following and then once again in September 2022 the relationship is briefly inverse, although opposite from the beginning of the graph, with a steep increase in mortgage rates and a steep decline in sales prices. Lastly, in November of 2022 the peak mortgage rate is reached and directly after steep declines are observed in both the mortgage rate and sales price. 

![ChangeRelationshipSalesPricevsMortRate](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/cp_ChangeRelationshipSalesPricevsMortRate.png)


| Time Frame | Sales Price | Mortgage Rate | Correlation |
|------------|---------|--------------|-------------------|
| July 2018 - Jan 2021 | Increasing | Decreasing | Negative correlation (inverse) |
| Jan 2021 - Jan 2022 | Increasing | Increasing | Positive correlation |
| Jan 2022 - July 2022 | Increasing | Increasing | Positive correlation |
| July 2022 - Sept 2022   | Decreasing | Decreasing | Positive correlation |
| Sept 2022 - Nov 2022   | Decreasing | Increasing | Negative correlation (inverse) |

Next, the relationship between the average median sales price and home inventory was analyzed to determine to what degree these variables are correlated. A scatterplot graph was created and a linear regression was calculated. The resulting r-value was 0.75, confirming a strong positive linear relationship between home inventory and median sales price. A multiline graph was plotted for further observations. When examining this graph it is apparent that this relationship looks almost identical to a supply and demand curve. This is an expected result considering we are analyzing the real estate market, which is similar to other markets, where buyers and sellers exchange goods and services. To further emphasize, when the inventory of homes is at it's lowest point on the graph (March 2022), median home sales prices are at their highest. When inventory increased, the 6-9 months following, the median sales prices began to decrease.  Considering the fluctuating changes noticed in the relationship between sales price and mortgage rate, it is somewhat of a surprise that the relationship between the home inventory and median sales price for this time period is quite consistent. At this phase in the analysis, this could mean that although the mortgage rate and sales price had a dynamic relationship in this period of time, the real estate market is fairly predictable. Further analysis will likely uncover a more nuanced relationship between the federal fund rate, the average mortgage rate, the average sales price and home inventory in the United States.

![MedianSalePricevsInventoryScatter](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/cp_MedianSalePricevsInventoryScatter.png)
![AverageSalesPrice_HomeInventory](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/cp_AverageSalesPrice_HomeInventory.png)


| Comparison | R-Value | Relationship |
|------------|---------|--------------|
| Home Inventory vs. Sales Price | 0.75 | Strong positive linear relationship |

## Further Considerations
Significant or historical events were identified as interesting and important considerations for the data analyzed. Several of these important dates were aggregated and compared to the prime loan rate and average mortgage rate to visualize any possible correlations. By creating multi-line plots and superimposing significant dates on the same plot a visualization was created for speculation. 

![five_year_historic](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/bc_5yrhistoric.png)

There were many significant events in the United States between 2018 and 2023. Most notably was the Covid 19 pandemic, which had a global impact. In addition there the George Floyd protests against police brutality which deeply impacted the social climate and a particularly volitile political environment which led to the January 6th attack on the capitol. The complexities of the historical events in this five year time span and how they impacted the economy and housing market are incredibly nuanced and outside of the scope of this project, however it is clear there is a relationship between what happens in a society and it's affect on the economy of that society. Further analysis of these events and their impacts on the economy and housing market would be beneficial for a more thorough and complete analysis of the relationships of the prime loan rate, average mortgage rate, median list price, median sales price and home inventory during this time period.  

In addition, the top 25 real estate markets' home inventories were compared to identify any trends our outliers. It appears that Miami, Florida has an atypical home inventory in comparison. Weather disruptions were considered for significant time points with relationship to the Miami home inventory for a first look. Weather disruptions and impacts on real estate variables would be a worthy analysis to continue with a wider scope.

![top_25_miami_outlier](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/bc_Miami.png)

## Conclusion
The time span considered for this analysis had many significant events that likely contributed to changes in the economy and the real estate market. A national state of emergency was declared, a pandemic was endured, a housing shortage was declared, home mortgage rates were at an all time low, social and political conflicts were frequent to name a few. It is assumed that these happenings were the reason for the changes to the market and economy. Further analysis would be needed to draw a causal link with a high degree of confidence but the initial analysis points to a likelihood that is appropriate for an opinion. 

## Sources:
Used for Prime Loan Rate: 
https://fred.stlouisfed.org/series/MPRIME

Used for 30-Year Fixed Rate Mortgage Average for the United States:
https://fred.stlouisfed.org/series/MORTGAGE30US

Pulled CSV's on Median List Prices, Median Sales Prices, Housing Inventory, and Days Pending:
https://www.zillow.com/research/data/

