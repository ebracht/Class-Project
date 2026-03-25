Class Project
================

Our proposed research question is: How have changes in mortgage interest
rates and housing prices affected homeownership rates across U.S. states
over time?

To study this, we plan to build a panel data set that examines each
state-year on homeownership rate, housing affordability, mortgage rates,
and other relevant variables like median income or unemployment rate.
Our primary data sources will be the U.S. Census Bureau and the Federal
Reserve Economic Data (FRED), which includes state homeownership rates
and the 30-year fixed mortgage rate. Additionally, the Federal Housing
Finance Agency’s House Price Index, which provides state-level data on
house price changes, and the Bureau of Labor Statistics, which has
state-level data on unemployment, will be pulled. Together, these
sources will provide panel data that can be used to examine how rising
mortgage rates and increasing prices affect homeownership, while
allowing room for controls like unemployment, median income, or
population, to understand this effect better.

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
exploring homeownership rates is well-aligned not only with this goal,
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

Our proposed research question is: How have changes in mortgage interest
rates and housing prices affected homeownership rates across U.S. states
over time?

**Personal Contributions**

**Meeting 1 (02/25):**

Liz, Ryan, and Levi decided on a weekly meeting time, went through the
requirements for the project, and established a shared doc. We planned
to each pitch an idea for our next meeting. This did not need to be
super formal, but we provided a brief description and data source links.

**Meeting 2 (03/04):**

**Ideas**  
Levi: Minimum Wage/Food Security/Poverty Programs

Description: The Center for Poverty Research compiled an impressive and
easy-to-use dataset with information on state policies such as the
minimum wage, SNAP, EITC, and so on. I propose using this dataset to
measure whether/how these policies have influenced variables of interest
such as poverty, employment, or food insecurity. The data set is fairly
comprehensive (part of the appeal), but I think it would be easy to find
opportunities to supplement it with other datasets. For example, the
food insecurity data in the Center for Poverty Research dataset only
goes up to 2001. If we wanted to look at how state economic policies
have influenced food insecurity over the past two decades, we would need
to pull in another dataset. I just filled out an online form offered by
Feeding America to request access to their food insecurity data
(available at the state level). They agreed to share it with us, so
that’s one option. I can think of plenty of other options, too. For
example, we could pull in Census data (I have experience scraping Census
data with R using an API key) to analyze whether these policies
influenced the ratio of people that own vs rent their homes. Generally
speaking, these analyses would require rigorous controls, so there would
be ample opportunity to pull in multiple datasets to try and control for
other factors that may influence these endpoints.

Potential data sources: National Welfare Data: “The Center for Poverty
Research annually updates our state-level panel data series covering
population, employment, unemployment, welfare, poverty, and politics.
Our current update includes information for the majority of the 2024
calendar year. We will update the remainder when available. These data
are publicly available to all users.”  
Link: <https://ukcpr.uky.edu/resources>  
Feeding America Food Insecurity Data: “Since 2011, Feeding America has
produced the Map the Meal Gap study, providing estimates of local food
insecurity and food costs on an annual basis to better understand people
and places facing hunger and to inform decisions and actions that will
help us achieve our mission. We do this by generating national and local
data about food insecurity, translating those data into insights and
tools like the interactive map below, and engaging partners to help them
use and improve our data and research in the future.”  
Link: <https://map.feedingamerica.org/>

Liz: Accessibility to alcohol’s relationship to levels of binge drinking
in a given (Iowa) county

Description: The Iowa Department of Health and Human Services has
launched a new campaign called Say “Yes” to Drinking Less Alcohol, to
combat binge drinking. Aiming to investigate whether factors like
accessibility to alcohol are correlated to higher levels of binge
drinking could inform where to best focus future resources and
interventions. Targeted campaigns and/or subsequent action by Iowa
Department of Health and Human Services, in conjunction with community
partners, in areas that show higher levels of average binge drinking
could aid in the ultimate goal of improving health, safety, and alcohol
responsibility in Iowa.

