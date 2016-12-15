Overview: 
_________

"Exploration of Growth in Female Farmers in California, 2002-2012"

This is part of the final project for Data Science in Public Policy class at the Goldman School of Public Policy at the University of California, Berkeley. Using time series data from the USDA Census of Agriculture from 2002, 2007, and 2012, I aimed to develop a model to predict whether tenure status (owner vs renter) will change for the female farmer population in California. 

A few studies estimate that by 2030, women over 60 may own about 75 percent of transferred farmland in the U.S.. This is often  combined with the assumption that female land owners/farmers are more inclined to implement sustainable agricultural practices or lease to tenants who are inclined to do so. Understanding what factors or parameters might predict tenure change for female farmers can help government geographically target policies and resources specific for female owners and renters. 

Data:
_____

NASS Quick Stats Dashboard: https://quickstats.nass.usda.gov/?source_desc=CENSUS

Getting Started
_______________

Download “CA_FINAL.csv” and save to desired directory
Download “Final_Project_Markdown.Rmd” and save to the same directory

Prerequisites
___________

R software (I used version 3.3.2)
RStudio (I used 1.0.44)
RStudio packages: 

library(maps) # mapping
library(ggplot2) # mapping + plotting package 
library(choroplethr) # mapping 
library(tidyverse) # pipe operator +
library(lubridate) # helps with strings 
library(gmodels) # helps tabulate  

Maps and Graphs:
________________

county_map: map of the change in female farmer population for each county in California

county_map_2012: map of the percentage of female farmers among all farmers by county in 2012

change_tenure: graphs the change in tenure status from 2002-2012 in California


Issues and Potential Bugs:
__________________________

California - value column includes a mixed bags of values including totals of acres, total of acres by crops, total number of operators, total number of farms operated by a female farmer. The code aims to parse all of these different totals out, place them in separate columns, and merge them all into a final data frame. 
 
The final merging steps need to be refined and bugs fixed. The data frames that are pending merge are:

CA_dummies
Tenure_spread
CA_fops_only 

Presentation:
____________

Female Farmers in California.pdf - summarizes project and includes county_map, change_tenure, and table ranking crops by acreage in CA. 

Author: 
______
Hortencia Rodríguez
MPP Candidate ‘17 
hortencia.c.rodriguez.s@gmail.com