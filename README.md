Class Project
================

- [Checkpoint 1: Progress on Eight Major
  Tasks](#checkpoint-1-progress-on-eight-major-tasks)
- [Research Topic](#research-topic)
- [Meeting Minutes and Personal
  Contributions](#meeting-minutes-and-personal-contributions)
- [Load Packages, Setup API Keys, Import
  Data](#load-packages-setup-api-keys-import-data)
- [**Compute Summary Statistics**](#compute-summary-statistics)
- [**Create Visualizations**](#create-visualizations)

### **This landing page displays the knitted output of our README.rmd file. For the code behind the analysis and figures shown below, please consult the README.rmd file.**

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
we made a list of the following action items to address some of the
feedback and begin preparing to work towards Checkpoint 2:

- Liz: Import repository to group page and update README
  - If time, look into using the integrated GitHub Project tool  
- Levi: In the README include descriptions of where to find files  
- Ryan: Clean repositor and make image file names more descriptive  
- All: Try to get more familiar working with datasets we plan to use

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
    ## 8 housing_permits                0

### **Other plots:**

![](README_files/figure-gfm/figure_4-1.png)<!-- -->

![](README_files/figure-gfm/figure_5-1.png)<!-- --> \## **Analysis**
\### **Multicollinearity check:**

    ##     mortgage_rate               hpi unemployment_rate     median_income 
    ##          1.169683          3.552392          2.047872          3.075912 
    ##       rent_burden   housing_permits 
    ##          2.289029          1.229762

### **Regression Analysis**

For directions on how to conduct multilinear regression and plot
confidence intervals, [click
here](https://www.geeksforgeeks.org/r-language/how-to-use-the-coeftest-function-in-r/).

#### **Model 1**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + hpi + median_income + 
    ##     unemployment_rate + state + as.factor(year), data = merged)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -3.3844 -0.4529  0.0224  0.5062  3.1016 
    ## 
    ## Coefficients: (1 not defined because of singularities)
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          8.434e+01  2.923e+00  28.855  < 2e-16 ***
    ## mortgage_rate       -2.307e+00  5.594e-01  -4.125 4.07e-05 ***
    ## hpi                  4.025e-03  8.528e-04   4.719 2.75e-06 ***
    ## median_income       -1.078e-05  1.717e-05  -0.628 0.530096    
    ## unemployment_rate   -8.596e-02  3.638e-02  -2.362 0.018372 *  
    ## stateAlaska         -4.663e+00  5.231e-01  -8.914  < 2e-16 ***
    ## stateArizona        -4.157e+00  3.000e-01 -13.859  < 2e-16 ***
    ## stateArkansas       -2.993e+00  2.767e-01 -10.817  < 2e-16 ***
    ## stateCalifornia     -1.469e+01  3.906e-01 -37.595  < 2e-16 ***
    ## stateColorado       -4.083e+00  3.771e-01 -10.830  < 2e-16 ***
    ## stateConnecticut    -2.583e+00  4.751e-01  -5.438 6.99e-08 ***
    ## stateDelaware        2.126e+00  3.458e-01   6.148 1.19e-09 ***
    ## stateFlorida        -2.880e+00  2.850e-01 -10.105  < 2e-16 ***
    ## stateGeorgia        -4.513e+00  3.022e-01 -14.932  < 2e-16 ***
    ## stateHawaii         -1.149e+01  4.399e-01 -26.126  < 2e-16 ***
    ## stateIdaho           5.003e-01  2.857e-01   1.751 0.080276 .  
    ## stateIllinois       -2.108e+00  3.627e-01  -5.813 8.59e-09 ***
    ## stateIndiana         7.347e-01  3.006e-01   2.444 0.014717 *  
    ## stateIowa            2.438e+00  3.325e-01   7.331 5.19e-13 ***
    ## stateKansas         -1.866e+00  3.287e-01  -5.676 1.87e-08 ***
    ## stateKentucky       -1.265e+00  2.757e-01  -4.590 5.08e-06 ***
    ## stateLouisiana      -2.580e+00  2.773e-01  -9.302  < 2e-16 ***
    ## stateMaine           2.028e+00  3.044e-01   6.662 4.77e-11 ***
    ## stateMaryland       -2.372e+00  5.233e-01  -4.533 6.63e-06 ***
    ## stateMassachusetts  -8.258e+00  4.256e-01 -19.404  < 2e-16 ***
    ## stateMichigan        3.144e+00  3.017e-01  10.423  < 2e-16 ***
    ## stateMinnesota       3.096e+00  3.981e-01   7.777 2.08e-14 ***
    ## stateMississippi    -1.203e-01  2.830e-01  -0.425 0.670797    
    ## stateMissouri       -1.263e+00  2.871e-01  -4.399 1.22e-05 ***
    ## stateMontana        -1.549e+00  2.831e-01  -5.472 5.82e-08 ***
    ## stateNebraska       -2.680e+00  3.353e-01  -7.995 4.07e-15 ***
    ## stateNevada         -1.166e+01  3.276e-01 -35.581  < 2e-16 ***
    ## stateNew Hampshire   1.598e+00  4.422e-01   3.613 0.000320 ***
    ## stateNew Jersey     -5.184e+00  4.856e-01 -10.674  < 2e-16 ***
    ## stateNew Mexico     -9.270e-01  2.746e-01  -3.376 0.000769 ***
    ## stateNew York       -1.651e+01  3.489e-01 -47.317  < 2e-16 ***
    ## stateNorth Carolina -3.434e+00  2.808e-01 -12.228  < 2e-16 ***
    ## stateNorth Dakota   -5.218e+00  3.455e-01 -15.104  < 2e-16 ***
    ## stateOhio           -2.023e+00  3.008e-01  -6.727 3.11e-11 ***
    ## stateOklahoma       -2.981e+00  2.962e-01 -10.064  < 2e-16 ***
    ## stateOregon         -7.392e+00  3.050e-01 -24.239  < 2e-16 ***
    ## statePennsylvania   -2.133e-01  3.015e-01  -0.708 0.479405    
    ## stateRhode Island   -8.646e+00  3.334e-01 -25.931  < 2e-16 ***
    ## stateSouth Carolina  1.593e-01  2.782e-01   0.573 0.567087    
    ## stateSouth Dakota   -1.487e+00  3.049e-01  -4.877 1.28e-06 ***
    ## stateTennessee      -2.248e+00  2.763e-01  -8.135 1.40e-15 ***
    ## stateTexas          -6.522e+00  3.318e-01 -19.656  < 2e-16 ***
    ## stateUtah            3.190e-01  3.853e-01   0.828 0.407994    
    ## stateVermont         1.243e+00  3.115e-01   3.989 7.18e-05 ***
    ## stateVirginia       -2.785e+00  4.072e-01  -6.839 1.49e-11 ***
    ## stateWashington     -6.761e+00  3.729e-01 -18.129  < 2e-16 ***
    ## stateWest Virginia   4.386e+00  2.798e-01  15.674  < 2e-16 ***
    ## stateWisconsin      -1.486e+00  3.197e-01  -4.647 3.88e-06 ***
    ## stateWyoming         7.223e-01  3.530e-01   2.046 0.041048 *  
    ## as.factor(year)2006  1.517e+00  3.012e-01   5.037 5.74e-07 ***
    ## as.factor(year)2007  1.273e+00  2.387e-01   5.334 1.22e-07 ***
    ## as.factor(year)2008  2.830e-01  1.596e-01   1.773 0.076531 .  
    ## as.factor(year)2009 -2.297e+00  5.892e-01  -3.898 0.000104 ***
    ## as.factor(year)2010 -3.511e+00  7.718e-01  -4.549 6.14e-06 ***
    ## as.factor(year)2011 -4.739e+00  9.170e-01  -5.168 2.93e-07 ***
    ## as.factor(year)2012 -7.261e+00  1.367e+00  -5.313 1.37e-07 ***
    ## as.factor(year)2013 -6.916e+00  1.205e+00  -5.738 1.32e-08 ***
    ## as.factor(year)2014 -6.995e+00  1.113e+00  -6.286 5.12e-10 ***
    ## as.factor(year)2015 -7.806e+00  1.313e+00  -5.944 4.01e-09 ***
    ## as.factor(year)2016 -8.267e+00  1.444e+00  -5.726 1.41e-08 ***
    ## as.factor(year)2017 -6.877e+00  1.282e+00  -5.364 1.04e-07 ***
    ## as.factor(year)2018 -5.602e+00  9.952e-01  -5.629 2.43e-08 ***
    ## as.factor(year)2019 -6.869e+00  1.378e+00  -4.986 7.42e-07 ***
    ## as.factor(year)2021 -7.978e+00  1.948e+00  -4.094 4.62e-05 ***
    ## as.factor(year)2022 -2.895e+00  6.780e-01  -4.270 2.17e-05 ***
    ## as.factor(year)2023  2.877e-01  2.020e-01   1.424 0.154773    
    ## as.factor(year)2024         NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8458 on 879 degrees of freedom
    ## Multiple R-squared:  0.9662, Adjusted R-squared:  0.9635 
    ## F-statistic: 359.3 on 70 and 879 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_1-1.png)<!-- -->

#### **Model 1 with Clustered Standard Errors**

    ## 
    ## t test of coefficients:
    ## 
    ##                        Estimate  Std. Error  t value  Pr(>|t|)    
    ## (Intercept)          8.4343e+01  5.5120e+00  15.3016 < 2.2e-16 ***
    ## mortgage_rate       -2.3072e+00  1.0787e+00  -2.1390 0.0327117 *  
    ## hpi                  4.0246e-03  1.7168e-03   2.3443 0.0192864 *  
    ## median_income       -1.0784e-05  3.1778e-05  -0.3393 0.7344330    
    ## unemployment_rate   -8.5957e-02  8.8684e-02  -0.9692 0.3326876    
    ## stateAlaska         -4.6630e+00  8.3243e-01  -5.6017 2.839e-08 ***
    ## stateArizona        -4.1571e+00  2.5858e-01 -16.0770 < 2.2e-16 ***
    ## stateArkansas       -2.9926e+00  8.9933e-02 -33.2762 < 2.2e-16 ***
    ## stateCalifornia     -1.4686e+01  6.5040e-01 -22.5792 < 2.2e-16 ***
    ## stateColorado       -4.0833e+00  5.2840e-01  -7.7278 2.985e-14 ***
    ## stateConnecticut    -2.5833e+00  7.5585e-01  -3.4177 0.0006604 ***
    ## stateDelaware        2.1259e+00  4.4396e-01   4.7884 1.972e-06 ***
    ## stateFlorida        -2.8803e+00  1.9585e-01 -14.7066 < 2.2e-16 ***
    ## stateGeorgia        -4.5132e+00  2.5081e-01 -17.9944 < 2.2e-16 ***
    ## stateHawaii         -1.1493e+01  7.1576e-01 -16.0574 < 2.2e-16 ***
    ## stateIdaho           5.0031e-01  1.8979e-01   2.6361 0.0085331 ** 
    ## stateIllinois       -2.1082e+00  4.5999e-01  -4.5832 5.242e-06 ***
    ## stateIndiana         7.3475e-01  2.2233e-01   3.3048 0.0009891 ***
    ## stateIowa            2.4377e+00  3.4123e-01   7.1437 1.907e-12 ***
    ## stateKansas         -1.8656e+00  3.2571e-01  -5.7279 1.396e-08 ***
    ## stateKentucky       -1.2652e+00  6.2329e-02 -20.2994 < 2.2e-16 ***
    ## stateLouisiana      -2.5799e+00  8.5633e-02 -30.1272 < 2.2e-16 ***
    ## stateMaine           2.0279e+00  3.1875e-01   6.3620 3.201e-10 ***
    ## stateMaryland       -2.3720e+00  8.6762e-01  -2.7339 0.0063841 ** 
    ## stateMassachusetts  -8.2582e+00  7.8786e-01 -10.4819 < 2.2e-16 ***
    ## stateMichigan        3.1444e+00  2.5715e-01  12.2278 < 2.2e-16 ***
    ## stateMinnesota       3.0959e+00  5.3993e-01   5.7338 1.350e-08 ***
    ## stateMississippi    -1.2033e-01  1.4401e-01  -0.8356 0.4036340    
    ## stateMissouri       -1.2629e+00  1.5534e-01  -8.1295 1.459e-15 ***
    ## stateMontana        -1.5493e+00  1.6760e-01  -9.2440 < 2.2e-16 ***
    ## stateNebraska       -2.6803e+00  3.5877e-01  -7.4707 1.924e-13 ***
    ## stateNevada         -1.1657e+01  3.7088e-01 -31.4308 < 2.2e-16 ***
    ## stateNew Hampshire   1.5976e+00  6.7794e-01   2.3565 0.0186670 *  
    ## stateNew Jersey     -5.1836e+00  8.2880e-01  -6.2543 6.226e-10 ***
    ## stateNew Mexico     -9.2697e-01  2.7706e-02 -33.4572 < 2.2e-16 ***
    ## stateNew York       -1.6510e+01  5.5008e-01 -30.0136 < 2.2e-16 ***
    ## stateNorth Carolina -3.4338e+00  1.4306e-01 -24.0027 < 2.2e-16 ***
    ## stateNorth Dakota   -5.2181e+00  3.9540e-01 -13.1971 < 2.2e-16 ***
    ## stateOhio           -2.0234e+00  2.2720e-01  -8.9056 < 2.2e-16 ***
    ## stateOklahoma       -2.9810e+00  2.2262e-01 -13.3903 < 2.2e-16 ***
    ## stateOregon         -7.3921e+00  3.3404e-01 -22.1290 < 2.2e-16 ***
    ## statePennsylvania   -2.1334e-01  2.7384e-01  -0.7791 0.4361563    
    ## stateRhode Island   -8.6464e+00  4.7528e-01 -18.1924 < 2.2e-16 ***
    ## stateSouth Carolina  1.5928e-01  1.1902e-01   1.3383 0.1811529    
    ## stateSouth Dakota   -1.4870e+00  2.6733e-01  -5.5623 3.534e-08 ***
    ## stateTennessee      -2.2478e+00  8.0474e-02 -27.9316 < 2.2e-16 ***
    ## stateTexas          -6.5218e+00  3.3777e-01 -19.3084 < 2.2e-16 ***
    ## stateUtah            3.1897e-01  5.2757e-01   0.6046 0.5456005    
    ## stateVermont         1.2427e+00  3.3551e-01   3.7040 0.0002255 ***
    ## stateVirginia       -2.7849e+00  5.9248e-01  -4.7004 3.013e-06 ***
    ## stateWashington     -6.7610e+00  5.7235e-01 -11.8127 < 2.2e-16 ***
    ## stateWest Virginia   4.3857e+00  1.3726e-01  31.9522 < 2.2e-16 ***
    ## stateWisconsin      -1.4855e+00  3.0629e-01  -4.8500 1.460e-06 ***
    ## stateWyoming         7.2234e-01  4.0311e-01   1.7919 0.0734935 .  
    ## as.factor(year)2006  1.5170e+00  5.6257e-01   2.6965 0.0071413 ** 
    ## as.factor(year)2007  1.2730e+00  4.2457e-01   2.9985 0.0027899 ** 
    ## as.factor(year)2008  2.8304e-01  1.1763e-01   2.4062 0.0163244 *  
    ## as.factor(year)2009 -2.2970e+00  1.1028e+00  -2.0828 0.0375581 *  
    ## as.factor(year)2010 -3.5112e+00  1.4280e+00  -2.4589 0.0141291 *  
    ## as.factor(year)2011 -4.7387e+00  1.7186e+00  -2.7572 0.0059502 ** 
    ## as.factor(year)2012 -7.2612e+00  2.5877e+00  -2.8061 0.0051260 ** 
    ## as.factor(year)2013 -6.9159e+00  2.2889e+00  -3.0215 0.0025884 ** 
    ## as.factor(year)2014 -6.9947e+00  2.0999e+00  -3.3309 0.0009017 ***
    ## as.factor(year)2015 -7.8057e+00  2.5008e+00  -3.1212 0.0018598 ** 
    ## as.factor(year)2016 -8.2675e+00  2.7658e+00  -2.9892 0.0028753 ** 
    ## as.factor(year)2017 -6.8771e+00  2.4453e+00  -2.8124 0.0050274 ** 
    ## as.factor(year)2018 -5.6022e+00  1.8670e+00  -3.0006 0.0027707 ** 
    ## as.factor(year)2019 -6.8685e+00  2.6354e+00  -2.6062 0.0093094 ** 
    ## as.factor(year)2021 -7.9775e+00  3.7455e+00  -2.1299 0.0334558 *  
    ## as.factor(year)2022 -2.8952e+00  1.3194e+00  -2.1943 0.0284780 *  
    ## as.factor(year)2023  2.8771e-01  2.3973e-01   1.2001 0.2304044    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

#### **Model 2**

    ## 
    ## Call:
    ## lm(formula = homeownership_rate ~ mortgage_rate + mortgage_rate_lag1 + 
    ##     mortgage_rate_lag2 + mortgage_rate_lag3 + hpi + median_income + 
    ##     unemployment_rate + state + as.factor(year), data = merged)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -3.3511 -0.4346  0.0286  0.4616  2.8344 
    ## 
    ## Coefficients: (4 not defined because of singularities)
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          6.695e+01  1.550e+00  43.191  < 2e-16 ***
    ## mortgage_rate       -1.682e-01  7.225e-02  -2.328 0.020162 *  
    ## mortgage_rate_lag1   1.940e-01  8.604e-02   2.255 0.024455 *  
    ## mortgage_rate_lag2   6.125e-02  7.752e-02   0.790 0.429735    
    ## mortgage_rate_lag3   5.395e-01  1.523e-01   3.542 0.000423 ***
    ## hpi                  3.515e-03  9.677e-04   3.632 0.000300 ***
    ## median_income       -1.123e-05  2.044e-05  -0.549 0.582905    
    ## unemployment_rate   -5.081e-02  3.787e-02  -1.342 0.180137    
    ## stateAlaska         -4.222e+00  6.179e-01  -6.833 1.75e-11 ***
    ## stateArizona        -4.316e+00  3.227e-01 -13.377  < 2e-16 ***
    ## stateArkansas       -3.006e+00  2.909e-01 -10.334  < 2e-16 ***
    ## stateCalifornia     -1.476e+01  4.348e-01 -33.936  < 2e-16 ***
    ## stateColorado       -4.214e+00  4.243e-01  -9.932  < 2e-16 ***
    ## stateConnecticut    -2.669e+00  5.517e-01  -4.837 1.61e-06 ***
    ## stateDelaware        2.367e+00  3.818e-01   6.201 9.36e-10 ***
    ## stateFlorida        -3.076e+00  2.979e-01 -10.326  < 2e-16 ***
    ## stateGeorgia        -4.717e+00  3.240e-01 -14.560  < 2e-16 ***
    ## stateHawaii         -1.114e+01  4.987e-01 -22.346  < 2e-16 ***
    ## stateIdaho           6.398e-01  3.009e-01   2.127 0.033784 *  
    ## stateIllinois       -2.289e+00  4.107e-01  -5.574 3.49e-08 ***
    ## stateIndiana         6.565e-01  3.213e-01   2.043 0.041396 *  
    ## stateIowa            2.476e+00  3.689e-01   6.712 3.85e-11 ***
    ## stateKansas         -2.017e+00  3.632e-01  -5.554 3.92e-08 ***
    ## stateKentucky       -1.463e+00  2.885e-01  -5.069 5.06e-07 ***
    ## stateLouisiana      -2.577e+00  2.909e-01  -8.859  < 2e-16 ***
    ## stateMaine           2.354e+00  3.197e-01   7.364 4.83e-13 ***
    ## stateMaryland       -2.270e+00  6.199e-01  -3.662 0.000268 ***
    ## stateMassachusetts  -8.084e+00  4.639e-01 -17.428  < 2e-16 ***
    ## stateMichigan        2.934e+00  3.211e-01   9.136  < 2e-16 ***
    ## stateMinnesota       2.906e+00  4.583e-01   6.340 4.01e-10 ***
    ## stateMississippi    -1.760e-01  2.971e-01  -0.592 0.553761    
    ## stateMissouri       -1.424e+00  3.056e-01  -4.658 3.79e-06 ***
    ## stateMontana        -1.407e+00  2.985e-01  -4.714 2.90e-06 ***
    ## stateNebraska       -2.601e+00  3.702e-01  -7.026 4.86e-12 ***
    ## stateNevada         -1.195e+01  3.583e-01 -33.356  < 2e-16 ***
    ## stateNew Hampshire   1.781e+00  5.098e-01   3.494 0.000505 ***
    ## stateNew Jersey     -5.186e+00  5.647e-01  -9.183  < 2e-16 ***
    ## stateNew Mexico     -8.238e-01  2.877e-01  -2.863 0.004311 ** 
    ## stateNew York       -1.628e+01  3.654e-01 -44.562  < 2e-16 ***
    ## stateNorth Carolina -3.513e+00  2.951e-01 -11.906  < 2e-16 ***
    ## stateNorth Dakota   -5.279e+00  3.902e-01 -13.530  < 2e-16 ***
    ## stateOhio           -2.253e+00  3.237e-01  -6.960 7.56e-12 ***
    ## stateOklahoma       -3.066e+00  3.164e-01  -9.691  < 2e-16 ***
    ## stateOregon         -7.372e+00  3.229e-01 -22.826  < 2e-16 ***
    ## statePennsylvania   -2.430e-01  3.239e-01  -0.750 0.453368    
    ## stateRhode Island   -8.491e+00  3.527e-01 -24.076  < 2e-16 ***
    ## stateSouth Carolina  3.766e-01  2.908e-01   1.295 0.195702    
    ## stateSouth Dakota   -1.213e+00  3.291e-01  -3.686 0.000245 ***
    ## stateTennessee      -2.403e+00  2.897e-01  -8.294 5.24e-16 ***
    ## stateTexas          -6.684e+00  3.683e-01 -18.149  < 2e-16 ***
    ## stateUtah            4.826e-01  4.386e-01   1.100 0.271486    
    ## stateVermont         1.597e+00  3.337e-01   4.785 2.07e-06 ***
    ## stateVirginia       -2.812e+00  4.660e-01  -6.034 2.54e-09 ***
    ## stateWashington     -6.750e+00  4.162e-01 -16.217  < 2e-16 ***
    ## stateWest Virginia   4.365e+00  2.935e-01  14.876  < 2e-16 ***
    ## stateWisconsin      -1.554e+00  3.487e-01  -4.457 9.63e-06 ***
    ## stateWyoming         1.063e+00  3.935e-01   2.701 0.007074 ** 
    ## as.factor(year)2009 -8.117e-01  2.245e-01  -3.615 0.000321 ***
    ## as.factor(year)2010 -1.049e+00  2.126e-01  -4.937 9.81e-07 ***
    ## as.factor(year)2011 -1.446e+00  2.019e-01  -7.165 1.90e-12 ***
    ## as.factor(year)2012 -1.648e+00  2.043e-01  -8.067 2.95e-15 ***
    ## as.factor(year)2013 -1.602e+00  2.356e-01  -6.802 2.15e-11 ***
    ## as.factor(year)2014 -1.935e+00  2.447e-01  -7.909 9.59e-15 ***
    ## as.factor(year)2015 -1.662e+00  2.854e-01  -5.823 8.68e-09 ***
    ## as.factor(year)2016 -1.803e+00  2.322e-01  -7.767 2.71e-14 ***
    ## as.factor(year)2017 -1.150e+00  2.070e-01  -5.557 3.85e-08 ***
    ## as.factor(year)2018 -9.185e-01  2.245e-01  -4.091 4.78e-05 ***
    ## as.factor(year)2019 -8.868e-01  1.913e-01  -4.635 4.22e-06 ***
    ## as.factor(year)2021         NA         NA      NA       NA    
    ## as.factor(year)2022         NA         NA      NA       NA    
    ## as.factor(year)2023         NA         NA      NA       NA    
    ## as.factor(year)2024         NA         NA      NA       NA    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.8133 on 732 degrees of freedom
    ##   (150 observations deleted due to missingness)
    ## Multiple R-squared:  0.9688, Adjusted R-squared:  0.966 
    ## F-statistic: 339.7 on 67 and 732 DF,  p-value: < 2.2e-16

![](README_files/figure-gfm/regression_2-1.png)<!-- -->
