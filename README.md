# Using Topic Modelling to Explore the Association between Neighborhood Reputations and Demographic Composition
This repository contains all the codes and partial resutls from my master thesis: Using Topic Modelling to Explore the Association between Neighborhood Reputations and Demographic Composition. This master thesis was finished in June 2022. Below is the descritpion of all the documents in this repository.

*Click [here](https://lijunpeng66.github.io/master_thesis_neighborhood_online_reputation/) for chekcing the interactive maps*

# Thesis Abstract 
Neighborhood reputations are the opinions and assessments ascribed to them by residents and non-residents. Neighborhood reputations can affect residents' social status, housing, schooling choices, moving intentions and well-being, with potential consequences for inequality and residential segregation. This paper examines the relationship between neighborhood reputations and neighborhood demographic composition in Stockholm municipality in Sweden. The primary source of information is posts from Flashback, a Swedish online open forum. Previous research has used interviews and questionnaires to measure neighborhood reputations in a general way but has not focused on specific dimensions of neighborhood reputation. For example, a neighborhood may have a bad reputation because it is associated with crime or poor infrastructure or may have a good reputation because its residents are economically advantaged or because it has many amenities. Social media platforms provide rich text data facilitating cultural research. These text data potentially cover a greater number of neighborhoods and can capture publicly visible reputations rather than privately held views of reputations. I apply latent Dirichlet allocation (LDA), a natural language processing technique, to detect neighborhood reputations from Flashback posts. Then, I analyze the relationship between neighborhood mentions and neighborhood demographics using SCB1 (Statistics Sweden) data with the Poisson model. Finally, I explore the association between topic scores and neighborhood demographics by calculating bivariate associations. I found that neighborhoods with more non-European residents can trigger more online discussions, and these discussions are likely to associate with the crime and immigrant topics. The topic of crime is also prevalent in communities with low socioeconomic status. The topic of high status is related to affluent areas. The topic of immigrant has a close relationship with communities where residents have low educational attainments. Results imply that ethnic composition, financial status and education can also affect the online reputations of communities.

**Keywords** Neighborhoods reputation, Text analysis, Topic modeling, LDA, Flashback

# Codes description

## 1. Neighborhood name list and Flashback Data.Rmd
This file includes forming a neighborhood name list, extracting neighborhood-related posts and listing descriptive statistics for selected posts. Neighborhood names were extracted from OpenStreetMap at the "suburb" level (Padgham & Lovelace, 2022) combining neighborhood names from other 3 sources: Sweden regional statistical areas (RegSo, Församlingar (parish division), Utsatta områden (vulnerable areas listed by police). I wrote a function to detect the posts that include neighborhood names from the name list (i.e., neighborhood posts). Neighborhood yearly mentions on the Swedish online open forum were plotted in this file.

## 2. Topic modeling - perform LDA.Rmd
The file includes 1) data preparation for the LDA model; 2) fitting the LDA model (Jones, 2021; Welbers, 2018/2022), reading LDA outcomes; 3) forming the lists of neighborhood posts; 4) calculating neighborhood topic scores (i.e., the probability of each neighborhood being discussed in each topic); 5) and testing the optimal number of topics with the whole and sample data (Nikita, 2020).

## 3. Combine demographic data and LDA outcomes.Rmd
The file has the following processes:
1.	Import 3 datasets: RegSO names and neighborhood posts, yearly neighborhood mentions and neighborhood topic scores.
2.	Import and process demographics that were downloaded from SCB. These variables are Education, Gender, Birthregion, Household type, High and low economic standard and Age.
3.	Combine neighborhood demographics with topic scores. Calculate average topic scores. Generate variable descriptive statistics. Subset demographic data for Stockholm municipality from Stockholm County.
4.	Measure bivariate associations between topic scores and demographics.
5.	Run the Poisson model.
6.	Finally, I mapped (Nowosad, 2021; Tennekes et al., 2022) demographics and topic scores for Stockholm County and Stockholm municipality.

## Packages: 
Programming language: R

Version of program: R version 4.0.4 (2021-02-15)

"tibble"	
"knitr"	
"tidyverse"
"dplyr"	
"kableExtra"	
"knitr"
"qdap"	
"lubridate"	
"kableExtra"
"tidytext"	
"tibble"	
"topicmodels"
"tm"	
"dplyr"	
"lubridate"
"ggplot2"	
"qdap"	
"quanteda"
"tidyverse"
"tidytext"	
"ldatuning"
"rgeos"	
"tm"	
"SnowballC"
"rgdal"	
"ggplot2"	
"textmineR"
"stopwords"
