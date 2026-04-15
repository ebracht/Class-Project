Class Project
================

- [Class Project](#class-project)
  - [Repository Guide](#repository-guide)
  - [Checkpoint 1: Progress on Eight Major
    Tasks](#checkpoint-1-progress-on-eight-major-tasks)
  - [Research Topic](#research-topic)
  - [Meeting Minutes and Personal
    Contributions](#meeting-minutes-and-personal-contributions)
  - [Load Packages, Setup API Keys, Import
    Data](#load-packages-setup-api-keys-import-data)
  - [**Compute Summary Statistics**](#compute-summary-statistics)
  - [**Create Visualizations**](#create-visualizations)

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

## Checkpoint 1: Progress on Eight Major Tasks

**1) Propose a research topic**

> Each team member proposed a thoughtful research topic along with
> relevant data sources. After deliberation (see meeting minutes below),
> our team chose to study how mortgage rates influence home ownership
> rates across the U.S. To study this topic, our team is constructing a
> panel dataset comprised of several reliable data sources including
> data from the U.S. Census Bureau, FRED, and BLS. We will organize our
> findings to Scott Turner, Secretary of Housing and Urban Development
> (HUD), to inform U.S. housing policy decisions.

**2) Create a GitHub repository and establish best practices for team
collaboration**

> We have created a GitHub repository. Each member has made substantial
> contributions. Thus far, we have included the following in this
> repository: the project topic, meeting minutes, information on the
> packages and API keys needed for analysis, code to import relevant
> data, summary statistics for key variables, and several helpful
> visualizations.

**3) Demonstrate merging of multiple data sources**

> To construct our panel dataset, we have imported, cleaned, and merged
> several data sources: population and income income data from the
> Census, home ownership data from the Census, the housing price index,
> unemployment data from BLS, and mortgage data from FRED.

**4) Visualize data using Tableau, R, Python, or a combination**

> We have used R to create several figures, including line graphs and
> histograms to accompany the summary statistics.

**5) Generate meaningful summary statistic (KPIs) of the data**

> We have generated summary statistics for the key variables we intend
> to analyze.

**6) Submit draft of progress at Checkpoint 1 and Checkpoint 2**

> This branch is our Checkpoint 1 Submission.

**7) Summarize your findings in a short video presentation**

> We will make progress on this in the coming weeks.

**8) Publish a detailed, well formatted markdown report of your
analytical story to your GitHub repository**

> We have posted this markdown file to our landing page. This will
> become the basis of our report.

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

## Load Packages, Setup API Keys, Import Data

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

### **Import online data:**

### **Import local data:**

**Merge imported data:**

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

### **Compute population summary statistics:**

    ## Summary statistics for population:

    ##     Min.  1st Qu.   Median     Mean  3rd Qu.     Max. 
    ##   495226  1814815  4439766  6341021  7321456 39557045

    ## Standard Deviation: 7047104

    ## Variance: 4.966168e+13

### **Compute median income summary statistics:**

    ## Summary statistics for median income:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   32938   47449   55646   58206   66919  104828

    ## Standard Deviation: 13858.12

    ## Variance: 192047587

### **Compute home ownership rate summary statistics:**

    ## Summary statistics for homeownership rate:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   52.98   65.03   67.51   66.96   70.01   76.30

    ## Standard Deviation: 4.429418

    ## Variance: 19.61974

### **Compute mortgage rate summary statistics:**

    ## Summary statistics for mortgage rate:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   2.958   3.936   4.545   4.864   6.027   6.807

    ## Standard Deviation: 1.152201

    ## Variance: 1.327568

### **Compute HPI summary statistics**

    ## Summary statistics for HPI:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   183.5   286.2   365.8   406.6   473.6  1229.7

    ## Standard Deviation: 163.7395

    ## Variance: 26810.63

### **Compute unemployment summary statistics**

    ## Summary statistics for Unemployment:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   1.800   3.700   4.700   5.262   6.500  13.500

    ## Standard Deviation: 2.131641

    ## Variance: 4.543892

### **Compute rent burden summary statistics:**

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   28.27   41.79   44.88   44.62   47.51   58.14

    ## Standard Deviation: 4.371337

    ## Variance: 19.10859

### **Compute rent burden summary statistics:**

    ##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
    ## 0.0006658 0.0023149 0.0033322 0.0040016 0.0050923 0.0200430

    ## Standard Deviation: 0.002469807

    ## Variance: 6.099947e-06

## **Create Visualizations**

### **Plot histograms of key variables:**

![](README_files/figure-gfm/figure_1-1.png)<!-- -->

### **Plot mortgage rate and national average homeownership rate:**

![](README_files/figure-gfm/figure_2-1.png)<!-- -->

### **Correlation Matrix:**

![](README_files/figure-gfm/figure_3-1.png)<!-- -->

### **Missingness check:**

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

### **Other plots:**

![](README_files/figure-gfm/figure_4-1.png)<!-- -->

![](README_files/figure-gfm/figure_5-1.png)<!-- --> \## **Analysis**
\### **Multicollinearity check:**

    ##     mortgage_rate               hpi unemployment_rate     median_income 
    ##          1.169637          3.585337          2.272322          3.257880 
    ##       rent_burden   perm_per_person 
    ##          1.927072          1.314518

### **Regression Analysis**

