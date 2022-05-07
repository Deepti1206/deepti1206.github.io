# Impact of City health services on Public health in the United States

[PLACES](https://www.cdc.gov/places/index.html), the expansion of The 500 Cities Project, is a partnership project between the Center for Disease Control (CDC) and the Robert Wood Johnson. It focusses on new approaches towards model-based analysis of health estimates for local areas across the United States. For the first time, it supplied data for cities and census tracts, many of which covered multiple counties or did not follow county lines. These data can be filtered (by city and/or tracts, as well as by measure) and downloaded by end-users for use in different analyses. 

The initiative provided the display, retrieval and exploration of health care data for the largest 500 cities at the selected city and tract level on the habits, and risk factors that have a significant impact on the health of the population. 

## Objective
The aim is to identify metrics and measures in the cities that predict the public health outcomes and can help to take preventive measures against the disease. 

The analysis enables local health departments and authorities to better understand the burden and geographic distribution of health measures in their areas, independent of population size or rurality, and to aid them in planning public health actions. This project employed small area estimating methods to acquire 27 chronic illness indices for the 500 largest American cities by reporting city and census tract-level data. Visitors were allowed to refer, browse and download the data at city and tract levels, which was made public through the “500 Cities” website. 

Despite the fact that data at the county and metropolitan levels was limited, this study was a first-of-its-kind data analysis that released information on a broad scale for cities and local areas within cities. This approach supplemented current surveillance data, allowing researchers to gain a better understanding of the health challenges that people of that city or census tract face. 

## How the data was collected?
The Center for Disease Control (CDC) has collected the data primarily from the CDC Behavioral Risk Factor Surveillance System, the Census 2010 population and the American Community survey. The only data used will be the CDC’s 2018 500 Cities Data. The Center for Disease Control is open about its data and techniques, as well as the limitations and issues, and their data is in the public domain (such as self-reported data). As a result, they’re perhaps the most reliable source of information on the subject.

The Centers for Disease Control and Prevention (CDC) is the public health agency of the United States of America. It works around the clock to protect America from both foreign and domestic health, safety, and security threats. CDC helps communities and citizens confront disease, whether it originates at home or abroad, is chronic or acute, curable or avoidable, caused by human error or a premeditated attack. As the nation’s health protection agency, the CDC saves lives and protects individuals from health threats. It conducts critical research and disseminates health information to protect the United States from hazardous health problems, as well as responding to them when they arise. 

The PLACES Project took over from the 500 Cities Project in December 2020. It was a collaboration between the Centers for Disease Control and Prevention, the Robert Wood Johnson Foundation, and the CDC Foundation. It offered small area estimates for chronic disease risk factors, health outcomes, and clinical preventive care utilization for the major 500 cities in the United States at the city and census tract level. These small-area estimates aided cities and local health departments in better understanding the burden and spatial distribution of health-related factors in their jurisdictions, allowing them to better plan public health interventions. 
Individual cities and groupings of cities, as well as other stakeholders, might have used this high-quality, small-area epidemiologic data to assist create and implement effective and focused prevention programs, identify developing health problems, and establish and monitor critical health targets. 
City planners and elected officials, for example, may have wished to utilize this information to target neighborhoods with high rates of smoking or other health-risk behaviors for successful interventions. 

The data is heavily skewed in favor of a few states. We can’t assume that what works in California will work in Alaska for a variety of reasons, including culture, legislation, and weather. However, only one city was studied in 11 states, whereas California had 83. As a result, the client’s location may have an impact on the accuracy of my findings. This occurred as a result of the study’s initial focus on the country’s largest cities, followed by the addition of a few more to ensure that every state was covered. Given this, it’s natural if you’re concerned about how this would affect a small community. 

The good thing about the dataset is that it is organized in a dataframe hence making it easier for analysis. 

However, the dataset is not clean i.e there are unnecessary and null values in the data set that needs to be cleaned. Hence, we will do a data cleaning for accurate analysis and predictions. The dataset is available in the public domain making it easier for researchers and analysts to use it and make recommendations to the relevant stakeholders. 

Here we are trying to find tyhe solution for the given questions:
* Does the city make a difference in how much a population uses preventative services?
* Can Cities Impact Healthy Behaviors? 
* What can the city do to drive greater use of the services? 

The variables which are likely to be used for study are  preventive measures and healthy behaviors where the city can have direct influence, which may then impact the health outcomes. For this , we will carry out hypothesis testing and  begin by looking at preventative services which consist of a number of outcomes.
We will also use this dataset to predict if the measures taken by cities have a significant influence on the healthy behaviors within the population. Some of the variables that will help answer this question include:\ “No leisure-time physical activity among adults aged >=18 Years” (LPA) ”Sleeping less than 7 hours among adults aged >=18 Years” (SLEEP) “Binge drinking among adults aged >=18 Years” (BINGE) ”Current smoking among adults aged >=18 Years” (CSMOKING)  

## Methodology
We will be using RStudio to analyze the dataset . The necessary R packages and libraries include: 
```
library(ggplot2) #for visualization
library(tidyverse) #for cleaning the dataset 
library(dplyr)  #for data manipulation
```
As the data may contain missing values or unnecesarry features, we will follow the data pre-processing which includes data cleaning and feature selection:

* Removal of variables that are not necessary for analysis  
* Removal of duplicates. 
* Removal of extreme values 
* Selection of important features 

## Descriptive analysis
In order to perform the data pre-processing and analysis first step is to understand about your data.
```
#Loading the dataset
data_health<-read.csv("500_Cities__Local_Data_for_Better_Health__2019_release.csv",header=T)
str(data_health)

#the summary output
![Image](src)





You can use the [editor on GitHub](https://github.com/Deepti1206/deepti1206.github.io/edit/main/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Deepti1206/deepti1206.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
