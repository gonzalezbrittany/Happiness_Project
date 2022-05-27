# Happiness Project


**Project Outline:**


## Requirements

-----------------------------------------------------------------------
### Presentation


**Topic:** World Happiness Report 2021


**Reason why we selected our topic:**  
Our team explored various data sets such as Olympic data, Zillow housing data, NBA player statistics and the World Happiness data.  

As we chatted about what insights we could gain from the analysis we decided the features and information available within the World Happiness data was what we wanted to explore.

**Description of source data:**
The World Happiness Report 2021 focuses on how people all over the world have coped with the effects of COVID-19.  The data set has two focuses, first the effects of COVID-19 on the structure and quality of people’s lives, and second to describe and evaluate how governments all over the world have dealt with the pandemic. The purpose of the data is to help to try and explain why some countries have done better than others.


**Questions they hope to answer with the data:**
By applying the most advanced techniques of Machine Learning, it would be possible to define the most important factors and measure quantitatively their contribution to one’s happiness.

Our team is hoping to apply advanced techniques with Machine Learning to define the most important factors to measure and compare and enhance countries happiness scores.

We are also looking into other measures not explored in the happiness dataset to see what kind of correlation other factors might have with the happiness data.

**Description of the data exploration phase of the project:**
We took several different data sets that reported their data by country and loaded them each into their own postgres SQL table. 

**Description of the analysis phase of the project:**
In SQL view to check how each country was reported in each data set to check for spelling differences or abbrivations. After identifying the different ways a country was referred to we created a cross reference table that we could join each of the data sets to. Then we combined all the datasets in a view that could be used when creating the machine learning model.

----------------------------------------------------------------------

### Git Hub


**Description of the communication protocols:**
Our team has agreed to use Slack direct messages to communicate.  All members are aware and active on the message string that was created May 5, 2022.

---------------------------------------------------------------------------

### Machine Learning Model


**Description of preliminary data preprocessing:**
 * CSV files were imported into Jupyter notebook
 * All column headers for each CSV file were reviewed, if column names containing same variable did not match between files, this was corrected.
 * All variables under “country_name” were reviewed. Country names that appeared multiple times were reviewed, any country names with slightly different spellings  	were corrected. 
 * Missing Region info for countries were researched and added to designated columns in each file. 
 * After all tables were combined into one master dataset table, Jupyter notebook was utilized to determine column NA count. All columns that had over 50% missing      values were removed.
 * All rows still containing missing values in the master dataset table were also removed.
 * Random Forest was used to narrow the total variables down to the top 10 variables that impact happiness scores the most. 

**Description of preliminary feature engineering and preliminary feature selection, including the decision-making process:**
 * The target for the machine learning model is happiness scores, this is labeled as “ladder_score” in the analysis
 * Random Forest was chosen to narrow down the number of variables to the ten most impactful for happiness scores. 
 * For this analysis, three machine learning models were chosen: Multiple Regression, Random Forest, and the decision tree. The goal is to see which model predicts happiness scores accurately while also figuring out which variables are statistically significant in the analysis. 


**Description of how data was split into training and testing sets:**
 * Multiple Regression and Random Forest: Default parameters were used to split the data into training and testing sets
 
**Explanation of model choice, including limitations and benefits:**

------------------------------------------------------------------------------

### Dashboard

**Storyboard on a Google Slide(s):**

https://docs.google.com/presentation/d/1Ko_ZfZzVwHrFdawHIv6q_K8g7W08cQ5EWS1CUCs4c8I/edit?usp=sharing


**Description of the tool(s) that will be used to create the final dashboard:**

Dashboard will be created using Tableau


**Description of interactive element(s):**

-Map will allow users to click and filter additional graphs on the page
-Happiness by Region will allow users to click and see details for that region
-Region Deep Dive will have filter to explore a specific region and or a country within that region


---------------------------------------------------------------------------