For directions on how to conduct multilinear regression and plot
confidence intervals, [click
here](https://www.geeksforgeeks.org/r-language/how-to-use-the-coeftest-function-in-r/).

#### **Basic Model**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + state + as.factor(year), 
    ##     data = merged)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -3.8234 -0.4618  0.0261  0.5014  3.0166 
    ## 
    ## Coefficients: (1 not defined because of singularities)
    ##                      Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          77.59302    1.29806  59.776  < 2e-16 ***
    ## mortgage_rate        -1.11789    0.20337  -5.497 5.07e-08 ***
    ## stateAlaska          -5.03879    0.28189 -17.875  < 2e-16 ***
    ## stateArizona         -3.98822    0.28189 -14.148  < 2e-16 ***
    ## stateArkansas        -3.10119    0.28189 -11.002  < 2e-16 ***
    ## stateCalifornia     -13.95476    0.28189 -49.505  < 2e-16 ***
    ## stateColorado        -3.61318    0.28189 -12.818  < 2e-16 ***
    ## stateConnecticut     -2.40966    0.28189  -8.548  < 2e-16 ***
    ## stateDelaware         2.61941    0.28189   9.292  < 2e-16 ***
    ## stateFlorida         -2.47198    0.28189  -8.769  < 2e-16 ***
    ## stateGeorgia         -4.50394    0.28189 -15.978  < 2e-16 ***
    ## stateHawaii         -10.61771    0.28189 -37.666  < 2e-16 ***
    ## stateIdaho            0.95863    0.28189   3.401 0.000702 ***
    ## stateIllinois        -2.23044    0.28189  -7.912 7.54e-15 ***
    ## stateIndiana          0.55277    0.28189   1.961 0.050200 .  
    ## stateIowa             2.33067    0.28189   8.268 4.98e-16 ***
    ## stateKansas          -2.05397    0.28189  -7.286 7.06e-13 ***
    ## stateKentucky        -1.27967    0.28189  -4.540 6.42e-06 ***
    ## stateLouisiana       -2.78857    0.28189  -9.892  < 2e-16 ***
    ## stateMaine            2.90787    0.28189  10.316  < 2e-16 ***
    ## stateMaryland        -1.98619    0.28189  -7.046 3.71e-12 ***
    ## stateMassachusetts   -6.75162    0.28189 -23.951  < 2e-16 ***
    ## stateMichigan         2.93326    0.28189  10.406  < 2e-16 ***
    ## stateMinnesota        3.22014    0.28189  11.423  < 2e-16 ***
    ## stateMississippi     -0.36356    0.28189  -1.290 0.197478    
    ## stateMissouri        -1.29037    0.28189  -4.578 5.38e-06 ***
    ## stateMontana         -1.06805    0.28189  -3.789 0.000162 ***
    ## stateNebraska        -2.64554    0.28189  -9.385  < 2e-16 ***
    ## stateNevada         -11.77529    0.28189 -41.773  < 2e-16 ***
    ## stateNew Hampshire    2.12143    0.28189   7.526 1.29e-13 ***
    ## stateNew Jersey      -4.62729    0.28189 -16.415  < 2e-16 ***
    ## stateNew Mexico      -0.89055    0.28189  -3.159 0.001636 ** 
    ## stateNew York       -15.30332    0.28189 -54.289  < 2e-16 ***
    ## stateNorth Carolina  -3.29667    0.28189 -11.695  < 2e-16 ***
    ## stateNorth Dakota    -5.09426    0.28189 -18.072  < 2e-16 ***
    ## stateOhio            -2.26167    0.28189  -8.023 3.27e-15 ***
    ## stateOklahoma        -3.23698    0.28189 -11.483  < 2e-16 ***
    ## stateOregon          -6.82778    0.28189 -24.222  < 2e-16 ***
    ## statePennsylvania     0.10262    0.28189   0.364 0.715912    
    ## stateRhode Island    -7.88154    0.28189 -27.960  < 2e-16 ***
    ## stateSouth Carolina   0.32341    0.28189   1.147 0.251576    
    ## stateSouth Dakota    -1.21144    0.28189  -4.298 1.92e-05 ***
    ## stateTennessee       -2.12028    0.28189  -7.522 1.33e-13 ***
    ## stateTexas           -6.71669    0.28189 -23.827  < 2e-16 ***
    ## stateUtah             0.74934    0.28189   2.658 0.007996 ** 
    ## stateVermont          1.99673    0.28189   7.083 2.87e-12 ***
    ## stateVirginia        -2.31778    0.28189  -8.222 7.10e-16 ***
    ## stateWashington      -6.03800    0.28189 -21.420  < 2e-16 ***
    ## stateWest Virginia    4.03283    0.28189  14.306  < 2e-16 ***
    ## stateWisconsin       -1.41935    0.28189  -5.035 5.79e-07 ***
    ## stateWyoming          0.65493    0.28189   2.323 0.020386 *  
    ## as.factor(year)2006   0.99144    0.15243   6.504 1.31e-10 ***
    ## as.factor(year)2007   0.84683    0.15075   5.618 2.60e-08 ***
    ## as.factor(year)2008   0.06457    0.15997   0.404 0.686557    
    ## as.factor(year)2009  -1.66261    0.29672  -5.603 2.81e-08 ***
    ## as.factor(year)2010  -2.53773    0.35928  -7.063 3.29e-12 ***
    ## as.factor(year)2011  -3.47556    0.40448  -8.593  < 2e-16 ***
    ## as.factor(year)2012  -5.00393    0.55690  -8.985  < 2e-16 ***
    ## as.factor(year)2013  -4.96503    0.49493 -10.032  < 2e-16 ***
    ## as.factor(year)2014  -5.15069    0.45764 -11.255  < 2e-16 ***
    ## as.factor(year)2015  -5.47921    0.51920 -10.553  < 2e-16 ***
    ## as.factor(year)2016  -5.63042    0.55758 -10.098  < 2e-16 ***
    ## as.factor(year)2017  -4.54569    0.49217  -9.236  < 2e-16 ***
    ## as.factor(year)2018  -3.83478    0.38629  -9.927  < 2e-16 ***
    ## as.factor(year)2019  -4.32169    0.50265  -8.598  < 2e-16 ***
    ## as.factor(year)2021  -4.07557    0.69499  -5.864 6.38e-09 ***
    ## as.factor(year)2022  -1.43293    0.24488  -5.852 6.86e-09 ***
    ## as.factor(year)2023   0.11205    0.18309   0.612 0.540715    
    ## as.factor(year)2024        NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8688 on 882 degrees of freedom
    ## Multiple R-squared:  0.9642, Adjusted R-squared:  0.9615 
    ## F-statistic:   355 on 67 and 882 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_basic-1.png)<!-- -->

#### **Model 1**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + hpi + median_income + 
    ##     unemployment_rate + rent_burden + perm_per_person + state + 
    ##     as.factor(year), data = merged)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -3.08872 -0.43975 -0.00714  0.47404  3.08047 
    ## 
    ## Coefficients: (1 not defined because of singularities)
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          7.901e+01  3.212e+00  24.599  < 2e-16 ***
    ## mortgage_rate       -2.145e+00  5.987e-01  -3.582 0.000359 ***
    ## hpi                  2.787e-03  8.656e-04   3.220 0.001331 ** 
    ## median_income       -3.841e-06  1.715e-05  -0.224 0.822864    
    ## unemployment_rate   -9.702e-02  3.967e-02  -2.446 0.014646 *  
    ## rent_burden          9.718e-02  1.974e-02   4.924 1.01e-06 ***
    ## perm_per_person      7.727e+01  2.451e+01   3.152 0.001677 ** 
    ## stateAlaska         -4.492e+00  5.201e-01  -8.637  < 2e-16 ***
    ## stateArizona        -4.694e+00  3.090e-01 -15.190  < 2e-16 ***
    ## stateArkansas       -2.907e+00  2.724e-01 -10.673  < 2e-16 ***
    ## stateCalifornia     -1.540e+01  4.332e-01 -35.544  < 2e-16 ***
    ## stateColorado       -4.804e+00  3.980e-01 -12.069  < 2e-16 ***
    ## stateConnecticut    -3.075e+00  5.065e-01  -6.072 1.88e-09 ***
    ## stateDelaware        1.635e+00  3.533e-01   4.626 4.28e-06 ***
    ## stateFlorida        -4.099e+00  3.583e-01 -11.440  < 2e-16 ***
    ## stateGeorgia        -5.052e+00  3.123e-01 -16.178  < 2e-16 ***
    ## stateHawaii         -1.212e+01  4.832e-01 -25.090  < 2e-16 ***
    ## stateIdaho           2.619e-01  2.873e-01   0.912 0.362229    
    ## stateIllinois       -2.340e+00  3.713e-01  -6.302 4.64e-10 ***
    ## stateIndiana         5.335e-01  3.007e-01   1.774 0.076339 .  
    ## stateIowa            2.539e+00  3.285e-01   7.730 2.95e-14 ***
    ## stateKansas         -1.776e+00  3.255e-01  -5.456 6.33e-08 ***
    ## stateKentucky       -1.024e+00  2.742e-01  -3.734 0.000201 ***
    ## stateLouisiana      -2.962e+00  2.831e-01 -10.463  < 2e-16 ***
    ## stateMaine           2.069e+00  3.022e-01   6.848 1.41e-11 ***
    ## stateMaryland       -2.850e+00  5.463e-01  -5.217 2.27e-07 ***
    ## stateMassachusetts  -8.296e+00  4.449e-01 -18.649  < 2e-16 ***
    ## stateMichigan        2.762e+00  3.153e-01   8.761  < 2e-16 ***
    ## stateMinnesota       2.775e+00  4.058e-01   6.839 1.49e-11 ***
    ## stateMississippi    -1.335e-01  2.781e-01  -0.480 0.631284    
    ## stateMissouri       -1.246e+00  2.841e-01  -4.385 1.30e-05 ***
    ## stateMontana        -1.249e+00  2.830e-01  -4.414 1.14e-05 ***
    ## stateNebraska       -2.550e+00  3.311e-01  -7.702 3.61e-14 ***
    ## stateNevada         -1.253e+01  3.557e-01 -35.233  < 2e-16 ***
    ## stateNew Hampshire   1.403e+00  4.566e-01   3.072 0.002194 ** 
    ## stateNew Jersey     -5.707e+00  5.093e-01 -11.205  < 2e-16 ***
    ## stateNew Mexico     -1.023e+00  2.713e-01  -3.770 0.000174 ***
    ## stateNew York       -1.672e+01  3.686e-01 -45.375  < 2e-16 ***
    ## stateNorth Carolina -3.812e+00  2.869e-01 -13.286  < 2e-16 ***
    ## stateNorth Dakota   -4.906e+00  3.483e-01 -14.086  < 2e-16 ***
    ## stateOhio           -2.103e+00  3.015e-01  -6.974 6.05e-12 ***
    ## stateOklahoma       -2.915e+00  2.920e-01  -9.983  < 2e-16 ***
    ## stateOregon         -7.887e+00  3.183e-01 -24.779  < 2e-16 ***
    ## statePennsylvania   -2.248e-01  3.066e-01  -0.733 0.463708    
    ## stateRhode Island   -8.605e+00  3.446e-01 -24.973  < 2e-16 ***
    ## stateSouth Carolina -1.986e-01  2.853e-01  -0.696 0.486568    
    ## stateSouth Dakota   -1.084e+00  3.126e-01  -3.469 0.000548 ***
    ## stateTennessee      -2.455e+00  2.742e-01  -8.953  < 2e-16 ***
    ## stateTexas          -7.144e+00  3.432e-01 -20.813  < 2e-16 ***
    ## stateUtah           -2.412e-02  3.836e-01  -0.063 0.949875    
    ## stateVermont         9.810e-01  3.308e-01   2.966 0.003101 ** 
    ## stateVirginia       -3.037e+00  4.140e-01  -7.337 4.98e-13 ***
    ## stateWashington     -7.127e+00  3.750e-01 -19.005  < 2e-16 ***
    ## stateWest Virginia   4.780e+00  2.833e-01  16.874  < 2e-16 ***
    ## stateWisconsin      -1.528e+00  3.185e-01  -4.796 1.90e-06 ***
    ## stateWyoming         1.214e+00  3.581e-01   3.390 0.000731 ***
    ## as.factor(year)2006  1.492e+00  3.078e-01   4.847 1.48e-06 ***
    ## as.factor(year)2007  1.405e+00  2.387e-01   5.887 5.61e-09 ***
    ## as.factor(year)2008  4.914e-01  1.756e-01   2.798 0.005258 ** 
    ## as.factor(year)2009 -1.980e+00  6.455e-01  -3.067 0.002230 ** 
    ## as.factor(year)2010 -3.264e+00  8.445e-01  -3.865 0.000119 ***
    ## as.factor(year)2011 -4.523e+00  1.005e+00  -4.500 7.73e-06 ***
    ## as.factor(year)2012 -6.868e+00  1.481e+00  -4.639 4.04e-06 ***
    ## as.factor(year)2013 -6.582e+00  1.305e+00  -5.045 5.51e-07 ***
    ## as.factor(year)2014 -6.719e+00  1.211e+00  -5.550 3.78e-08 ***
    ## as.factor(year)2015 -7.384e+00  1.423e+00  -5.188 2.65e-07 ***
    ## as.factor(year)2016 -7.760e+00  1.560e+00  -4.973 7.92e-07 ***
    ## as.factor(year)2017 -6.415e+00  1.386e+00  -4.628 4.25e-06 ***
    ## as.factor(year)2018 -5.256e+00  1.080e+00  -4.865 1.35e-06 ***
    ## as.factor(year)2019 -6.356e+00  1.484e+00  -4.284 2.04e-05 ***
    ## as.factor(year)2021 -7.494e+00  2.084e+00  -3.597 0.000340 ***
    ## as.factor(year)2022 -2.777e+00  7.320e-01  -3.794 0.000159 ***
    ## as.factor(year)2023  2.324e-01  1.999e-01   1.163 0.245299    
    ## as.factor(year)2024         NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8309 on 877 degrees of freedom
    ## Multiple R-squared:  0.9675, Adjusted R-squared:  0.9648 
    ## F-statistic: 362.4 on 72 and 877 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_1-1.png)<!-- -->

#### **Model 1 with Clustered Standard Errors**

    ## 
    ## t test of coefficients:
    ## 
    ##                        Estimate  Std. Error  t value  Pr(>|t|)    
    ## (Intercept)          7.9008e+01  5.7010e+00  13.8587 < 2.2e-16 ***
    ## mortgage_rate       -2.1449e+00  1.1082e+00  -1.9354 0.0532575 .  
    ## hpi                  2.7870e-03  1.8520e-03   1.5048 0.1327311    
    ## median_income       -3.8405e-06  3.3119e-05  -0.1160 0.9077100    
    ## unemployment_rate   -9.7020e-02  7.3667e-02  -1.3170 0.1881806    
    ## rent_burden          9.7179e-02  4.7536e-02   2.0443 0.0412208 *  
    ## perm_per_person      7.7270e+01  4.1556e+01   1.8594 0.0632996 .  
    ## stateAlaska         -4.4919e+00  8.8124e-01  -5.0972 4.223e-07 ***
    ## stateArizona        -4.6937e+00  3.1658e-01 -14.8263 < 2.2e-16 ***
    ## stateArkansas       -2.9073e+00  9.7082e-02 -29.9468 < 2.2e-16 ***
    ## stateCalifornia     -1.5399e+01  7.9717e-01 -19.3171 < 2.2e-16 ***
    ## stateColorado       -4.8035e+00  6.0641e-01  -7.9213 7.102e-15 ***
    ## stateConnecticut    -3.0754e+00  8.7963e-01  -3.4962 0.0004955 ***
    ## stateDelaware        1.6345e+00  4.7504e-01   3.4408 0.0006074 ***
    ## stateFlorida        -4.0985e+00  5.6092e-01  -7.3067 6.155e-13 ***
    ## stateGeorgia        -5.0520e+00  3.3094e-01 -15.2657 < 2.2e-16 ***
    ## stateHawaii         -1.2124e+01  8.2553e-01 -14.6869 < 2.2e-16 ***
    ## stateIdaho           2.6193e-01  1.9691e-01   1.3302 0.1838000    
    ## stateIllinois       -2.3400e+00  5.3322e-01  -4.3884 1.281e-05 ***
    ## stateIndiana         5.3350e-01  2.6330e-01   2.0262 0.0430423 *  
    ## stateIowa            2.5392e+00  3.3804e-01   7.5116 1.438e-13 ***
    ## stateKansas         -1.7759e+00  3.3268e-01  -5.3383 1.195e-07 ***
    ## stateKentucky       -1.0239e+00  1.2238e-01  -8.3661 2.332e-16 ***
    ## stateLouisiana      -2.9623e+00  2.0649e-01 -14.3456 < 2.2e-16 ***
    ## stateMaine           2.0691e+00  3.2121e-01   6.4416 1.947e-10 ***
    ## stateMaryland       -2.8497e+00  9.4985e-01  -3.0001 0.0027752 ** 
    ## stateMassachusetts  -8.2964e+00  8.2653e-01 -10.0376 < 2.2e-16 ***
    ## stateMichigan        2.7621e+00  3.7293e-01   7.4065 3.045e-13 ***
    ## stateMinnesota       2.7751e+00  5.8079e-01   4.7781 2.074e-06 ***
    ## stateMississippi    -1.3352e-01  1.2641e-01  -1.0562 0.2911614    
    ## stateMissouri       -1.2458e+00  1.7160e-01  -7.2600 8.536e-13 ***
    ## stateMontana        -1.2492e+00  1.9598e-01  -6.3740 2.973e-10 ***
    ## stateNebraska       -2.5503e+00  3.4095e-01  -7.4799 1.805e-13 ***
    ## stateNevada         -1.2534e+01  4.8374e-01 -25.9107 < 2.2e-16 ***
    ## stateNew Hampshire   1.4026e+00  7.1177e-01   1.9706 0.0490878 *  
    ## stateNew Jersey     -5.7073e+00  9.1722e-01  -6.2224 7.578e-10 ***
    ## stateNew Mexico     -1.0226e+00  7.1260e-02 -14.3503 < 2.2e-16 ***
    ## stateNew York       -1.6724e+01  6.1489e-01 -27.1978 < 2.2e-16 ***
    ## stateNorth Carolina -3.8124e+00  1.7305e-01 -22.0308 < 2.2e-16 ***
    ## stateNorth Dakota   -4.9058e+00  4.2591e-01 -11.5185 < 2.2e-16 ***
    ## stateOhio           -2.1026e+00  2.7392e-01  -7.6760 4.373e-14 ***
    ## stateOklahoma       -2.9152e+00  2.1650e-01 -13.4651 < 2.2e-16 ***
    ## stateOregon         -7.8872e+00  4.0848e-01 -19.3086 < 2.2e-16 ***
    ## statePennsylvania   -2.2477e-01  3.1881e-01  -0.7050 0.4809840    
    ## stateRhode Island   -8.6055e+00  5.3540e-01 -16.0730 < 2.2e-16 ***
    ## stateSouth Carolina -1.9862e-01  1.5610e-01  -1.2724 0.2035662    
    ## stateSouth Dakota   -1.0845e+00  3.3148e-01  -3.2717 0.0011108 ** 
    ## stateTennessee      -2.4550e+00  9.8619e-02 -24.8938 < 2.2e-16 ***
    ## stateTexas          -7.1439e+00  4.1600e-01 -17.1729 < 2.2e-16 ***
    ## stateUtah           -2.4123e-02  5.1619e-01  -0.0467 0.9627374    
    ## stateVermont         9.8103e-01  3.8250e-01   2.5648 0.0104902 *  
    ## stateVirginia       -3.0372e+00  6.1344e-01  -4.9511 8.849e-07 ***
    ## stateWashington     -7.1265e+00  5.7838e-01 -12.3214 < 2.2e-16 ***
    ## stateWest Virginia   4.7798e+00  1.9993e-01  23.9073 < 2.2e-16 ***
    ## stateWisconsin      -1.5277e+00  3.2068e-01  -4.7639 2.222e-06 ***
    ## stateWyoming         1.2139e+00  4.6034e-01   2.6370 0.0085120 ** 
    ## as.factor(year)2006  1.4920e+00  5.5474e-01   2.6895 0.0072915 ** 
    ## as.factor(year)2007  1.4050e+00  4.0033e-01   3.5096 0.0004716 ***
    ## as.factor(year)2008  4.9140e-01  2.0688e-01   2.3753 0.0177467 *  
    ## as.factor(year)2009 -1.9796e+00  1.2697e+00  -1.5590 0.1193465    
    ## as.factor(year)2010 -3.2643e+00  1.6235e+00  -2.0106 0.0446720 *  
    ## as.factor(year)2011 -4.5233e+00  1.9061e+00  -2.3731 0.0178564 *  
    ## as.factor(year)2012 -6.8682e+00  2.7742e+00  -2.4757 0.0134849 *  
    ## as.factor(year)2013 -6.5820e+00  2.4414e+00  -2.6960 0.0071524 ** 
    ## as.factor(year)2014 -6.7190e+00  2.2514e+00  -2.9844 0.0029203 ** 
    ## as.factor(year)2015 -7.3841e+00  2.6267e+00  -2.8112 0.0050458 ** 
    ## as.factor(year)2016 -7.7595e+00  2.8931e+00  -2.6821 0.0074544 ** 
    ## as.factor(year)2017 -6.4152e+00  2.5431e+00  -2.5226 0.0118253 *  
    ## as.factor(year)2018 -5.2565e+00  1.9368e+00  -2.7139 0.0067796 ** 
    ## as.factor(year)2019 -6.3558e+00  2.6994e+00  -2.3545 0.0187658 *  
    ## as.factor(year)2021 -7.4938e+00  3.8630e+00  -1.9399 0.0527135 .  
    ## as.factor(year)2022 -2.7770e+00  1.3623e+00  -2.0385 0.0417999 *  
    ## as.factor(year)2023  2.3243e-01  2.3620e-01   0.9840 0.3253713    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

#### **Model 2**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + mortgage_rate_lag1 + 
    ##     mortgage_rate_lag2 + mortgage_rate_lag3 + hpi + median_income + 
    ##     unemployment_rate + rent_burden + perm_per_person + state + 
    ##     as.factor(year), data = merged)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -3.2293 -0.4098  0.0067  0.4462  2.9315 
    ## 
    ## Coefficients: (4 not defined because of singularities)
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          6.312e+01  1.933e+00  32.650  < 2e-16 ***
    ## mortgage_rate       -1.337e-01  7.461e-02  -1.792 0.073611 .  
    ## mortgage_rate_lag1   2.233e-01  8.632e-02   2.587 0.009877 ** 
    ## mortgage_rate_lag2   7.226e-02  7.658e-02   0.944 0.345709    
    ## mortgage_rate_lag3   5.981e-01  1.540e-01   3.883 0.000112 ***
    ## hpi                  1.939e-03  1.015e-03   1.911 0.056386 .  
    ## median_income        3.260e-06  2.063e-05   0.158 0.874476    
    ## unemployment_rate   -3.610e-02  4.114e-02  -0.878 0.380465    
    ## rent_burden          5.915e-02  2.155e-02   2.745 0.006203 ** 
    ## perm_per_person      1.144e+02  3.052e+01   3.749 0.000191 ***
    ## stateAlaska         -4.313e+00  6.133e-01  -7.034 4.64e-12 ***
    ## stateArizona        -4.788e+00  3.368e-01 -14.216  < 2e-16 ***
    ## stateArkansas       -2.944e+00  2.884e-01 -10.208  < 2e-16 ***
    ## stateCalifornia     -1.519e+01  4.904e-01 -30.973  < 2e-16 ***
    ## stateColorado       -4.867e+00  4.579e-01 -10.631  < 2e-16 ***
    ## stateConnecticut    -3.059e+00  5.913e-01  -5.174 2.97e-07 ***
    ## stateDelaware        1.869e+00  3.984e-01   4.691 3.24e-06 ***
    ## stateFlorida        -3.931e+00  3.830e-01 -10.263  < 2e-16 ***
    ## stateGeorgia        -5.162e+00  3.400e-01 -15.183  < 2e-16 ***
    ## stateHawaii         -1.155e+01  5.587e-01 -20.676  < 2e-16 ***
    ## stateIdaho           3.263e-01  3.057e-01   1.068 0.286031    
    ## stateIllinois       -2.447e+00  4.209e-01  -5.815 9.06e-09 ***
    ## stateIndiana         4.742e-01  3.233e-01   1.467 0.142859    
    ## stateIowa            2.430e+00  3.642e-01   6.672 4.97e-11 ***
    ## stateKansas         -2.031e+00  3.592e-01  -5.654 2.25e-08 ***
    ## stateKentucky       -1.272e+00  2.891e-01  -4.398 1.26e-05 ***
    ## stateLouisiana      -2.857e+00  3.011e-01  -9.489  < 2e-16 ***
    ## stateMaine           2.512e+00  3.211e-01   7.824 1.80e-14 ***
    ## stateMaryland       -2.744e+00  6.519e-01  -4.210 2.88e-05 ***
    ## stateMassachusetts  -7.943e+00  4.883e-01 -16.268  < 2e-16 ***
    ## stateMichigan        2.716e+00  3.378e-01   8.041 3.60e-15 ***
    ## stateMinnesota       2.562e+00  4.705e-01   5.446 7.04e-08 ***
    ## stateMississippi    -1.287e-01  2.933e-01  -0.439 0.660983    
    ## stateMissouri       -1.402e+00  3.029e-01  -4.629 4.35e-06 ***
    ## stateMontana        -1.200e+00  2.998e-01  -4.002 6.91e-05 ***
    ## stateNebraska       -2.655e+00  3.654e-01  -7.265 9.58e-13 ***
    ## stateNevada         -1.269e+01  3.939e-01 -32.203  < 2e-16 ***
    ## stateNew Hampshire   1.599e+00  5.267e-01   3.036 0.002479 ** 
    ## stateNew Jersey     -5.648e+00  5.969e-01  -9.462  < 2e-16 ***
    ## stateNew Mexico     -8.322e-01  2.853e-01  -2.916 0.003650 ** 
    ## stateNew York       -1.623e+01  3.937e-01 -41.213  < 2e-16 ***
    ## stateNorth Carolina -3.933e+00  3.053e-01 -12.881  < 2e-16 ***
    ## stateNorth Dakota   -5.403e+00  4.001e-01 -13.506  < 2e-16 ***
    ## stateOhio           -2.289e+00  3.238e-01  -7.068 3.68e-12 ***
    ## stateOklahoma       -3.065e+00  3.122e-01  -9.819  < 2e-16 ***
    ## stateOregon         -7.676e+00  3.430e-01 -22.379  < 2e-16 ***
    ## statePennsylvania   -1.849e-01  3.303e-01  -0.560 0.575805    
    ## stateRhode Island   -8.305e+00  3.675e-01 -22.596  < 2e-16 ***
    ## stateSouth Carolina -2.707e-02  3.002e-01  -0.090 0.928180    
    ## stateSouth Dakota   -1.148e+00  3.399e-01  -3.377 0.000771 ***
    ## stateTennessee      -2.633e+00  2.900e-01  -9.079  < 2e-16 ***
    ## stateTexas          -7.363e+00  3.927e-01 -18.749  < 2e-16 ***
    ## stateUtah           -5.787e-03  4.464e-01  -0.013 0.989661    
    ## stateVermont         1.529e+00  3.573e-01   4.280 2.11e-05 ***
    ## stateVirginia       -3.090e+00  4.782e-01  -6.461 1.90e-10 ***
    ## stateWashington     -7.104e+00  4.244e-01 -16.738  < 2e-16 ***
    ## stateWest Virginia   4.665e+00  2.993e-01  15.584  < 2e-16 ***
    ## stateWisconsin      -1.618e+00  3.479e-01  -4.649 3.96e-06 ***
    ## stateWyoming         1.183e+00  3.929e-01   3.012 0.002684 ** 
    ## as.factor(year)2009 -8.358e-01  2.224e-01  -3.759 0.000184 ***
    ## as.factor(year)2010 -1.113e+00  2.115e-01  -5.260 1.89e-07 ***
    ## as.factor(year)2011 -1.511e+00  2.023e-01  -7.469 2.31e-13 ***
    ## as.factor(year)2012 -1.627e+00  2.016e-01  -8.071 2.86e-15 ***
    ## as.factor(year)2013 -1.577e+00  2.353e-01  -6.701 4.13e-11 ***
    ## as.factor(year)2014 -1.908e+00  2.429e-01  -7.857 1.41e-14 ***
    ## as.factor(year)2015 -1.528e+00  2.864e-01  -5.335 1.28e-07 ***
    ## as.factor(year)2016 -1.648e+00  2.345e-01  -7.029 4.78e-12 ***
    ## as.factor(year)2017 -1.009e+00  2.094e-01  -4.817 1.77e-06 ***
    ## as.factor(year)2018 -7.968e-01  2.261e-01  -3.524 0.000452 ***
    ## as.factor(year)2019 -7.330e-01  1.932e-01  -3.794 0.000160 ***
    ## as.factor(year)2021         NA         NA      NA       NA    
    ## as.factor(year)2022         NA         NA      NA       NA    
    ## as.factor(year)2023         NA         NA      NA       NA    
    ## as.factor(year)2024         NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8023 on 730 degrees of freedom
    ##   (150 observations deleted due to missingness)
    ## Multiple R-squared:  0.9698, Adjusted R-squared:  0.9669 
    ## F-statistic: 339.2 on 69 and 730 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_2-1.png)<!-- -->

#### **Model 3**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + mortgage_rate_lag1 + 
    ##     mortgage_rate_lag2 + hpi + median_income + unemployment_rate + 
    ##     rent_burden + perm_per_person + state + as.factor(year), 
    ##     data = merged)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -3.3520 -0.4192  0.0107  0.4758  2.9905 
    ## 
    ## Coefficients: (3 not defined because of singularities)
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          5.431e+02  1.043e+02   5.208 2.44e-07 ***
    ## mortgage_rate       -9.149e+01  2.012e+01  -4.547 6.32e-06 ***
    ## mortgage_rate_lag1   4.369e+01  9.600e+00   4.551 6.19e-06 ***
    ## mortgage_rate_lag2  -3.009e+01  6.644e+00  -4.529 6.85e-06 ***
    ## hpi                  2.013e-03  9.759e-04   2.063 0.039462 *  
    ## median_income        4.535e-06  1.964e-05   0.231 0.817417    
    ## unemployment_rate   -6.332e-02  4.086e-02  -1.550 0.121608    
    ## rent_burden          8.426e-02  2.105e-02   4.002 6.88e-05 ***
    ## perm_per_person      9.145e+01  2.983e+01   3.066 0.002244 ** 
    ## stateAlaska         -4.487e+00  5.881e-01  -7.630 6.87e-14 ***
    ## stateArizona        -4.783e+00  3.308e-01 -14.460  < 2e-16 ***
    ## stateArkansas       -2.911e+00  2.853e-01 -10.203  < 2e-16 ***
    ## stateCalifornia     -1.540e+01  4.765e-01 -32.310  < 2e-16 ***
    ## stateColorado       -4.891e+00  4.423e-01 -11.059  < 2e-16 ***
    ## stateConnecticut    -3.197e+00  5.699e-01  -5.610 2.81e-08 ***
    ## stateDelaware        1.705e+00  3.861e-01   4.415 1.15e-05 ***
    ## stateFlorida        -4.031e+00  3.776e-01 -10.676  < 2e-16 ***
    ## stateGeorgia        -5.108e+00  3.340e-01 -15.294  < 2e-16 ***
    ## stateHawaii         -1.192e+01  5.397e-01 -22.082  < 2e-16 ***
    ## stateIdaho           3.812e-01  3.019e-01   1.263 0.207068    
    ## stateIllinois       -2.477e+00  4.086e-01  -6.063 2.08e-09 ***
    ## stateIndiana         4.529e-01  3.187e-01   1.421 0.155704    
    ## stateIowa            2.488e+00  3.545e-01   7.020 4.84e-12 ***
    ## stateKansas         -1.931e+00  3.505e-01  -5.508 4.94e-08 ***
    ## stateKentucky       -1.143e+00  2.867e-01  -3.986 7.35e-05 ***
    ## stateLouisiana      -2.951e+00  2.977e-01  -9.913  < 2e-16 ***
    ## stateMaine           2.431e+00  3.174e-01   7.658 5.61e-14 ***
    ## stateMaryland       -2.900e+00  6.228e-01  -4.656 3.79e-06 ***
    ## stateMassachusetts  -8.102e+00  4.795e-01 -16.897  < 2e-16 ***
    ## stateMichigan        2.664e+00  3.342e-01   7.971 5.57e-15 ***
    ## stateMinnesota       2.549e+00  4.521e-01   5.638 2.41e-08 ***
    ## stateMississippi    -9.140e-02  2.904e-01  -0.315 0.753046    
    ## stateMissouri       -1.355e+00  2.993e-01  -4.527 6.90e-06 ***
    ## stateMontana        -1.153e+00  2.975e-01  -3.875 0.000116 ***
    ## stateNebraska       -2.593e+00  3.558e-01  -7.287 7.77e-13 ***
    ## stateNevada         -1.271e+01  3.858e-01 -32.944  < 2e-16 ***
    ## stateNew Hampshire   1.510e+00  5.080e-01   2.973 0.003040 ** 
    ## stateNew Jersey     -5.796e+00  5.736e-01 -10.105  < 2e-16 ***
    ## stateNew Mexico     -8.817e-01  2.830e-01  -3.116 0.001903 ** 
    ## stateNew York       -1.646e+01  3.889e-01 -42.323  < 2e-16 ***
    ## stateNorth Carolina -3.863e+00  3.024e-01 -12.772  < 2e-16 ***
    ## stateNorth Dakota   -5.213e+00  3.820e-01 -13.646  < 2e-16 ***
    ## stateOhio           -2.266e+00  3.198e-01  -7.086 3.09e-12 ***
    ## stateOklahoma       -3.004e+00  3.079e-01  -9.756  < 2e-16 ***
    ## stateOregon         -7.783e+00  3.368e-01 -23.109  < 2e-16 ***
    ## statePennsylvania   -2.363e-01  3.257e-01  -0.725 0.468397    
    ## stateRhode Island   -8.429e+00  3.643e-01 -23.137  < 2e-16 ***
    ## stateSouth Carolina -7.100e-02  2.979e-01  -0.238 0.811657    
    ## stateSouth Dakota   -1.091e+00  3.321e-01  -3.285 0.001066 ** 
    ## stateTennessee      -2.537e+00  2.871e-01  -8.837  < 2e-16 ***
    ## stateTexas          -7.309e+00  3.801e-01 -19.231  < 2e-16 ***
    ## stateUtah           -9.164e-03  4.282e-01  -0.021 0.982931    
    ## stateVermont         1.333e+00  3.508e-01   3.800 0.000156 ***
    ## stateVirginia       -3.148e+00  4.608e-01  -6.832 1.68e-11 ***
    ## stateWashington     -7.115e+00  4.111e-01 -17.307  < 2e-16 ***
    ## stateWest Virginia   4.740e+00  2.970e-01  15.959  < 2e-16 ***
    ## stateWisconsin      -1.615e+00  3.410e-01  -4.737 2.58e-06 ***
    ## stateWyoming         1.163e+00  3.834e-01   3.032 0.002512 ** 
    ## as.factor(year)2008 -8.879e+00  1.961e+00  -4.529 6.86e-06 ***
    ## as.factor(year)2009 -8.866e+01  1.939e+01  -4.573 5.59e-06 ***
    ## as.factor(year)2010 -8.697e+01  1.892e+01  -4.598 4.98e-06 ***
    ## as.factor(year)2011 -1.245e+02  2.706e+01  -4.601 4.92e-06 ***
    ## as.factor(year)2012 -1.973e+02  4.296e+01  -4.594 5.08e-06 ***
    ## as.factor(year)2013 -1.414e+02  3.059e+01  -4.621 4.47e-06 ***
    ## as.factor(year)2014 -1.619e+02  3.503e+01  -4.622 4.46e-06 ***
    ## as.factor(year)2015 -1.898e+02  4.120e+01  -4.608 4.74e-06 ***
    ## as.factor(year)2016 -1.881e+02  4.083e+01  -4.606 4.80e-06 ***
    ## as.factor(year)2017 -1.577e+02  3.433e+01  -4.593 5.08e-06 ***
    ## as.factor(year)2018 -1.275e+02  2.772e+01  -4.601 4.91e-06 ***
    ## as.factor(year)2019 -1.972e+02  4.311e+01  -4.574 5.57e-06 ***
    ## as.factor(year)2021 -2.424e+02  5.329e+01  -4.549 6.26e-06 ***
    ## as.factor(year)2022         NA         NA      NA       NA    
    ## as.factor(year)2023         NA         NA      NA       NA    
    ## as.factor(year)2024         NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8202 on 779 degrees of freedom
    ##   (100 observations deleted due to missingness)
    ## Multiple R-squared:  0.9685, Adjusted R-squared:  0.9657 
    ## F-statistic:   342 on 70 and 779 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_3-1.png)<!-- -->

#### **Model 4**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + mortgage_rate_lag1 + 
    ##     hpi + median_income + unemployment_rate + rent_burden + perm_per_person + 
    ##     state + as.factor(year), data = merged)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -3.2072 -0.4396 -0.0085  0.4842  3.0653 
    ## 
    ## Coefficients: (2 not defined because of singularities)
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          1.063e+02  8.291e+00  12.822  < 2e-16 ***
    ## mortgage_rate       -5.865e+00  1.271e+00  -4.616 4.54e-06 ***
    ## mortgage_rate_lag1  -3.820e-01  1.527e-01  -2.502 0.012552 *  
    ## hpi                  2.214e-03  9.091e-04   2.436 0.015064 *  
    ## median_income        2.583e-06  1.820e-05   0.142 0.887209    
    ## unemployment_rate   -8.453e-02  4.031e-02  -2.097 0.036302 *  
    ## rent_burden          9.954e-02  2.029e-02   4.905 1.13e-06 ***
    ## perm_per_person      9.104e+01  2.769e+01   3.288 0.001052 ** 
    ## stateAlaska         -4.506e+00  5.504e-01  -8.186 1.02e-15 ***
    ## stateArizona        -4.802e+00  3.177e-01 -15.113  < 2e-16 ***
    ## stateArkansas       -2.916e+00  2.783e-01 -10.476  < 2e-16 ***
    ## stateCalifornia     -1.550e+01  4.524e-01 -34.250  < 2e-16 ***
    ## stateColorado       -4.932e+00  4.167e-01 -11.837  < 2e-16 ***
    ## stateConnecticut    -3.245e+00  5.350e-01  -6.065 2.00e-09 ***
    ## stateDelaware        1.632e+00  3.670e-01   4.447 9.90e-06 ***
    ## stateFlorida        -4.172e+00  3.660e-01 -11.400  < 2e-16 ***
    ## stateGeorgia        -5.142e+00  3.214e-01 -15.996  < 2e-16 ***
    ## stateHawaii         -1.215e+01  5.088e-01 -23.874  < 2e-16 ***
    ## stateIdaho           2.781e-01  2.936e-01   0.947 0.343817    
    ## stateIllinois       -2.471e+00  3.878e-01  -6.372 3.09e-10 ***
    ## stateIndiana         4.422e-01  3.086e-01   1.433 0.152216    
    ## stateIowa            2.480e+00  3.398e-01   7.301 6.72e-13 ***
    ## stateKansas         -1.880e+00  3.369e-01  -5.582 3.23e-08 ***
    ## stateKentucky       -1.079e+00  2.803e-01  -3.848 0.000128 ***
    ## stateLouisiana      -3.016e+00  2.897e-01 -10.409  < 2e-16 ***
    ## stateMaine           2.259e+00  3.093e-01   7.302 6.65e-13 ***
    ## stateMaryland       -2.969e+00  5.795e-01  -5.123 3.75e-07 ***
    ## stateMassachusetts  -8.220e+00  4.629e-01 -17.758  < 2e-16 ***
    ## stateMichigan        2.667e+00  3.236e-01   8.243 6.53e-16 ***
    ## stateMinnesota       2.605e+00  4.256e-01   6.119 1.45e-09 ***
    ## stateMississippi    -1.226e-01  2.837e-01  -0.432 0.665772    
    ## stateMissouri       -1.332e+00  2.911e-01  -4.576 5.46e-06 ***
    ## stateMontana        -1.183e+00  2.900e-01  -4.078 4.99e-05 ***
    ## stateNebraska       -2.629e+00  3.420e-01  -7.688 4.25e-14 ***
    ## stateNevada         -1.269e+01  3.683e-01 -34.448  < 2e-16 ***
    ## stateNew Hampshire   1.344e+00  4.806e-01   2.797 0.005281 ** 
    ## stateNew Jersey     -5.850e+00  5.374e-01 -10.887  < 2e-16 ***
    ## stateNew Mexico     -9.743e-01  2.765e-01  -3.523 0.000449 ***
    ## stateNew York       -1.663e+01  3.786e-01 -43.919  < 2e-16 ***
    ## stateNorth Carolina -3.904e+00  2.943e-01 -13.266  < 2e-16 ***
    ## stateNorth Dakota   -5.107e+00  3.618e-01 -14.113  < 2e-16 ***
    ## stateOhio           -2.221e+00  3.098e-01  -7.169 1.67e-12 ***
    ## stateOklahoma       -2.971e+00  2.992e-01  -9.929  < 2e-16 ***
    ## stateOregon         -7.879e+00  3.262e-01 -24.153  < 2e-16 ***
    ## statePennsylvania   -2.590e-01  3.158e-01  -0.820 0.412401    
    ## stateRhode Island   -8.534e+00  3.547e-01 -24.058  < 2e-16 ***
    ## stateSouth Carolina -1.852e-01  2.912e-01  -0.636 0.525001    
    ## stateSouth Dakota   -1.089e+00  3.216e-01  -3.388 0.000738 ***
    ## stateTennessee      -2.526e+00  2.801e-01  -9.016  < 2e-16 ***
    ## stateTexas          -7.309e+00  3.588e-01 -20.371  < 2e-16 ***
    ## stateUtah           -6.616e-02  4.029e-01  -0.164 0.869587    
    ## stateVermont         1.109e+00  3.401e-01   3.260 0.001161 ** 
    ## stateVirginia       -3.158e+00  4.343e-01  -7.273 8.17e-13 ***
    ## stateWashington     -7.169e+00  3.909e-01 -18.342  < 2e-16 ***
    ## stateWest Virginia   4.748e+00  2.900e-01  16.371  < 2e-16 ***
    ## stateWisconsin      -1.608e+00  3.287e-01  -4.891 1.20e-06 ***
    ## stateWyoming         1.124e+00  3.690e-01   3.045 0.002400 ** 
    ## as.factor(year)2007 -1.518e-01  2.069e-01  -0.734 0.463368    
    ## as.factor(year)2008 -2.258e+00  5.867e-01  -3.848 0.000128 ***
    ## as.factor(year)2009 -8.562e+00  1.831e+00  -4.675 3.43e-06 ***
    ## as.factor(year)2010 -1.153e+01  2.369e+00  -4.864 1.37e-06 ***
    ## as.factor(year)2011 -1.382e+01  2.734e+00  -5.055 5.30e-07 ***
    ## as.factor(year)2012 -1.920e+01  3.771e+00  -5.092 4.39e-07 ***
    ## as.factor(year)2013 -1.804e+01  3.466e+00  -5.204 2.46e-07 ***
    ## as.factor(year)2014 -1.732e+01  3.209e+00  -5.399 8.75e-08 ***
    ## as.factor(year)2015 -1.909e+01  3.616e+00  -5.280 1.65e-07 ***
    ## as.factor(year)2016 -2.032e+01  3.920e+00  -5.184 2.73e-07 ***
    ## as.factor(year)2017 -1.780e+01  3.542e+00  -5.025 6.18e-07 ***
    ## as.factor(year)2018 -1.444e+01  2.828e+00  -5.107 4.06e-07 ***
    ## as.factor(year)2019 -1.760e+01  3.585e+00  -4.910 1.10e-06 ***
    ## as.factor(year)2021 -2.262e+01  4.910e+00  -4.608 4.72e-06 ***
    ## as.factor(year)2022 -9.369e+00  2.070e+00  -4.526 6.88e-06 ***
    ## as.factor(year)2023         NA         NA      NA       NA    
    ## as.factor(year)2024         NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8251 on 828 degrees of freedom
    ##   (50 observations deleted due to missingness)
    ## Multiple R-squared:  0.9681, Adjusted R-squared:  0.9653 
    ## F-statistic: 353.6 on 71 and 828 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_4-1.png)<!-- -->
