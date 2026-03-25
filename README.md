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