[Presentation Draft](https://docs.google.com/presentation/d/1FTfu_1N8J6h3-7x8WgbGIEKKDn-arSCbyVsIBhNfVoQ/edit?usp=sharing)

---------------------------------------------------------------------------

---------------------------------------------------------------------------

**Data Sources:**
 - [World Happiness Data](https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2021)
 - [Covid Data](https://ourworldindata.org/covid-cases)
 - [Alcohol Consumption by Country](https://worldpopulationreview.com/country-rankings/alcohol-consumption-by-country)
 - [Meat Consumption, Median Age, Suicide Rate](https://www.kaggle.com/datasets/daniboy370/world-data-by-country-2020)
 - [Land Use and Density](https://en.wikipedia.org/wiki/Land_use_statistics_by_country)
 - [Average Screen Time](https://www.comparitech.com/tv-streaming/screen-time-statistics/)

----------------------------------------------------------------------
-----------------------------------------------------------------------------

## Checklist (Segment 2)

### Presentation
 - ~~Select Topic~~
 - ~~Reason for selected topic~~
 - ~~Description of the source of the data~~
 - ~~Questions we hope to answer with the data~~
 - ~~Description of the data exploration phase of the project~~
 - ~~Description of the analysis phase of the project~~

### GitHub Repository
 -  **Main Branch**
     *  ~~All code necessary to perform exploratory analysis~~
     *  ~~Some code necessary to complete the machine learning portion of the project~~
 -  **README.md**
     *  ~~includes description of communication protocols~~
     *  ~~Includes outline of the project (may include images but should be easy to follow)~~
 -  **Individual Branches**
     *  ~~At least one branch for Each team member~~
     *  ~~Each team member has at least four commits for the duration of the second segment~~

### Machine Learning Model
 - ~~Description of preliminary data preprocessing~~
 - ~~Description of preliminary feature engineering and preliminary feature selection, including the decision-making process~~
 - ~~Description of how data was split into training and testing sets~~
 - Explanation of model choice, including limitations and benefits

### Database Integration
  - ~~Database stores static data for use during the project~~
  - Database interfaces with the project in some format (e.g., scraping updates the database)
  - ~~Includes at least two tables (or collections, if using MongoDB)~~
  - ~~Includes at least one join using the database language (not including any joins in Pandas)~~
  - ~~Includes at least one connection string (using SQLAlchemy or PyMongo)~~

### Dashboard
 - ~~Storyboard on a Google Slide(s): https://docs.google.com/presentation/d/1Ko_ZfZzVwHrFdawHIv6q_K8g7W08cQ5EWS1CUCs4c8I/edit?usp=sharing~~
 - ~~Description of the tool(s) that will be used to create the final dashboard~~
 - ~~Description of interactive element(s)~~

------------------------------------------------------------------------

## Checklist (Segment 1)

### Presentation
 - ~~Select Topic~~
 - ~~Reason for selected topic~~
 - ~~Descripiton of the source of the data~~
 - ~~Questions we hope to answer with the data~~

### GitHub Repository
 -  **Main Branch**
     *  ~~Main branch includes README.md~~
 -  **README.md**
     *  ~~README.md includes description of communication protocols~~
 -  **Individual Branches**
     *  ~~At least one branch for Each team member~~
     *  ~~Each team member has at least four commits for the duration of the first segment~~

### Machine Learning Model
 - ~~Takes in data from the provisional database~~
 - ~~Outputs label for input data~~

### Database Integration
  - ~~Sample data that mimics the expected final database structure or schema~~
  - ~~Draft machine learning model is connected to the provisional database~~

### Dashboard
 - <Nothing>



## Final Deliverable Outline
- Project Overview
- Usage and installation instructions of libraries/tools that are used
- Intro (business question and motivation)
- Group by world geographic regions: 
	* Which region had the highest happiness scores overall during 2021? (Bar Graph?)
	* What variables have the strongest impact on happiness scores for each region? (correlation plot)
	* How has the happiness score changed overtime for each region? (plot mean, maybe line plot?)
  	* Is there a way to predict happiness scores based on the 7 variables provided? If so, what model can be used to accurately predict happiness? (Try Multiple Regression, Decision Tree and Random Forest) 
- Data pre-processing/gathering steps (cleaning and manipulation)
- Visuals and explanations
- Machine Learning / Deep Learning Modeling
- Additional explanations
- Major findings
- Conclusion
- References
- Team Members

