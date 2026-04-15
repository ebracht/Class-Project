Class Project
================

- [Class Project](#class-project)
  - [Repository Guide](#repository-guide)
  - [Checkpoint 2: Progress on Eight Major
    Tasks](#checkpoint-2-progress-on-eight-major-tasks)
  - [Research Topic](#research-topic)
  - [Meeting Minutes and Personal
    Contributions](#meeting-minutes-and-personal-contributions)
  - [Load Packages, Setup API Keys, Import
    Data](#load-packages-setup-api-keys-import-data)
  - [**Merge Imported Data:**](#merge-imported-data)
  - [**Compute Summary Statistics**](#compute-summary-statistics)
  - [**Visualizations and Analysis**](#visualizations-and-analysis)
  - [**Regression Analysis**](#regression-analysis)

### **This landing page displays the knitted output of our README.Rmd file. For the code behind the analysis and figures shown below, please consult the README.Rmd file.**

# Class Project

## Repository Guide

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

## Checkpoint 2: Progress on Eight Major Tasks

**1) Propose a research topic**

> This task is complete. Please see Checkpoint 1 or the next section
> below for details.

**2) Create a GitHub repository and establish best practices for team
collaboration**

> We created and have been working in this GitHub repository. Please see
> above for a description of the repository and our workflow/best
> preactices.

**3) Demonstrate merging of multiple data sources**

> By checkpoint 1, we had imported, cleaned, and merged several data
> sources: population and income income data from the Census, home
> ownership data from the Census, the housing price index, unemployment
> data from BLS, and mortgage data from FRED. Since then, we have added
> housing permit data and created a new variable called “Housing Permits
> Per Person.”

**4) Visualize data using Tableau, R, Python, or a combination**

> We have developed many useful polts and visualizations, including:
> histograms, line graphs, a correlation matrix, lines of best fit, box
> plots, and confidence interval plots. These polts were developed in R
> and are displayed below.

**5) Generate meaningful summary statistic (KPIs) of the data**

> We have generated summary statistics for the key variables we intend
> to analyze. We generated summary statistics for all variables added
> since Checkpoint 1.

**6) Submit draft of progress at Checkpoint 1 and Checkpoint 2**

> This branch is our Checkpoint 2 Submission.

**7) Summarize your findings in a short video presentation**

> We are preparing for this and will record in time for the final
> submission.

**8) Publish a detailed, well formatted markdown report of your
analytical story to your GitHub repository**

> We have posted this markdown file to our landing page. It includes
> details on our analytical story. We have also outlined our report,
> please see “Report Outline.docx” in this repository.

## Research Topic

**Our proposed research question is: How have changes in mortgage
interest rates and housing prices affected home ownership rates across
U.S. states over time?**

To study this, we plan to build a panel data set that examines each
state-year on home ownership rate, housing affordability, mortgage
rates, and other relevant variables like median income or unemployment
rate. Our primary data sources will be the U.S. Census Bureau and the
Federal Reserve Economic Data (FRED), which includes state home
ownership rates and the 30-year fixed mortgage rate. Additionally, the
Federal Housing Finance Agency’s House Price Index, which provides
state-level data on house price changes, and the Bureau of Labor
Statistics, which has state-level data on unemployment, will be pulled.
Together, these sources will provide panel data that can be used to
examine how rising mortgage rates and increasing prices affect home
ownership, while allowing room for controls like unemployment, median
income, or population, to understand this effect better.

Once we have established the relationship between mortgage interest
rates, housing affordability, and home ownership rates, we will consider
what policy options or levers are available to improve home ownership
rates. We may do this by conducting additional primary analysis to test
the efficacy of certain policies where data are available, or by
consulting the relevant literature to form reasonable conclusions about
the linkages between various housing policies and mortgage
rates/affordability. Once we have identified policy recommendations, we
will present these to the U.S. Secretary of Housing and Urban
Development, Scott Turner.

The Secretary of Housing and Urban Development (HUD) manages the
Department of Housing and Urban Development, with responsibilities
including the creation and oversight of affordable housing policies and
programs and advising the President on housing issues. As our ultimate
aim is to contribute to improving home ownership rates, we will explore
the various economic indicators that may positively or negatively impact
this, strategically analyzing these relationships in order to make
predictions and recommendations for affecting future policy change.
Secretary Turner has the power to act on these recommendations, with his
actions guided by a goal of creating affordable housing policy. Our work
exploring home ownership rates is well-aligned not only with this goal,
but also Turner’s previous efforts on opportunity zones. Thus, Scott
Turner is the key figure whom we will focus the implications of our
findings toward. We plan to create these visualizations using a mix of
software programs (including R and Tableau) to create easily and quickly
digestible visualizations that best inform and support our
recommendations.

**Sources:**

- <https://fred.stlouisfed.org/series/MORTGAGE30US>
- <https://www.fhfa.gov/data/hpi/datasets?tab=quarterly-data>
- <https://www.census.gov/data.html>
- <https://www.bls.gov/web/laus/laumstrk.htm>

## Meeting Minutes and Personal Contributions

### **Meeting 1 (02/25):**

Initial meeting of Liz, Ryan, and Levi; we decided on a weekly meeting
time, went through the requirements for the project, and established a
shared document. We planned to each pitch an idea (i.e., provide a brief
description and data source links) in advance of our next meeting, at
which we hoped to narrow in on a topic.

### **Meeting 2 (03/04):**

**Ideas**

- Levi: Minimum Wage/Food Security/Poverty Programs
  - Description: The Center for Poverty Research compiled an impressive
    and easy-to-use dataset with information on state policies such as
    the minimum wage, SNAP, EITC, and so on. I propose using this
    dataset to measure whether/how these policies have influenced
    variables of interest such as poverty, employment, or food
    insecurity. The data set is fairly comprehensive (part of the
    appeal), but I think it would be easy to find opportunities to
    supplement it with other datasets. For example, the food insecurity
    data in the Center for Poverty Research dataset only goes up
    to 2001. If we wanted to look at how state economic policies have
    influenced food insecurity over the past two decades, we would need
    to pull in another dataset. I just filled out an online form offered
    by Feeding America to request access to their food insecurity data
    (available at the state level). They agreed to share it with us, so
    that’s one option. I can think of plenty of other options, too. For
    example, we could pull in Census data (I have experience scraping
    Census data with R using an API key) to analyze whether these
    policies influenced the ratio of people that own vs rent their
    homes. Generally speaking, these analyses would require rigorous
    controls, so there would be ample opportunity to pull in multiple
    datasets to try and control for other factors that may influence
    these endpoints.  
  - Potential data sources:  
    - **National Welfare Data:** “The Center for Poverty Research
    annually updates our state-level panel data series covering
    population, employment, unemployment, welfare, poverty, and
    politics. Our current update includes information for the majority
    of the 2024 calendar year. We will update the remainder when
    available. These data are publicly available to all users.”  
    - Link: <https://ukcpr.uky.edu/resources>  
    - **Feeding America Food Insecurity Data:** “Since 2011, Feeding
    America has produced the Map the Meal Gap study, providing estimates
    of local food insecurity and food costs on an annual basis to better
    understand people and places facing hunger and to inform decisions
    and actions that will help us achieve our mission. We do this by
    generating national and local data about food insecurity,
    translating those data into insights and tools like the interactive
    map below, and engaging partners to help them use and improve our
    data and research in the future.”  
    - Link: <https://map.feedingamerica.org/>
- Liz: Accessibility to alcohol’s relationship to levels of binge
  drinking in a given (Iowa) county
  - Description: The Iowa Department of Health and Human Services has
    already launched a new campaign called Say “Yes” to Drinking Less
    Alcohol, to combat high rates of binge drinking. Aiming to
    investigate whether factors like accessibility to alcohol are
    correlated to higher levels of binge drinking could inform where to
    best focus future resources and interventions. Targeted campaigns
    and/or subsequent action by Iowa Department of Health and Human
    Services, in conjunction with community partners, in areas that show
    higher levels of average binge drinking could aid in the ultimate
    goal of improving health, safety, and alcohol responsibility in
    Iowa. We could compare the rate across states, explore whether/how
    the severity has changed over time, and look into the local data
    from class to compare behavioral data to accessibility (e.g.,
    looking at number of stores in a given area) and purchase rates at a
    county level.  
  - Potential data sources:  
    - **Class Data on Iowa Liquor Sales:** would provide specific store
    location as well as county-by-county info and sales stats  
    - Link:
    <https://data.iowa.gov/Sales-Distribution/Iowa-Liquor-Sales/m3tr-qhgy/about_data>  
    - **U.S. National Health Stats Ranking:** allow for the
    contextualization of a focus on Iowa and make clear the imminent
    need for further work aimed at lowering binge drinking levels;
    provides national excess drinking data.  
    - Link:
    <https://www.americashealthrankings.org/explore/measures/ExcessDrink/IA>  
    - **Behavioral Risk Factor Surveillance System (BRFSS) Data:**
    provides past years’ BRFSS data; this is used to measure progress
    toward health goals and is conducted annually in Iowa. Iowa BRFSS
    survey data supports the creation and implementation of public
    health activities and, per the Iowa Health and Human Services
    website, “aims to reducing chronic diseases and other leading causes
    of death for Iowans.”  
    - Link: <https://hhs.iowa.gov/about/data-reports/brfss>
- **Ryan: Housing Costs, Interest Rates, and home ownership in the
  U.S.**
  - Description: My idea is to study how mortgage interest rates and
    housing prices affect home ownership rates across states. We could
    combine Census housing data, FRED mortgage rates, and FHFA house
    price indexes to build a panel dataset and estimate how changes in
    borrowing costs and housing prices influence home ownership or rent
    burden over time. One potential research question would be: How do
    changes in mortgage interest rates and housing prices affect home
    ownership rates across U.S. states over time? Data should be
    relatively easy to access and merge. Housing outcomes are influenced
    by many economic factors, so we could add controls like median
    income, unemployment rates, or population growth to isolate the
    effect of interest rates and housing prices. We could explore
    regional differences, like if changes in interest rates affect home
    ownership differently in high-cost housing markets compared to more
    affordable states. We’d probably create a panel dataset that
    observes states over time, so each state-year would be an
    observation. The panel would track how home ownership rates change
    as mortgage rates, housing prices, and other economic variables
    change.  
  - Potential data sources:  
    - **Home ownership and Housing Data:** The U.S. Census Bureau
    provides state and national data on home ownership rates, housing
    costs, median home values, rent burdens, and other housing market
    indicators. These data are available through FRED.  
    - Link:
    <https://fred.stlouisfed.org/searchresults/?st=homeownership%20rates%20by%20state>  
    - Link: <https://fred.stlouisfed.org/series/RSAHORUSQ156S>  
    - **Mortgage Interest Rate Data:** The Federal Reserve Economic Data
    (FRED) database provides historical mortgage interest rates and
    other macroeconomic indicators that can be merged with housing data
    to analyze how changes in borrowing costs affect housing outcomes.  
    - Link: <https://fred.stlouisfed.org/series/MORTGAGE30US>  
    - **Housing Price Index Data:** The Federal Housing Finance Agency
    (FHFA) provides a House Price Index with quarterly and annual data
    on housing price changes at the state and metropolitan levels.  
    - Link: <https://www.fhfa.gov/data/hpi/datasets?tab=quarterly-data>

**Discussion:** After talking through the ideas, Levi pointed out that
Ryan’s idea had overlap with the Federal Reserve data that we had to use
for R HW 3. We agreed to proceed with that topic and aimed to think
about it in parallel with the homework. We each tried to merge data sets
to make sure we had the skill to do so moving forward.

### **Meeting 3 (03/11)**

We finalized our decision to focus on Ryan’s proposed topic, and
prepared for our topic submission due 03/13. In preparation, we split up
the work as such:

- Ryan will submit the topic on Canvas course page  
- All will work on respective sections
  - Levi: Process of choosing a topic, opportunities to expand.
  - Liz: Policy implications Scott Turner HUD
  - Ryan: Topic (research question, data sources)  
- Levi will inform Bangjun (former group member) of the plan to log
  notes in this document rather than sending weekly emails  
- Liz will create a GitHub page, will add everyone as collaborators &
  email Prof Chale with a status update about a potential issue
- Ryan will upload a file joining Census and FRED data, including a loop
  to bring in multiple years of Census data  
- Levi will investigate data availability for controlling for state
  housing policy

### **Meeting 4 (03/18)**

We talked through the Checkpoint 1 criteria and made the following plan
in advance of Meeting 5:  
- Work on README/update on Github (update on personal contributions, add
progress updates for each checkpoint, etc.)  
- Try to run code that someone else posted on github and become more
familiar with platform/collaborative repositories  
- If possible, try to create simple visualizations  
- Date to keep in mind: April 14th (project draft is due)

### **Meeting 5 (03/25)**

We discussed our progress on using our collaborative github repo. We
also brainstormed ideas about additional potential directions in
response to the feedback we received on our topic submission earlier in
the week. We then divided up remaining tasks necessary for the
Checkpoint 1 submission as follows:

- Liz: Add remaining (Meeting 5) updates; fix formatting (adjust
  headers, resolve spacing issues, add bullets, etc.); clean
  up/formalize wording of notes where necessary
- Levi: Fill in progress on 8 major tasks and submission  
- Ryan: Create histogram plots of variable and move to README

In advance of Meeting 6, we plan to look into:  
- Potential variables to control for like state housing policies
(explore law atlas data sets)  
- How home ownership impacts wealth for households, per topic submission
feedback  
- Lags in mortgage and home ownership rates

### **Meeting 6 (03/30)**

We reviewed the feedback on our Checkpoint 1 submission and the what we
need to work on for Checkpoint 2. In advance of our meeting next week,
we made a list of the following action items to address the feedback and
begin preparing to work towards Checkpoint 2:

- Liz: Import repository to group page and update README
  - If time, look into using the integrated GitHub Project tool  
- Levi: In the README include descriptions of where to find files  
- Ryan: Clean repositor and make image file names more descriptive  
- All: Try to get more familiar working with datasets we plan to use

### **Meeting 7 (04/06)**

We discussed progress we had made since our last meeting. Liz was
coordinating with Professor Chale on how to import our repository to the
group page. Ryan created several additional figures to inform the data
summary and test for missingness and multicolinearity. Levi created a
multilinear regression model and tested variable significance with and
without clustered standard errors. To prepare for Checkpoint 2, we
assigned each person to (a) section(s) of the report for the purposes of
drafting the outline. Those assignments and other next steps are as
follows:

- Report Outline
  - Intro (Ryan)
  - Data Summary (Ryan)
  - Data Analytics (Levi)
  - Conclusion (Liz)
  - Policy Recommendations (Liz)
- Sort out repository on class page (Liz email prof)
- Add detailed instructions of repository on README (Ryan)
- Develop additional regression models for Data Analytics section (Levi)
- Updating Readme notes (All)
  - Meeting to meeting
  - Contributions
- Check in on submission/last steps next week

### **Meeting 8 (04/13)**

We again discussed progress we had made since our last meeting. We
assessed what remained before our Checkpoint 2 submission due Wednesday
(04/15):

- Fix formatting of and update meeting/contribuion notes (Liz)  
- Clean data labels (Liz)  
- Shorten regression tables (Levi)  
- Knit latest version of README (Ryan)  
- Finalize outline (Liz - add section/read over & finalize)  
- Update on eight major tasks (Levi)  
- Create Checkpoint 2 branch before submitting / submit (Levi)

## Load Packages, Setup API Keys, Import Data

### **Load Required Packages:**

- tidyverse
- janitor
- readr
- readxl
- tidycensus
- fredr
- lubridate
- tsibble
- fpp3

### **Set API Keys:**

- [tidycensus api key](https://api.census.gov/data/key_signup.html)
- [fredr api key](https://fred.stlouisfed.org/docs/api/api_key.html)

### **Import Data:**

## **Merge Imported Data:**

``` r
#Merge the data sets by year and state
merged <- left_join(
  population,
  income,
  by = c("state", "year")
) %>%
  left_join(
    homeownership,
    by = c("state", "year")
  ) %>%
  left_join(
    hpi_annual,
    by = c("state", "year")
  ) %>%
  left_join(
    state_unemployment,
    by = c("state", "year")
  ) %>%
  left_join(
    rent_burden,
    by = c("state", "year")
  ) %>%
  left_join(
    permits_state,
    by = c("state", "year")
  ) %>%
  left_join(
    mortgage_annual,
    by = "year"
  )
```

## **Compute Summary Statistics**

### **Compute Population Summary Statistics:**

    ## Summary statistics for population:

    ##     Min.  1st Qu.   Median     Mean  3rd Qu.     Max. 
    ##   495226  1814815  4439766  6341021  7321456 39557045

    ## Standard Deviation: 7047104

    ## Variance: 4.966168e+13

### **Compute Median Income Summary Statistics:**

    ## Summary statistics for median income:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   32938   47449   55646   58206   66919  104828

    ## Standard Deviation: 13858.12

    ## Variance: 192047587

### **Compute Home Ownership Rate Summary Statistics:**

    ## Summary statistics for homeownership rate:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   52.98   65.03   67.51   66.96   70.01   76.30

    ## Standard Deviation: 4.429418

    ## Variance: 19.61974

### **Compute Mortgage Rate Summary Statistics:**

    ## Summary statistics for mortgage rate:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   2.958   3.936   4.545   4.864   6.027   6.807

    ## Standard Deviation: 1.152201

    ## Variance: 1.327568

### **Compute HPI Summary Statistics**

    ## Summary statistics for HPI:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   183.5   286.2   365.8   406.6   473.6  1229.7

    ## Standard Deviation: 163.7395

    ## Variance: 26810.63

### **Compute Unemployment Summary Statistics**

    ## Summary statistics for Unemployment:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   1.800   3.700   4.700   5.262   6.500  13.500

    ## Standard Deviation: 2.131641

    ## Variance: 4.543892

### **Compute Rent Burden Summary Statistics:**

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   28.27   41.79   44.88   44.62   47.51   58.14

    ## Standard Deviation: 4.371337

    ## Variance: 19.10859

### **Compute Rent Burden Summary Statistics:**

    ##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
    ## 0.0006658 0.0023149 0.0033322 0.0040016 0.0050923 0.0200430

    ## Standard Deviation: 0.002469807

    ## Variance: 6.099947e-06

## **Visualizations and Analysis**

### **Plot Histograms of Key Variables:**

![](README_files/figure-gfm/figure_1-1.png)<!-- -->

### **Plot Mortgage Rate and National Average Homeownership Rate:**

![](README_files/figure-gfm/figure_2-1.png)<!-- -->

### **Correlation Matrix:**

![](README_files/figure-gfm/figure_3-1.png)<!-- -->

### **Missingness Check:**

    ## # A tibble: 8 × 2
    ##   variable           missing_count
    ##   <chr>                      <int>
    ## 1 homeownership_rate             0
    ## 2 median_income                  0
    ## 3 population                     0
    ## 4 hpi                            0
    ## 5 unemployment_rate              0
    ## 6 mortgage_rate                  0
    ## 7 rent_burden                    0
    ## 8 perm_per_person                0

### **Other Plots:**

![](README_files/figure-gfm/figure_4-1.png)<!-- -->

![](README_files/figure-gfm/figure_5-1.png)<!-- -->

### **Multicollinearity Check:**

    ##     mortgage_rate               hpi unemployment_rate     median_income 
    ##          1.169637          3.585337          2.272322          3.257880 
    ##       rent_burden   perm_per_person 
    ##          1.927072          1.314518

### **Create Lag Variables:**

``` r
#Create lag variables
merged <- merged %>%
  arrange(state, year) %>%
  group_by(state) %>%
  mutate(
    mortgage_rate_lag1 = lag(mortgage_rate, 1),
    mortgage_rate_lag2 = lag(mortgage_rate, 2),
    mortgage_rate_lag3 = lag(mortgage_rate, 3),
    hpi_lag1 = lag(hpi, 1),
    hpi_lag2 = lag(hpi, 2),
    hpi_lag3 = lag(hpi, 3)
  ) %>%
  ungroup()
```

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
