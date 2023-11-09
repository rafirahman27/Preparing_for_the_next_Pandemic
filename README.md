# Project_4-Group_Project

# Preparing for the next Pandemic:
### An analysis of the Covid-19 Pandemic at the State and County Levels

## Problem Statement
In 2023, with the total number of new coronavirus cases decreasing and the Pandemic beginning to stabilize, Congress directed the Department of Health and Human Services (HHS) to conduct an in-depth analysis of the coronavirus pandemic. After more than 1 million Americans died during the pandemic, Congress tasked HHS with creating a report detailing how the response to Pandemic could have been improved as well as crafting a resiliency plan aimed at reducing death tolls of future pandemics. 

HHS received funding for this analysis and hired our consulting firm, FF consulting, to develop machine learning models that could explain which variables were most strongly linked to covid outcomes. HHS specifically was interested not only in different policy explanations, but also asked us to consider demographics such as age and race, the pre-existing health conditions of the populations, income, education, and any other factors we found to be potentially causational. 

## Background:
Both in terms of total deaths, as well as deaths per capita, The United States fared worse than most other countries during the coronavirus pandemic. In the United States, more than 341 people out of 100,000 died due to coronavirus. Only Peru had per population more deaths than the United States (John Hopkins Coronavirus Resource Center). Some states and counties within the United States fared better or worse than others (Lancet study). 

With the pandemic occurring so recently, there are few comprehensive studies examining the links between coronavirus outcomes and different factors such as demographic differences or policy choices. However we were able to find a few studies examining coronavirus outcomes in the United States and abroad. 


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
|Employer_2019|float|Employer sponsored insurance| 
|Non-group|numeric|Non-group| 
|Medicaid|float|Percent enrolled in Medicaid| 
|Medicare|float|Percent enrolled in Medicare| 
|Military|float|Military| 
|Uninsured|numeric|Total Uninsured| 
|Population_Density_per mi2|float|Population Density per sq mile| 
|year Population|float|The population for that year| 
|flu_vaccination_rate_2019|float|the percent of population vaccinated for the flu| 
|asthma_prevalence|numeric|Percent of population diagnosed with asthma| 
|cardiac_mortality_rate|float|population standardized mortality rate| 
|high_bp_prevalence|float|The percent of the population aware of high blood pressure| 
|copd_prevalence|float|The percent of population diagnosed with COPD| 
|kidney_disase_prevalence|float|The percent of the population diagnosed with kidney disease| 
|diabetes_prevalence|float|Percent of population diagnosed with diabetes| 
|Physicians|float|The number of physicians| 
|Physicians Rate|float|The number of physicians scaled to population| 
|Active MO|numeric|Number of Active MO| 
|Active MO Rate|float|The number of active MO scaled to population| 
|Active DO|float|The number of active DO| 
|Dist_Per_100K_year|float|The number of doses of covid-19 vaccine distributed in year by 100k population| 
|Dist_Per_100K_year|float|Population scaled number of doses distributed to individuals over 65|
|Admin_Per_100K_year|float|Population scaled number of doses administered|
|Admin_Per_100K_65Plus_year|float|Population scaled number of doses administered to individuals over 65|
|Additional_Doses_Vax_Pct_year|float|Percent of population receiving a second dose|
|Mandatory|float|The number of days a vaccine mandate was in effect|
|Current President|float|Approval of the current president|
|Your State Governor|float|Approval of the governor of the state|
|Go to Work|float|Percent of respondents who say they go in to work|
|Go to the Gym|float|Percent of respondents who say they go to the gym|
|Go Visit a friend|float|Percent of respondents who stated they visit friends|
|Go to a cafe, bar, or a restaurant|float|Percent of respondents who went to cafes, bars, and restaurants|
|Go to a doctor or visit a hospital|float|Percent of respondents who went to or visited a hospital|
|Go to church or another place of worship|float|Percent of respondents who said they go to a place of worship|
|Take mass transit|float|Percent of respondents who said they take mass transit|
|Avoiding contact with other people|float|Percent of respondents who say they avoid contact with other people|
|Avoiding public or crowded places|float|Percent of respondents who say they avoid public or crowded places|
|Frequently washing hands|float|Percent of respondents who say they frequently wash their hands|
|Wearing a face mask when outside of your home|float|Percent of respondents who say they wear a fask mask outside of their home|
|Been in a room with someone outside of household in the past 24 hours|float|Percent of respondents|
|Yes, 5-10 people|float|Percent of respondents who have been around 5-10 people|
|Yes, 11-50 people|float|Percent of respondents who have been around 11-50 people|
|Yes, 50 or more people people|float|Percent of respondents who have been around 50 ormore people|


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



## Data Cleaning & EDA:
Initial data cleaning of large csv files took place in the Data Collection and Cleaning notebook found in the Code folder. The size of large files was reduced by selecting the minimum variables of interest for time periods of signficance. The smaller dataframes were then saved as CSVs in the code folder and re-accessed in the Data Cleaning and EDA notbeook. We cleaned individual data sets from the various sources and then combined the datasets into a county dataframe and a state dataframe. Most of the data had few typos and errors, however there was missing data for some variables. NJ did not report rates for pre-existing medical conditions in 2019 and therefore the 2018 statistics were substituted in. Other features of interest at the county level such as income by race and other variables by race were dropped due to a large amount of missing data. The segregation index for example was dropped from the final county model to retain as many observations as possible. At the county level, some cases and deaths were attributed to a state but not a specific county. For the county-level analysis, we used counties' share of the states population to re-allocate these cases and deaths to specific counties within a state. While more than 20 states had some unallocated deaths, only a handful had a significant number (more than 1-2% of overall cases and deaths). 

## Modeling:
Our goal with modeling was two-fold:
1. Develop model(s) that predicted Covid-19 outcomes as successfully as possible
2. Develop model(s) that could be used to interpret the relationships between certain features and different outcomes.

We developed models with multiple target variables to understand covid-19 outcomes through a broader lense. We looked at both deaths attributed to covid-19 as well as excess death statistics. Excess deaths were examined due to multiple studies suggesting that covid-19 deaths were being consistently under-reported, especially among poor and minority communities. We also examined covid-19 cases as cases also had a significant impact on populations and communities. When discussing the analysis

As we were concerned with understanding the relationships between specific features and covid-19 outcomes, we first developed white-box linear regression models at both the state and county level. The results of the State models led us to begin the county-level analysis. In the OLS Stats Summary Table for the state-level linear regression model, p-values for specific variables are missing. There are two strong possibilities for why this was the case. First, while the model's r2 metric was very strong, the model contains multiple collinearr variables that can muddy the interpretation of individual variables. Second, at the state level we only had 51 observations including Puerto Rico. This is a very small sample size and makes it difficult to make conclusions about the true relationships between features and the y-variables. 

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
