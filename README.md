# Project_4-Group_Project

# Preparing for the next Pandemic:
### An analysis of the Covid-19 Pandemic at the State and County Levels

## Problem Statement
In 2023, with the total number of new coronavirus cases decreasing and the Pandemic beginning to stabilize, Congress directed the Department of Health and Human Services (HHS) to conduct an in-depth analysis of the coronavirus pandemic. After more than 1 million Americans died during the pandemic, Congress tasked HHS with creating a report detailing how the response to Pandemic could have been improved as well as crafting a resiliency plan aimed at reducing death tolls of future pandemics. 

HHS received funding for this analysis and hired our consulting firm, FF consulting, to develop machine learning models that could explain which variables were most strongly linked to covid outcomes. HHS specifically was interested not only in different policy explanations, but also asked us to consider demographics such as age and race, the pre-existing health conditions of the populations, income, education, and any other factors we found to be potentially causational. 

## Background:
Both in terms of total deaths, as well as deaths per capita, The United States fared worse than most other countries during the coronoavirus pandemic. In the United States, more than 341 people out of 100,000 died due to coronavirus. Only Peru had per population more deaths than the United States (John Hopkins Coronavirus Resource Center). Some states and counties within the United States fared better or worse than others (Lancet study). 

With the pandemic occuring so recently, there are few comprehensive studies examining the links between coronavirus outcomes and different factors such as demographic differences or policy choices. However... 


https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(23)00461-0/fulltext
Authors Thomas J Bollyky, Emma Castro, Aleksandr Y Aravkin, Kayleight Bhangdia, Jeremy Dalos, Erin Hulland et al. conducted a comparative study of covid deaths in each state and Washington DC from Jan 1, 2020 to July 31, 2022. Their findings included:
- "A lower poverty rate, higher mean number of years of education, and a greater proportion of people expressing interpersonal trust were statistically associated with lower infection and death rates"
- "states where larger percentages of the population identify as Black (non-Hispanic) or Hispanic were associated with higher cumulative death rates"
- "Access to quality health care (measured by the IHME's Healthcare Access and Quality Index) was associated with fewer total COVID-19 deaths and SARS-CoV-2 infections"
- "but higher public health spending and more public health personnel per capita were not, at the state level."
- "The political affiliation of the state governor was not associated with lower SARS-CoV-2 infection or COVID-19 death rates"
- "Worse COVID-19 outcomes were associated with the proportion of a state's voters who voted for the 2020 Republican presidential candidate."
- "State governments' uses of protective mandates were associated with lower infection rates, as were mask use, lower mobility, and higher vaccination rate, while vaccination rates were associated with lower death rates."
- "Employment, however, had a statistically significant relationship with restaurant closures and greater infections and deaths: on average, 1574 (95% UI 884–7107) additional infections per 10 000 population were associated in states with a one percentage point increase in employment rate."


https://www.bmj.com/content/369/bmj.m2282
Author Parth Patel examined racial disparities within Covid-19 outcomes in the United Kingdom. Patel explains the signficant disparity in death and case rates were much higher among the "Black, Asian and Ethnic Minority" communities. 

https://jamanetwork.com/journals/jamainternalmedicine/fullarticle/2807617
Authors Jacob Wallace, Paul Goldsmith-Pinkham, and Jason L. Schwartz, compared Ohio and Florida from March 2020 to December 2021 to examine the question, "Was political party affiliation a risk factor associated with excess mortality during the COVID-19 pandemic in Florida and Ohio?" The authors found evidence of a strong political component to Covid-19 deaths; "excess mortality was significantly higher for Republican voters than Democratic voters after COVID-19 vaccines were available to all adults, but not before. These differences were concentrated in counties with lower vaccination rates, and primarily noted in voters residing in Ohio."

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7480051/
Authors Andrew C. Stokes, Dielle J. Lundberg,Irma T. Elo Katherine Hempstead, Jacob Bor, and Samuel H. Preston found strong evidence that "direct Covid-19 death counts in the United States in 2020 substantially underestimated total excess mortality attributable to Covid-19." The authors also found evidence that under-reporting of Covid-19 deaths was exacerbated by racial and socio-economic disparties. They also noted a regional component, with states in the South and West more likely to report the cause of death as something other than coronavirus. 

https://coronavirus.jhu.edu/data/mortality
John Hopkins School of Medicine Coronavirus Resource Center
How the number of deaths from covid in the US compares to death rates of other countries


## Methodology:
In order to build off of existing literature and work towards a comprehensive understanding of factors related to/ driving Coronavirus outcomes, we examined cases and deaths at both the State and County levels from the beginning of 2020 through December 31, 2022. We obtained data at the state level covering pre-existing health conditions, employment, income, education, demographics, health behaviors, mask policies, vaccination rates, insurance rates, and population size and density. At the county level we were not able to obtain standardized data regarding health behaviors but were able to find racial and age demographics for the overall population, vaccination rates, cases, and deaths as well as multiple measures of income inequality.  

The factors we considered in our state models:
- Pre-existing medical conditions
- Demographics
- Income
- Age
- Housing Crisis
- Population Size
- Population Density
- Employment
- Percent population insured
- Mask Policy (Duration of policy)
- Vaccination Rates
- Behaviors (ie wearing a mask, visiting friends)

The factors in our county models:
- Pre-existing medical conditions
- Racial Demographics
- Income
- Age
- Housing Crisis
- Income Inequality
- Segregation
- Population Size
- Rural vs Urban
- Employment
- Percent population insured
- Mask Policy (Number of days a policy was in place)
- Vaccination Rates
- Air Quality


