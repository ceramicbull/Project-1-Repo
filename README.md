# Project 1
# Analysis of the Relationships Between the Federal Fund Rate, Average Mortgage Rates and Home Prices in the United States

## Introduction

## Questions

## Process

## Analysis
The first analysis of data was making the following comparisons: 
- Prime Rate vs. Mortgage Rate
- Mortgage Rate vs. List Price
- Mortgage Rate vs. Sales Price
- Mortgage Rate vs. Inventory

For each consideration a scatter plot was created, a linear regression and correlation coefficient (r-value) was caluculated. The results of this first analysis showed that the prime rate and mortgage rate have a moderate to strong positive linear relationship. This is not surprising considering the interest rate on loans is affected by the prime rate. <> Of the comparisons made between the mortgage rate and real estate variables none of them showed linear relationship. 

![image](https://user-images.githubusercontent.com/120599626/230491078-2332ae07-ccc0-425f-9df4-63c56d75e7d5.png)
![image](https://user-images.githubusercontent.com/120599626/230491024-80a6729f-ab1a-4d05-8667-a8b146013d10.png)


| Comparison | R-Value | Relationship |
|------------|---------|--------------|
| Prime Rate vs. Mortgage Rate | 0.67 | Strong positive linear relationship |
| Mortgage Rate vs. List Price | 0.24 | Weak positive linear relationship |
| Mortgage Rate vs. Sales Price | 0.10 | Very weak positive linear relationship |
| Mortgage Rate vs. Inventory   | 0.01 | No linear relationship |

A more appropriate regression line was needed to analyze the relationship between average mortgage rates, sales price and list price. A polynomial regresion line was calculated for average mortgage rate vs. list price and average mortgage rate vs. sales price. This regression calculation showed a much stronger correlation. Since the results of the inventory vs mortgage rate showed no correlation it was determined that inventory should be compared to other real estate variables to result in meaningful data analysis.  

![image](https://user-images.githubusercontent.com/120599626/230493767-a7047764-e720-4e41-98d6-d264e00c1bd2.png)
![image](https://user-images.githubusercontent.com/120599626/230493840-e294caf1-9f9f-48a5-b107-39b1d70ae6e8.png)


| Comparison | R-Value | Relationship |
|------------|---------|--------------|
| Mortgage Rate vs. List Price | 0.83 | Very strong positive linear relationship |
| Mortgage Rate vs. Sales Price | 0.65 | Strong positive linear relationship |

It was noted that the r-values for sales price and list price were not as close as expected. A multiline plot was generated to compare list price and sales price to see if there were any obvious factors to explain the differences. The relationship between these two lines appears to be quite similar although a more consistent slope is observed for the sales price while list price ebbs and flows indicitive of micro-markets heavily affected by other external factors. It is notable that there is small period of time where the sales price and list price are almost identical, which points to a seller's market. The list price remains high, although sales prices did not continue to increase at the same rate.

![image](https://user-images.githubusercontent.com/120599626/230495850-fc935620-6519-4423-905e-dea219adecb8.png)

Multiline plots were generated to further observe the relationship between average sales price and average mortgage rate. Notable observations about this graph show that from the beginning time point (July 2018) to the first vertical line (January 2021) there is a clear inverse relationship showing a steady increase in average home sales and a steady decrease in mortgage rates. Then follows a slow increase in mortgage rates accompanied by a positive linear increase in sales price until January 2022 when the sales price continues on the positive linear increase and mortgage rates increase sharply until July of 2022, the peak of the sales price. There is a steep decline in both rates for two months following and then once again in September 2022 the relationship is briefly inverse, although opposite from the beginning of the graph, with a steep increase in in mortgage rates and a steep decline in sales prices. Lastly, in November of 2022 the peak mortgage rate is reached and directly after steep declines are observed in both the mortgage rate and sales price. 

![image](https://user-images.githubusercontent.com/120599626/230497460-53f68740-fc83-4cff-8e61-066a06b7ce0f.png)

| Time Frame | Sales Price | Mortgage Rate | Correlation |
|------------|---------|--------------|-------------------|
| July 2018 - Jan 2021 | Increasing | Decreasing | Negative correlation (inverse) |
| Jan 2021 - Jan 2022 | Increasing | Increasing | Positive correlation |
| Jan 2022 - July 2022 | Increasing | Increasing | Positive correlation |
| July 2022 - Sept 2022   | Decreasing | Decreasing | Positive correlation |
| Sept 2022 - Nov 2022   | Decreasing | Increasing | Negative correlation (inverse) |

Next, the relationship between the average median sales price and home inventory was analyzed to determine to what degree these variables are correlated. A scatterplot graph was created and a linear regression was calculated. The resulting r-value was 0.75, confirming a strong positive linear relationship between home inventory and median sales price. A multiline graph was plotted for further observations. When examining this graph it is apparent that this relationship looks almost identical to a supply and demand curve. This is an expected result considering we are analyzing the real estate market, which is like all other markets, a place where buyers and sellers exchange goods and services. To further emphasize, when the inventory of homes is at it's lowest point on the graph (March 2022), median home sales prices are at their highest. When inventory increased, the 6-9 months following, the median sales prices began to decrease.  Considering the flucuating changes noticed in the relationship between sales price and mortgage rate, it is somewhat of a surprise that the relationship between the home inventory and sales price for this time period is quite consistent. At this phase in the analysis, this could mean that the although the mortgage rate and sales price had a dynamic relationship in this period of time, the real estate market is fairly predictable. Further analysis will likely uncover a more nuanced relationship between the federal fund rate, the average mortgage rate, the average sales price and home inventory in the United States.

![image](https://user-images.githubusercontent.com/120599626/230501402-e77223b3-0e52-4de6-903c-cf4533b46ff5.png)
![image](https://user-images.githubusercontent.com/120599626/230501445-720bc931-a499-4b2e-a598-cea9efaa6d2c.png)


| Comparison | R-Value | Relationship |
|------------|---------|--------------|
| Home Inventory vs. Sales Price | 0.75 | Strong positive linear relationship |


## Considerations

![Test image](https://github.com/ceramicbull/Project-1-Repo/blob/main/images/cp_MortgageRatevsMedianPrice.png)


link to project presentation:
https://docs.google.com/presentation/d/1p39E9oMrE0zHUl1MSPLrDNICQNgomjx4eWUpZPXJpIc/edit?usp=sharing

## Sources:
Used for Prime Loan Rate: 
https://fred.stlouisfed.org/series/MPRIME

Used for 30-Year Fixed Rate Mortgage Average for the United States:
https://fred.stlouisfed.org/series/MORTGAGE30US

Pulled CSV's on Median List Prices, Median Sales Prices, Housing Inventory, and Days Pending:
https://www.zillow.com/research/data/

