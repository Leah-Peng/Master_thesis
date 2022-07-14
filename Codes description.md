# R programming information

## Programming language: R
## Version of program: R version 4.0.4 (2021-02-15)

## 1. Neighborhood name list and Flashback Data.Rmd
This file includes forming a neighborhood name list, extracting neighborhood-related posts and listing descriptive statistics for selected posts. Neighborhood names were extracted from OpenStreetMap at the "suburb" level (Padgham & Lovelace, 2022). Then combine names with other sources of names. I wrote a function to detect the posts that include names from the name list (i.e., neighborhood posts). Neighborhood yearly mentions were plotted in this file.

## 2. Topic modeling - perform LDA.Rmd
The file includes 1) data preparation for the LDA model; 2) fitting the LDA model (Jones, 2021; Welbers, 2018/2022), reading LDA outcomes; 3) forming the lists of neighborhood posts; 4) calculating neighborhood topic scores (i.e., the probability of each neighborhood being discussed for each topic); 5) and testing the optimal number of topics with whole and sample data (Nikita, 2020).

## 3. Combine demographic data and LDA outcomes.Rmd
This third file has the following processes:
1.	Import 3 datasets: RegSO names and neighborhood posts, yearly neighborhood mentions and neighborhood topic scores.
2.	Import and process demographics that download from SCB. These variables are Education, Gender, Birthregion, Household type, High and low economic standard and Age.
3.	Combine neighborhood demographics with topic scores. Calculate average topic scores. Generate variable descriptive statistics. Subset demographic data for Stockholm municipality from Stockholm County.
4.	Measure bivariate associations between topic scores and demographics.
5.	Run the Poisson model
6.	Finally, I map (Nowosad, 2021; Tennekes et al., 2022) demographics and topic scores for Stockholm County and Stockholm municipality.

## Packages: 
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
	　	　
