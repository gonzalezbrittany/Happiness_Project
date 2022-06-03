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
 * Random Forest was used to narrow the total variables down to the top 12 variables that impact happiness scores the most. 

**Description of preliminary feature engineering and preliminary feature selection, including the decision-making process:**
 * The target for the machine learning model is happiness scores, this is labeled as “ladder_score” in the analysis
 * Random Forest was chosen to narrow down the number of variables to the twelve most impactful for happiness scores. The below were listed as the top twelve.
  

![image](https://user-images.githubusercontent.com/96347024/171903399-9c1822d3-9c99-4818-ae7c-0034006cd367.png)


 * For this analysis, three machine learning models were chosen: Multiple Regression, Random Forest, and the decision tree. The goal is to see which model predicts happiness scores accurately while also figuring out which variables are statistically significant in the analysis. 


**Description of how data was split into training and testing sets:**
 * Multiple Regression and Random Forest: Default parameters were used to split the data into training and testing sets
 * Decision Tree: 80% train and 20% test
 
**Explanation of model choice, including limitations and benefits:**

* Our first attempt to create an accurate predictive model involved the use of the decision tree. At first the default parameters for splitting the data (75% train and 25% test) were used. However, this produced a very low accuracy score. The model was then rerun with splitting the data between 80% train and 20% test. This did increase the accuracy score slightly to 40%, however, this may cause an overfitting issue when running the same predictive model on new data.  For the third attempt at increasing the accuracy for the decisions tree, we used SMOTE to attempt to correct the imbalance in the dataset prior to re-running the model. Model split did not change (80% train and 20% test). This did bring the accuracy score from to 58.3%. We still are checking to see if there are any additional ways to bring up the accuracy score for this model.

	![image](https://user-images.githubusercontent.com/26393180/171965722-780aecab-1747-4113-9bf5-716a16b7f994.png)


* Since the decision tree shows a very low accuracy score, this may be an indication of a week model due to the dataset being too small. To account for this issue and attempt to strengthen the model, Random Forest was chosen to be our next predictive model. Prior to balancing the data by using SMOTE, the accuracy score was 45.4%. When running SMOTE prior to running the Random Forest model, the accuracy score jumped up to 67.0%. We still are checking to see if there are any additional ways to bring up the accuracy score for this model.

	![image](https://user-images.githubusercontent.com/26393180/171966433-34ddc790-49bd-4e46-90a3-6ab3d2dbed97.png)

* To see if we can find a model that is even more accurate, R was used to create a predictive model using multiple regression. Default perameters were used to split the data between train and test. Our final predictive model for multiple regression shows an accuracy score of 77.2% with five variables being statistically signification: freedom, social_support, percept_corrupt, meat_consumption and generosity. Between the three models, multiple regression is the best predictive model to predict happiness scores.

	

------------------------------------------------------------------------------

### Dashboard

**Storyboard on a Google Slide(s):**

https://docs.google.com/presentation/d/1Ko_ZfZzVwHrFdawHIv6q_K8g7W08cQ5EWS1CUCs4c8I/edit?usp=sharing


**Description of the tool(s) that will be used to create the final dashboard:**

Dashboard has been created and Published on Tableau Public
https://public.tableau.com/app/profile/christina.elenbaas/viz/Happiness_AWS/WorldHappiness

<img width="800" alt="World Happiness" src="https://user-images.githubusercontent.com/96347024/171909393-90ad233f-322b-49c6-a996-49f5066e1214.png">



**Description of interactive element(s):**


-Filters for Region and Country Name are in the top right of each Dashboard

-Additional Filtering is available on the Map, bar graph and the Ledged of the Scatter plots


---------------------------------------------------------------------------

[Presentation Draft](https://docs.google.com/presentation/d/1FTfu_1N8J6h3-7x8WgbGIEKKDn-arSCbyVsIBhNfVoQ/edit?usp=sharing)

---------------------------------------------------------------------------

---------------------------------------------------------------------------

**Data Sources:**
 - [World Happiness Data](https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2021)
 - [Covid Data](https://ourworldindata.org/covid-cases)
 - [Alcohol Consumption by Country](https://worldpopulationreview.com/country-rankings/alcohol-consumption-by-country)
 - [Meat Consumption, Median Age, Suicide Rate](https://www.kaggle.com/datasets/daniboy370/world-data-by-country-2020)
 - [Land Use and Density](https://data.world/jst5th/country-population-land-area-density)
 - [Average Screen Time](https://www.comparitech.com/tv-streaming/screen-time-statistics/)

----------------------------------------------------------------------
-----------------------------------------------------------------------------

## Checklist (Segment 3)

### Presentation
 - ~~Select Topic~~
 - ~~Reason for selected topic~~
 - ~~Description of the source of the data~~
 - ~~Questions we hope to answer with the data~~
 - ~~Description of the data exploration phase of the project~~
 - ~~Description of the analysis phase of the project~~
 - Technologies, languages, tools, and algorithms used throughout the project
 - **Slides**
     * Presentation is drafted in google slides

### GitHub Repository
 -  **Main Branch**
     *  ~~All code necessary to perform exploratory analysis~~
     *  ~~Some code necessary to complete the machine learning portion of the project~~
     *  All code is production ready
 -  **README.md**
     *  remove description of communication protocols
     *  Cohesive, structured outline of the project (this may include images, but they should be easy to follow and digest)
     *  Google Slides Link: 
 -  **Individual Branches**
     *  ~~At least one branch for Each team member~~
     *  ~~Each team member has at least four commits for the duration of the second segment~~

### Machine Learning Model
 - ~~Description of data preprocessing~~
 - ~~Description of feature engineering and feature selection, including the decision-making process~~
 - ~~Description of how data was split into training and testing sets~~
 -  ~~Explanation of model choice, including limitations and benefits~~
 -  ~~Explanation of changes in model choice (if changes occurred between the Segment 2 and Segment 3 deliverables)~~
 	* no changes
 -  ~~Description of how they have trained the model thus far, and any additional training that will take place~~
 -  ~~Description of current accuracy score~~

### Database Integration
  <There are no deliverables for the database integration section of the project for this segment.>

### Dashboard
 - Images from the initial analysis
 - Data (images or report) from the machine learning task
 - At least one interactive element
 - The dashboard presents a data story that is logical and easy to follow for someone unfamiliar with the topic. It includes the following:


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
 -  ~~Explanation of model choice, including limitations and benefits~~

### Database Integration
  - ~~Database stores static data for use during the project~~
  - ~~Database interfaces with the project in some format (e.g., scraping updates the database)~~
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