Potential data sources: Class Data on Iowa Liquor Sales: would provide
specific store location as well as county-by-county info and sales
stats  
Link:
<https://data.iowa.gov/Sales-Distribution/Iowa-Liquor-Sales/m3tr-qhgy/about_data>  
U.S. National Health Stats Ranking: allow for the contextualization of a
focus on Iowa and make clear the imminent need for further work aimed at
lowering binge drinking levels; provides national excess drinking
data.  
Link:
<https://www.americashealthrankings.org/explore/measures/ExcessDrink/IA>  
Behavioral Risk Factor Surveillance System (BRFSS) Data: provides past
year’s BRFSS data; this is used to measure progress toward health goals
and is conducted annually in Iowa. Iowa BRFSS survey data supports the
creation and implementation of public health activities and, per the
Iowa Health and Human Services website, “aims to reducing chronic
diseases and other leading causes of death for Iowans.”  
Link: <https://hhs.iowa.gov/about/data-reports/brfss>

**Ryan: Housing Costs, Interest Rates, and Homeownership in the U.S.**

Description: I am very much okay with doing any research topic, but here
is another one so that we have a range of options. My idea is to study
how mortgage interest rates and housing prices affect homeownership
rates across states. We could combine Census housing data, FRED mortgage
rates, and FHFA house price indexes to build a panel dataset and
estimate how changes in borrowing costs and housing prices influence
homeownership or rent burden over time. One potential research question
would be: How do changes in mortgage interest rates and housing prices
affect homeownership rates across U.S. states over time? Data should be
relatively easy to access and merge. Housing outcomes are influenced by
many economic factors, so we could add controls like median income,
unemployment rates, or population growth to isolate the effect of
interest rates and housing prices. We could explore regional
differences, like if changes in interest rates affect homeownership
differently in high-cost housing markets compared to more affordable
states. We’d probably create a panel dataset that observes states over
time, so each state-year would be an observation. The panel would track
how homeownership rates change as mortgage rates, housing prices, and
other economic variables change.

Potential data sources: Homeownership and Housing Data: The U.S. Census
Bureau provides state and national data on homeownership rates, housing
costs, median home values, rent burdens, and other housing market
indicators. These data are available through FRED.  
Links:
<https://fred.stlouisfed.org/searchresults/?st=homeownership%20rates%20by%20state>  
<https://fred.stlouisfed.org/series/RSAHORUSQ156S> Mortgage Interest
Rate Data: The Federal Reserve Economic Data (FRED) database provides
historical mortgage interest rates and other macroeconomic indicators
that can be merged with housing data to analyze how changes in borrowing
costs affect housing outcomes.  
Link: <https://fred.stlouisfed.org/series/MORTGAGE30US>  
Housing Price Index Data: The Federal Housing Finance Agency (FHFA)
provides a House Price Index with quarterly and annual data on housing
price changes at the state and metropolitan levels.  
Link: <https://www.fhfa.gov/data/hpi/datasets?tab=quarterly-data>

**Discussion:**

Levi pointed out that Ryan’s idea had overlap with the Federal Reserve
data we had to use for R HW 3. We all agreed to proceed with that idea
and aimed to think about it in parallel with the homework. We each tried
to merge data sets to make sure we had the skill to do so.

**Meeting 3 (03/11)**

We agreed to move forward with Ryan’s topic, and prepared for our topic
submission due 03/13. In preparation for that, we split up the work as
such:

Ryan will submit the topic by Friday  
All will work on respective sections (see below).  
Levi sections: Process of choosing a topic, opportunities to expand. Liz
sections Policy implications Scott Turner HUD Ryan sections: Topic
(research question, data sources)

Levi will inform Bangjun (former group member) of the plan to log notes
in this document rather than send weekly emails  
Liz will create a GitHub page, will add everyone as collaborators &
email Prof Chale with a status update about a potential issue  
Ryan will upload a file joining Census and FRED data, including a loop
to bring in multiple years of Census data  
Levi will investigate data availability for controlling for state
housing policy

**Meeting 3 (03/18)**

Talked through Checkpoint 1 criteria and made the following plan in
advance of Meeting 4: Work on README/update on Github Updates on
personal contributions Progress on each checkpoint  
1 and 2 are completely done  
Ryan merged some for 3  
Try to run code that someone else posted on github  
We can think on/try simple visualizations but seems like we don’t
actually need anything for a little while  
Date to keep in mind: April 14th is when project draft is due

**Progress on Eight Major Tasks** 1) Propose a research topic (Option 1
or Option 2)

