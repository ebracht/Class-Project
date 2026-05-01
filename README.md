Class Project
================

- [Repository Guide](#repository-guide)
- [Introduction](#introduction)
- [Data Summary](#data-summary)
- [Data Analytics](#data-analytics)
  - [**Regression Analysis**](#regression-analysis)
- [Conclusion](#conclusion)
- [Policy Recommendation](#policy-recommendation)
- [Recorded Policy Brief](#recorded-policy-brief)
- [Version Control](#version-control)
- [References](#references)

### **This landing page displays the knitted output of our README.Rmd file. For the code behind the analysis and figures shown below, please consult the README.Rmd file.**

# Repository Guide

This repository contains our group project for Software Tools for Data
Analysis. Our project studies how mortgage interest rates and housing
prices affect homeownership rates across U.S. states over time. The
final audience for this work is Scott Turner, U.S. Secretary of Housing
and Urban Development (HUD).

### Branch Structure

- `main`: current working branch for the final project deliverables
- `Checkpoint-1` branch: preserved as a historical archive of our first
  checkpoint submission
- `Checkpoint-2` branch: preserved as a historical archive of our second
  checkpoint submission

### Repository Contents

- `README.Rmd`: source file for this repository landing page
- `README.md`: knitted GitHub-facing version of the README
- `Data/`: raw and cleaned data files used in the analysis
- `Report Outline.docx`: working outline for the written report
- `README_files/`: figures generated from the README

### Team Workflow

To keep the repository organized, team members should: 1. Pull the most
recent version of the repository before starting work 2. Make changes
locally in the appropriate files 3. Knit `README.Rmd` after updating it
so that `README.md` stays current 4. Commit changes with clear commit
messages 5. Push updates after meaningful progress

### Current Project Responsibilities

- Ryan: Introduction, Data Summary, README/repository instructions
- Levi: Data Analytics
- Liz: Conclusion, Policy Recommendations, repository/class page
  coordination

This README serves as the main landing page for our project progress,
documentation, meeting notes, and selected analysis outputs.

# Introduction

Homeownership remains one of the most important pathways to
wealth-building, stability, and long-term financial security in the
United States. However, recent housing market conditions have made
homeownership increasingly difficult to attain for many families and
individuals. Higher mortgage rates raise the cost of borrowing, while
rising housing prices increase the upfront and long-term financial
burden of purchasing a home. These pressures are especially important
for the U.S. Department of Housing and Urban Development (HUD), which is
responsible for supporting fair, affordable, and sustainable access to
housing across the country.

This report is written for Scott Turner, U.S. Secretary of Housing and
Urban Development. As HUD considers how to address challenges with
affordability, expand access to homeownership, and support stable
housing markets, policymakers need evidence on which factors are most
closely associated with changes in homeownership rates. While mortgage
rates and housing prices are central to the current affordability
discussion, homeownership is also shaped by broader state-level
conditions. Some of these include income, unemployment, rent burden, and
housing supply. For that reason, our analysis examines both the direct
relationship between borrowing costs, housing prices, and homeownership,
as well as the role of additional economic and housing market drivers.

Our research question is: **How do mortgage interest rates, housing
prices, and related state-level economic and housing market conditions
affect homeownership rates across the United States over time?** To
answer this question, we construct a state-year panel dataset covering
U.S. states from 2005 to 2024. We exclude 2020 due to comparability
issues in one-year American Community Survey data during the COVID-19
period. We combine public data from the U.S. Census Bureau, Federal
Reserve Economic Data (FRED), the Federal Housing Finance Agency (FHFA),
the Bureau of Labor Statistics (BLS), and the Census Building Permits
Survey.

The results of this analysis can help HUD evaluate which policy levers
may be most relevant for improving access to homeownership. If
homeownership rates are strongly related to mortgage rates, housing
prices, rent burden, or housing supply, then federal housing policies
can be better targeted toward fixing conditions that most constrain
citizens from purchasing homes. These decisions have consequences beyond
individual buyers: homeownership patterns affect household wealth
accumulation, neighborhood stability, housing market equity, and the
broader economic health of communities.

# Data Summary

To study these relationships, we construct a state-year panel dataset
covering U.S. states from 2005 to 2024, excluding 2020 because one-year
American Community Survey data were not available in a comparable form
during the COVID-19 period. Each observation in the dataset represents
one state in one year. This structure allows us to compare both
differences across states and changes within states over time, making it
well suited for analyzing how economic and housing market conditions are
associated with homeownership outcomes.

The dataset combines several reputable public sources. Homeownership
rates, median income, population, and rent burden are drawn from the
U.S. Census Bureau’s American Community Survey. Mortgage rates come from
the Federal Reserve Economic Data database, while state-level housing
price data come from the Federal Housing Finance Agency House Price
Index. We also include unemployment data from the Bureau of Labor
Statistics and housing permit data from the Census Building Permits
Survey as a proxy for housing supply. After importing, cleaning, and
merging these sources, we use the resulting dataset to examine patterns
in homeownership, affordability, labor market conditions, and housing
supply across states. This combined dataset provides the foundation for
both our descriptive analysis and our regression modeling.

|  | Unique | Missing Pct. | Mean | SD | Min | Median | Max |
|----|----|----|----|----|----|----|----|
| Population | 950 | 0 | 6341021.1 | 7047104.4 | 495226.0 | 4439766.0 | 39557045.0 |
| Median Income | 935 | 0 | 58206.5 | 13858.1 | 32938.0 | 55645.5 | 104828.0 |
| Homeownership Rate | 950 | 0 | 67.0 | 4.4 | 53.0 | 67.5 | 76.3 |
| Mortgage Rate | 19 | 0 | 4.9 | 1.2 | 3.0 | 4.5 | 6.8 |
| Housing Price Index | 949 | 0 | 406.6 | 163.7 | 183.5 | 365.8 | 1229.7 |
| Unemployment Rate | 100 | 0 | 5.3 | 2.1 | 1.8 | 4.7 | 13.5 |
| Rent Burden | 950 | 0 | 44.6 | 4.4 | 28.3 | 44.9 | 58.1 |
| Housing Permits | 932 | 0 | 24953.9 | 35857.7 | 578.0 | 14327.5 | 287250.0 |
| Housing Permits Per Person | 950 | 0 | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 |

\[Discussion of summary stats.\]

### **Plot Histograms of Key Variables:**

![](README_files/figure-gfm/figure_1-1.png)<!-- -->

\[Discussion of histograms.\]

# Data Analytics

### **Key Trends Over Time:**

    ## Warning: `autoplot.tbl_ts()` was deprecated in fabletools 0.6.0.
    ## ℹ Please use `ggtime::autoplot.tbl_ts()` instead.
    ## ℹ Graphics functions have been moved to the {ggtime} package. Please use
    ##   `library(ggtime)` instead.
    ## This warning is displayed once every 8 hours.
    ## Call `lifecycle::last_lifecycle_warnings()` to see where this warning was
    ## generated.

![](README_files/figure-gfm/figure_2-1.png)<!-- --> Figure 2 shows broad
time trends in average state homeownership rates, house price index
values, and 30-year mortgage rates. Average homeownership declined from
the mid-2000s through the mid-2010s, reaching its lowest point around
2014–2015 before gradually recovering in the late 2010s and early 2020s.
Over the same period, the average state house price index increased
substantially, especially after 2020, suggesting that housing prices
rose much faster than homeownership rates recovered.

The mortgage rate trend provides additional context. Mortgage rates
generally declined from the mid-2000s through 2021, but then rose
sharply in the early 2020s. This creates an important policy concern, as
even though homeownership partially recovered after the mid-2010s,
households now face a combination of elevated housing prices and higher
borrowing costs. Together, these trends suggest that homeownership
affordability is shaped by multiple pressures at once rather than by any
single variable alone.

### **Correlation Matrix:**

![](README_files/figure-gfm/figure_3-1.png)<!-- -->

Figure 3, the correlation heatmap provides an initial look at the
relationships among different variables before moving into regression
analysis. Homeownership has negative correlations with population, rent
burden, house price index, median income, and unemployment, suggesting
that states with larger populations, higher housing costs, and greater
rental affordability pressure tend to have lower homeownership rates.
The negative relationship with rent burden is especially important
because it suggests that places where renters face greater financial
strain may also be places where households have more difficulty
transitioning into ownership.

The heatmap also shows several relationships among the explanatory
variables themselves. Median income and house price index have a strong
positive correlation, indicating that higher-income states also tend to
have more expensive housing markets. Rent burden is positively
correlated with population and house price index, which supports the
broader affordability story that larger and more expensive states tend
to place more pressure on renters. These correlations help motivate the
use of multivariable regression, since homeownership is related to
several overlapping economic and housing market conditions rather than
one factor in isolation.

![](README_files/figure-gfm/figure_4-1.png)<!-- -->

Figure 4 compares homeownership rates with several key predictors using
scatterplots and fitted trend lines. The clearest negative relationship
appears between rent burden and homeownership: as rent burden increases,
homeownership rates tend to decline. This supports the idea that states
where renters face greater financial pressure may also be states where
households have more difficulty transitioning into homeownership.

House price index, median income, and unemployment rate also show
negative relationships with homeownership, though the strength and
interpretation of these patterns vary. The negative relationship between
house prices and homeownership is consistent with an affordability
issue, since higher housing costs may make ownership less accessible.
The median income relationship is more complicated because higher-income
states may also be states with substantially higher housing costs,
meaning income alone does not necessarily translate into easier access
to homeownership. Mortgage rates and housing permits per person show
slightly positive trend lines in this figure, but these relationships
should be interpreted cautiously because they do not account for
differences across states, changes over time, or other overlapping
economic conditions.

![](README_files/figure-gfm/figure_5-1.png)<!-- -->

Figure 5 shows the distribution of homeownership rates by state across
the study period. States are ordered by their typical homeownership
rate, making it easy to identify states that consistently have higher or
lower ownership levels. West Virginia, Michigan, Delaware, Maine, and
Minnesota appear near the top of the distribution, while New York,
California, Nevada, Hawaii, and Rhode Island appear near the bottom.

The lower-homeownership states are especially important for HUD because
many of them are large or high-cost housing markets where affordability
challenges are likely more severe. For example, California and New York
have relatively low homeownership rates, which is consistent with the
broader finding that higher housing costs and rent burden are associated
with lower ownership. The chart also shows that some states have wider
ranges than others, meaning homeownership conditions changed more over
time in certain states while remaining more stable in others.

### **Multicollinearity Check:**

    ##     mortgage_rate               hpi unemployment_rate     median_income 
    ##          1.169637          3.585337          2.272322          3.257880 
    ##       rent_burden   perm_per_person 
    ##          1.927072          1.314518

The multicollinearity check suggests that the predictors can be included
together in the regression model without serious multicollinearity
concerns. All variance inflation factor values are below the common
threshold of 5, and well below the stricter threshold of 10, meaning
that none of the predictors appears to be excessively redundant with the
others. The highest values are for house price index and median income,
which makes sense because states with higher incomes often also have
higher housing prices. However, these values are still moderate, so the
model can reasonably estimate the relationship between each predictor
and homeownership while controlling for the others.

## **Regression Analysis**

For directions on how to conduct multilinear regression and plot
confidence intervals, [click
here](https://www.geeksforgeeks.org/r-language/how-to-use-the-coeftest-function-in-r/).

### **Basic Model**

    ## 
    ## Table 1: Simple OLS Regression
    ## ==========================================================
    ##                               Homeownership Rate          
    ## ----------------------------------------------------------
    ## Mortgage Rate                      -1.12***               
    ##                                     (0.20)                
    ##                                                           
    ## N                                    950                  
    ## R2                                   0.96                 
    ## Adjusted R2                          0.96                 
    ## Residual Std. Error            0.87 (df = 882)            
    ## F Statistic                354.97*** (df = 67; 882)       
    ## ==========================================================
    ## Notes:              ***Significant at the 1 percent level.
    ##                      **Significant at the 5 percent level.
    ##                      *Significant at the 10 percent level.

![](README_files/figure-gfm/regression_basic-1.png)<!-- -->

\[Discussion of basic model.\]

### **Model 1**

    ## 
    ## Table 2: OLS Regression with Controls
    ## =================================================================
    ##                                      Homeownership Rate          
    ## -----------------------------------------------------------------
    ## Mortgage Rate                             -2.14***               
    ##                                            (0.60)                
    ##                                                                  
    ## House Price Index                         0.003***               
    ##                                           (0.001)                
    ##                                                                  
    ## Median Income                             -0.0000                
    ##                                           (0.0000)               
    ##                                                                  
    ## Unemployment Rate                         -0.10**                
    ##                                            (0.04)                
    ##                                                                  
    ## Rent Burden                               0.10***                
    ##                                            (0.02)                
    ##                                                                  
    ## Housing Permits per Person                77.27***               
    ##                                           (24.51)                
    ##                                                                  
    ## N                                           950                  
    ## R2                                          0.97                 
    ## Adjusted R2                                 0.96                 
    ## Residual Std. Error                   0.83 (df = 877)            
    ## F Statistic                       362.36*** (df = 72; 877)       
    ## =================================================================
    ## Notes:                     ***Significant at the 1 percent level.
    ##                             **Significant at the 5 percent level.
    ##                             *Significant at the 10 percent level.

![](README_files/figure-gfm/regression_1-1.png)<!-- -->

\[Discussion of model 1.\]

### **Model 2**

    ## 
    ## Table 3: OLS Regression with 3 Lags
    ## =================================================================
    ##                                      Homeownership Rate          
    ## -----------------------------------------------------------------
    ## Mortgage Rate                              -0.13*                
    ##                                            (0.07)                
    ##                                                                  
    ## Lagged Mortgage Rate (1)                  0.22***                
    ##                                            (0.09)                
    ##                                                                  
    ## Lagged Mortgage Rate (2)                    0.07                 
    ##                                            (0.08)                
    ##                                                                  
    ## Lagged Mortgage Rate (3)                  0.60***                
    ##                                            (0.15)                
    ##                                                                  
    ## House Price Index                          0.002*                
    ##                                           (0.001)                
    ##                                                                  
    ## Median Income                              0.0000                
    ##                                           (0.0000)               
    ##                                                                  
    ## Unemployment Rate                          -0.04                 
    ##                                            (0.04)                
    ##                                                                  
    ## Rent Burden                               0.06***                
    ##                                            (0.02)                
    ##                                                                  
    ## Housing Permits per Person               114.42***               
    ##                                           (30.52)                
    ##                                                                  
    ## N                                           800                  
    ## R2                                          0.97                 
    ## Adjusted R2                                 0.97                 
    ## Residual Std. Error                   0.80 (df = 730)            
    ## F Statistic                       339.23*** (df = 69; 730)       
    ## =================================================================
    ## Notes:                     ***Significant at the 1 percent level.
    ##                             **Significant at the 5 percent level.
    ##                             *Significant at the 10 percent level.

![](README_files/figure-gfm/regression_2-1.png)<!-- -->

\[Discussion of model 2.\]

### **Model 3**

    ## 
    ## Table 4: OLS Regression with 2 Lags
    ## =================================================================
    ##                                      Homeownership Rate          
    ## -----------------------------------------------------------------
    ## Mortgage Rate                              -0.13*                
    ##                                            (0.07)                
    ##                                                                  
    ## Lagged Mortgage Rate (1)                  0.22***                
    ##                                            (0.09)                
    ##                                                                  
    ## Lagged Mortgage Rate (2)                    0.07                 
    ##                                            (0.08)                
    ##                                                                  
    ## House Price Index                         0.60***                
    ##                                            (0.15)                
    ##                                                                  
    ## Median Income                              0.002*                
    ##                                           (0.001)                
    ##                                                                  
    ## Unemployment Rate                          0.0000                
    ##                                           (0.0000)               
    ##                                                                  
    ## Rent Burden                                -0.04                 
    ##                                            (0.04)                
    ##                                                                  
    ## Housing Permits per Person                0.06***                
    ##                                            (0.02)                
    ##                                                                  
    ## perm_per_person                          114.42***               
    ##                                           (30.52)                
    ##                                                                  
    ## N                                           800                  
    ## R2                                          0.97                 
    ## Adjusted R2                                 0.97                 
    ## Residual Std. Error                   0.80 (df = 730)            
    ## F Statistic                       339.23*** (df = 69; 730)       
    ## =================================================================
    ## Notes:                     ***Significant at the 1 percent level.
    ##                             **Significant at the 5 percent level.
    ##                             *Significant at the 10 percent level.

![](README_files/figure-gfm/regression_3-1.png)<!-- -->

\[Discussion of model 3.\]

### **Model 4**

    ## 
    ## Table 5: OLS Regression with 1 Lag
    ## =================================================================
    ##                                      Homeownership Rate          
    ## -----------------------------------------------------------------
    ## Mortgage Rate                              -0.13*                
    ##                                            (0.07)                
    ##                                                                  
    ## Lagged Mortgage Rate (1)                  0.22***                
    ##                                            (0.09)                
    ##                                                                  
    ## House Price Index                           0.07                 
    ##                                            (0.08)                
    ##                                                                  
    ## Median Income                             0.60***                
    ##                                            (0.15)                
    ##                                                                  
    ## Unemployment Rate                          0.002*                
    ##                                           (0.001)                
    ##                                                                  
    ## Rent Burden                                0.0000                
    ##                                           (0.0000)               
    ##                                                                  
    ## Housing Permits per Person                 -0.04                 
    ##                                            (0.04)                
    ##                                                                  
    ## rent_burden                               0.06***                
    ##                                            (0.02)                
    ##                                                                  
    ## perm_per_person                          114.42***               
    ##                                           (30.52)                
    ##                                                                  
    ## N                                           800                  
    ## R2                                          0.97                 
    ## Adjusted R2                                 0.97                 
    ## Residual Std. Error                   0.80 (df = 730)            
    ## F Statistic                       339.23*** (df = 69; 730)       
    ## =================================================================
    ## Notes:                     ***Significant at the 1 percent level.
    ##                             **Significant at the 5 percent level.
    ##                             *Significant at the 10 percent level.

![](README_files/figure-gfm/regression_4-1.png)<!-- -->

\[Discussion of model 4.\]

### **Compare Models**

    ## 
    ## Table 6: Regression Comparisons)
    ## ==============================================================================================================================
    ##                                                                    Homeownership Rate                                         
    ##                                      OLS                  OLS - 3 Lags             OLS - 2 Lags             OLS - 1 Lag       
    ##                                      (1)                      (2)                      (3)                      (4)           
    ## ------------------------------------------------------------------------------------------------------------------------------
    ## Mortgage Rate                      -2.14***                  -0.13*                 -91.49***                 -5.86***        
    ##                                     (0.60)                   (0.07)                  (20.12)                   (1.27)         
    ##                                                                                                                               
    ## Lagged Mortgage Rate (1)                                    0.22***                  43.69***                 -0.38**         
    ##                                                              (0.09)                   (9.60)                   (0.15)         
    ##                                                                                                                               
    ## Lagged Mortgage Rate (2)                                      0.07                  -30.09***                                 
    ##                                                              (0.08)                   (6.64)                                  
    ##                                                                                                                               
    ## Lagged Mortgage Rate (3)                                    0.60***                                                           
    ##                                                              (0.15)                                                           
    ##                                                                                                                               
    ## House Price Index                  0.003***                  0.002*                  0.002**                  0.002**         
    ##                                    (0.001)                  (0.001)                  (0.001)                  (0.001)         
    ##                                                                                                                               
    ## Median Income                      -0.0000                   0.0000                   0.0000                   0.0000         
    ##                                    (0.0000)                 (0.0000)                 (0.0000)                 (0.0000)        
    ##                                                                                                                               
    ## Unemployment Rate                  -0.10**                   -0.04                    -0.06                   -0.08**         
    ##                                     (0.04)                   (0.04)                   (0.04)                   (0.04)         
    ##                                                                                                                               
    ## Rent Burden                        0.10***                  0.06***                  0.08***                  0.10***         
    ##                                     (0.02)                   (0.02)                   (0.02)                   (0.02)         
    ##                                                                                                                               
    ## Housing Permits per Person         77.27***                114.42***                 91.45***                 91.04***        
    ##                                    (24.51)                  (30.52)                  (29.83)                  (27.69)         
    ##                                                                                                                               
    ## N                                    950                      800                      850                      900           
    ## R2                                   0.97                     0.97                     0.97                     0.97          
    ## Adjusted R2                          0.96                     0.97                     0.97                     0.97          
    ## Residual Std. Error            0.83 (df = 877)          0.80 (df = 730)          0.82 (df = 779)          0.83 (df = 828)     
    ## F Statistic                362.36*** (df = 72; 877) 339.23*** (df = 69; 730) 341.97*** (df = 70; 779) 353.64*** (df = 71; 828)
    ## ==============================================================================================================================
    ## Notes:                                                                                  ***Significant at the 1 percent level.
    ##                                                                                          **Significant at the 5 percent level.
    ##                                                                                          *Significant at the 10 percent level.

\[Comparison of models and selection of model 4 as preffered model.\]

# Conclusion

This project examined how mortgage interest rates, housing prices, and
related economic and housing market variables are associated with
homeownership rates across U.S. states over time. To answer this
question, we constructed a state-year panel dataset combining
homeownership rates, median income, population, rent burden, mortgage
rates, house price index values, unemployment rates, and housing permits
per person. We used descriptive visualizations, correlation analysis,
state-level distribution plots, multicollinearity checks, and regression
models to study both broad trends and more specific relationships among
these variables.

The analysis shows that homeownership rates vary meaningfully across
both time and states. Average homeownership declined from the mid-2000s
into the mid-2010s before partially recovering in the late 2010s and
early 2020s. However, this recovery occurred alongside a sharp rise in
house price index values and, after 2021, a rapid increase in mortgage
rates. This suggests that the current housing environment is shaped by
multiple affordability pressures at once: households face not only
higher home prices, but also higher borrowing costs.

Several patterns from the visual analysis help clarify the broader
story. The correlation heatmap and scatterplots suggest that
homeownership tends to be lower in states with higher population, higher
rent burden, higher house price index values, and higher unemployment.
Rent burden appears especially important because it connects the rental
and ownership sides of the housing market: states where renters are
already financially strained may also be states where households have
more difficulty moving into ownership. The box plot by state also shows
substantial geographic variation, with states such as New York,
California, Nevada, Hawaii, and Rhode Island consistently showing lower
homeownership rates than many other states.

The regression analysis adds further support to the idea that
homeownership is influenced by several overlapping economic and housing
market conditions. Mortgage rates are generally negatively associated
with homeownership, especially in the baseline and controlled models,
which is consistent with the idea that higher borrowing costs reduce
access to ownership. Housing supply, measured through housing permits
per person, appears positively associated with homeownership in the
models, suggesting that states with more residential construction
activity may have stronger ownership outcomes. Rent burden and
unemployment also provide important context, although some relationships
are more complex once controls and lagged variables are included.

There are several limitations to this analysis. First, the project uses
observational data, so the results should be interpreted as associations
rather than definitive causal effects. Second, some variables are
measured at the national level, such as the 30-year mortgage rate, while
others vary by state and year, which limits how precisely we can isolate
state-specific mortgage effects. Third, the exclusion of 2020 due to ACS
comparability issues helps maintain consistency but removes an important
year from the housing market timeline. Finally, our housing supply
measure captures permits rather than completed housing units, so it may
not fully reflect the actual availability of homes.

Future work could improve the analysis by incorporating more localized
data at the county or metropolitan level, adding measures of housing
inventory and new construction completions, and exploring differences by
household income, race, age, or first-time buyer status. Additional
modeling could also test fixed effects more deeply, examine regional
differences, or use causal inference methods to better isolate the
effects of policy-relevant housing market changes.

# Policy Recommendation

Turning to policy, it should first and foremost be the priority to
increase the housing supply, given the robust finding that more permits
per capita result in higher rates of homeownership. To do so, certain
barriers can be reduced. For example, working to update zoning
regulations to streamline the use of land and permit more density and
innovative construction techniques/housing types. It is important not
simply to increase housing generally but to increase affordable housing,
as homeownership rates are lower in largely populated areas where the
rent burden is already high. In addition to increasing the homeownership
rate, increasing access to affordable housing also has a wealth of other
benefits for people. There have been several initiatives at the state
level that can be applied at the federal level to improve homeownership
generally, as well as to help states that are at a lower rate
potentially catch up. Actions like lessening parking requirements,
density limits, and minimum lot sizes for new residential buildings
allow for more financially feasible constructions. Thus, finding ways to
reduce these kinds of restrictive zoning, which are otherwise
contributing to the affordability crisis in the US, may further aid this
endeavor to increase homeownership rates.

With high rent burden correlated with low homeownership, actions should
be taken to also address this renter issue to allow for mobility toward
homeownership for those who want to purchase a house but have
historically financially struggled to do so because of the already large
burden of rent. This could be approached by the development of more
affordable rental properties and/or expanding rental assistance. We also
need to turn to the impact mortgage rates have, with a one percentage
point increase resulting in both an immediate and long-term negative
effect on homeownership. With mortgage rates rising and staying high in
recent years, it may be helpful to expand access to and opportunity for
fixed-rate mortgages at lower rates. Combined, further resources and
energy need to be directed toward the HOME Investment Partnerships
Program, both at the rental (renter and rental construction development)
and homeownership levels.

Specific focus should be given to states with the lowest rates of
homeownership, like California, New York, Nevada, and Hawaii. Those at
the federal level should aim to work with and hear from homeowners,
developers, and local and state legislators to best understand the needs
of those in areas struggling most. Inspiration can also be taken from
successful state policies, especially in states with higher rates of
homeownership, more permits per person, and lower rent burden.

# Recorded Policy Brief

TO BE ADDED BY MAY 11.

# Version Control

\[Version control text here.\]

# References

Federal Housing Finance Agency. (n.d.). *FHFA House Price Index®
datasets*. Retrieved 2026, from
<https://www.fhfa.gov/data/house-price-index>

Federal Reserve Bank of St. Louis. (n.d.). *30-year fixed rate mortgage
average in the United States \[MORTGAGE30US\]*. FRED. Retrieved 2026,
from <https://fred.stlouisfed.org/series/MORTGAGE30US>

U.S. Bureau of Labor Statistics. (n.d.). *Local Area Unemployment
Statistics*. Retrieved 2026, from <https://www.bls.gov/lau/>

U.S. Census Bureau. (n.d.). *American Community Survey data via API*.
Retrieved 2026, from
<https://www.census.gov/programs-surveys/acs/data/data-via-api.html>

U.S. Census Bureau. (n.d.). *Building Permits Survey*. Retrieved 2026,
from <https://www.census.gov/permits>
