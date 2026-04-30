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

Homeownership remains one of the most important pathways to household
wealth-building and long-term financial stability in the United States.
At the same time, recent increases in mortgage interest rates and
housing prices have made homeownership less attainable for many
households, raising important questions about affordability and access
across states. In this report, we examine how changes in mortgage rates
and housing prices relate to homeownership rates over time, with a
particular focus on variation across U.S. states. By identifying the
economic factors most strongly associated with homeownership outcomes,
we aim to provide evidence that can help inform housing policy decisions
at the federal level.

Our analysis is designed to support the policy goals of the U.S.
Department of Housing and Urban Development by clarifying the extent to
which borrowing costs, housing market conditions, and broader economic
variables may influence homeownership. We are especially interested in
whether rising mortgage rates and rising housing prices place measurable
downward pressure on homeownership rates, even after accounting for
other relevant state-level conditions. The findings of this report will
ultimately be used to develop practical policy recommendations that can
help improve housing affordability and expand access to homeownership
for American households.

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

![](README_files/figure-gfm/figure_2-1.png)<!-- -->

\[Discussion of trends over time.\]

### **Correlation Matrix:**

![](README_files/figure-gfm/figure_3-1.png)<!-- -->

\[Discussion of correlation matrix.\]

![](README_files/figure-gfm/figure_4-1.png)<!-- -->

\[Discussion of lines of best fit.\]

![](README_files/figure-gfm/figure_5-1.png)<!-- -->

\[Discussion of box and whisker plots.\]

### **Multicollinearity Check:**

    ##     mortgage_rate               hpi unemployment_rate     median_income 
    ##          1.169637          3.585337          2.272322          3.257880 
    ##       rent_burden   perm_per_person 
    ##          1.927072          1.314518

\[Discussion of multicollinearity check.\]

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

\[Conclusion text here.\]

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

- <https://fred.stlouisfed.org/series/MORTGAGE30US>
- <https://www.fhfa.gov/data/hpi/datasets?tab=quarterly-data>
- <https://www.census.gov/data.html>
- <https://www.bls.gov/web/laus/laumstrk.htm>