2)  Create a GitHub repository and establish best practices for team
    collaboration.

3)  Demonstrate merging of multiple data sources

4)  Visualize data using Tableau, R, Python, or a combination

5)  Generate meaningful summary statistic (KPIs) of the data

6)  Submit draft of progress at Checkpoint 1 and Checkpoint 2.

7)  Summarize your findings in a short video presentation.

8)  Publish a detailed, well formatted markdown report of your
    analytical story to your GitHub repository. Report requirements are
    outlined below.

**Load Required Packages:**

- tidyverse
- janitor
- readr
- readxl
- tidycensus
- fredr
- lubridate
- tsibble
- fpp3

**Set API Keys:**

- [tidycensus api key](https://api.census.gov/data/key_signup.html)
- [fredr api key](https://fred.stlouisfed.org/docs/api/api_key.html)

**Import necessary data:**

``` r
#Set years to include the last two decades, excluding 2020 due to the COVID-19 pandemic.
years <- c(2005:2019, 2021:2024)

#Extract homeownership data from the Census
homeownership <- map_dfr(
  years,
  function(yr) {
    get_acs(
      geography = "state",
      variables = c(
        total_occupied = "B25003_001",
        owner_occupied = "B25003_002"
      ),
      year = yr,
      survey = "acs1"
    ) %>%
      select(NAME, variable, estimate) %>%
      pivot_wider(names_from = variable, values_from = estimate) %>%
      mutate(
        year = yr,
        homeownership_rate = 100 * owner_occupied / total_occupied
      ) %>%
      transmute(
        state = NAME,
        year,
        homeownership_rate
      )
  }
)

#Extract income data from the Census
income_list <- map(
  years,
  ~ get_acs(
      geography = "state",
      variables = "B19013_001",
      year = .x,
      survey = "acs1"
    ) %>%
      transmute(
        state = NAME,
        year = .x,
        median_income = estimate
      )
)

#Bind the income data into a DF
income <- bind_rows(income_list)

#Extract population data from the Census
population_list <- map(
  years,
  ~ get_acs(
      geography = "state",
      variables = "B01003_001",
      year = .x,
      survey = "acs1"
    ) %>%
      transmute(
        state = NAME,
        year = .x,
        population = estimate
      )
)

#Bind the population data into a DF
population <- bind_rows(population_list)

#Extract mortgage data from FRED
mortgage_raw <- fredr(
  series_id = "MORTGAGE30US",
  observation_start = as.Date("2005-01-01")
)

#Estimate annual mortgage rates
mortgage_annual <- mortgage_raw %>%
  mutate(year = year(date)) %>%
  group_by(year) %>%
  summarise(
    mortgage_rate = mean(value, na.rm = TRUE),
    .groups = "drop"
  )
```

**Merge imported data:**

``` r
#Merge the data sets by year and state
merged <- left_join(
  population, 
  income, 
  by=c("state", "year")) %>%
  left_join(
    homeownership,
    by=c("state", "year")) %>%
      left_join(
        mortgage_annual,
        by="year")
```

**Compute population summary statistics:**

    ## Summary statistics for population:

    ##     Min.  1st Qu.   Median     Mean  3rd Qu.     Max. 
    ##   495226  1773866  4236748  6177740  7053887 39557045

    ## Standard Deviation: 6964177

    ## Variance: 4.849976e+13

**Compute median income summary statistics:**

    ## Summary statistics for median income:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   17184   47153   55609   57792   66969  109707

    ## Standard Deviation: 14977.34

    ## Variance: 224320711

**Compute homeownership rate summary statistics:**

    ## Summary statistics for homeownership rate:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   39.12   64.78   67.47   66.54   69.94   76.30

    ## Standard Deviation: 5.580628

    ## Variance: 31.14341

**Compute mortgage rate summary statistics:**

    ## Summary statistics for mortgage rate:

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   2.958   3.936   4.545   4.864   6.027   6.807

    ## Standard Deviation: 1.152178

    ## Variance: 1.327514

**Plot mortgage rate and national average homeownership rate:**

    ## Warning: Removed 2 rows containing missing values or values outside the scale range
    ## (`geom_line()`).

![](README_files/figure-gfm/figure_1-1.png)<!-- -->