## Data Sources:

#### County level data
Cases, deaths, and population by county
https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/state/texas/ 

#### State Level data
Mask Policy Implementation Dates
https://www.kaggle.com/datasets/manuvarghese98/impact-of-mask-mandate-on-covid19

Death Counts by week and state
https://data.cdc.gov/NCHS/Provisional-COVID-19-Death-Counts-by-Week-Ending-D/r8kw-7aab

Excess Deaths
https://www.cdc.gov/nchs/nvss/vsrr/covid19/excess_deaths.htm

Population per State (Double check that this is the right link)
https://wisevoter.com/state-rankings/states-by-population/ 

Brainstorm site w Population Density:
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9022803/

State Healthcare Compare
https://statehealthcompare.shadac.org/Bulk#1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52

Three Datasets- Health Behaviors, Public Health Measures, and Executive Approval
https://lazerlab.shinyapps.io/Behaviors_During_COVID/

Covid Vaccines by week by state
https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-Jurisdi/unsk-b7fc

500 Cities: Current lack of health insurance among adults aged 18-64 years
https://data.cdc.gov/500-Cities-Places/500-Cities-Current-lack-of-health-insurance-among-/8dbf-5cp2

Health Insurance Coverage of the Total Population - 2019 and 2021
https://www.kff.org/other/state-indicator/total-population/?currentTimeframe=0&sortModel=%7B%22colId%22:%22Location%22,%22sort%22:%22asc%22%7D

## Data Dictionary

#### State Models
|Feature|Type| Description|
|---|---|---|
|Employment_year|numeric|Total Employment by year| 
|Inc_Per_Cap_year|float|Income per capita by year| 
|Life_expectancy_year|float|The average life_expectancy of the country during that year| 
|Employer_2019|float|??| 
|Non-group|numeric|Total Employment by year| 
|Medicaid|float|Income per capita by year| 
|Medicare|float|The average life_expectancy of the country during that year| 
|Military|float|??| 
|Uninsured|numeric|Total Employment by year| 
|Population_Density_per mi2|float|Income per capita by year| 
|year Population|float|The average life_expectancy of the country during that year| 
|flu_vaccination_rate_2019|float|??| 

|asthma_prevalence|numeric|Total Employment by year| 
|Inc_Per_Cap_year|float|Income per capita by year| 
|Life_expectancy_year|float|The average life_expectancy of the country during that year| 
|Employer_2019|float|??| 
|Non-group|numeric|Total Employment by year| 
|Medicaid|float|Income per capita by year| 
|Medicare|float|The average life_expectancy of the country during that year| 
|Military|float|??| 
|Uninsured|numeric|Total Employment by year| 
|Population_Density_per mi2|float|Income per capita by year| 
|year Population|float|The average life_expectancy of the country during that year| 
|flu_vaccination_rate_2019|float|??| 

#### State Models
|Feature|Type| Description|
|---|---|---|
|Employment_year|numeric|Total Employment by year| 
|Inc_Per_Cap_year|float|Income per capita by year| 
|Life_expectancy_year|float|The average life_expectancy of the country during that year| 
|Employer_2019|float|??| 
|Non-group|numeric|Total Employment by year| 
|Medicaid|float|Income per capita by year| 
|Medicare|float|The average life_expectancy of the country during that year| 
|Military|float|??| 
|Uninsured|numeric|Total Employment by year| 
|Population_Density_per mi2|float|Income per capita by year| 
|year Population|float|The average life_expectancy of the country during that year| 
|flu_vaccination_rate_2019|float|??| 

|asthma_prevalence|numeric|Total Employment by year| 
|Inc_Per_Cap_year|float|Income per capita by year| 
|Life_expectancy_year|float|The average life_expectancy of the country during that year| 
|Employer_2019|float|??| 
|Non-group|numeric|Total Employment by year| 
|Medicaid|float|Income per capita by year| 
|Medicare|float|The average life_expectancy of the country during that year| 
|Military|float|??| 
|Uninsured|numeric|Total Employment by year| 
|Population_Density_per mi2|float|Income per capita by year| 
|year Population|float|The average life_expectancy of the country during that year| 
|flu_vaccination_rate_2019|float|??| 


## Data Cleaning & EDA:
Link to tableau dashboard

## Modeling:
Our goal with modeling was two-fold:
1. Develop model(s) that predicted Covid-19 outcomes as successfully as possible
2. Develop model(s) that could be used to interpret the relationships between certain features and different outcomes.

As we were concerned with 

## Analysis/ Conclusions:


## Initial Findings & Reccomendations:


## Next Steps & Further Study:
With more time, we believe experimenting with the following feature engineering steps would yield stronger models with less features and easier interpretability.
Further Data Engineering:
- Combining similar/collinear variables into index variables
    - vaccination rate index
    - health behaviors index
    - pre-existing health of the population index
    - inequality
    - insurance rates/ healthcare access
- Use PCA to reduce dimensionality & combine factors into 1 to 3 variables
    - Pre-existing health conditions
    - Income & Education
    - Political Factors
    - Segregation/ Diversity
    - Strength/ amount of healthcare infrastructure

Further Data Collection:
- Health behaviors at the county level
- Racial demographics at the state level
- Political leanings at state and county level (voter registrations)

Future Models:
In our initial modeling process, we explored multiple y-variables (excess deaths, total deaths attributed to covid-19, and total cases). 
- Time series utilizing policy implementation dates, vaccination rates over time, and covid-19 cases and deaths, v
- 