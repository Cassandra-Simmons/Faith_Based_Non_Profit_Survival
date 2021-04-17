# Faith_Based_Non_Profit_Survival

## Objective

Data describing multiple characteristics of various faith-based non-profits. The goal is to use this data to predict if a non-profit is likely to stay open or close.

## Background
Data was obtained from multiple faith-based nonprofits, including Athiestic, Muslim, Christian, Buddist etc. The survey was filled out by hand and then read into the system using available software. Data can be found at https://www.thearda.com/Archive/Files/Codebooks/NONPROF11_CB.asp

## Cleaning and Considerations
Data was messy and contained many missing values that had to be infered and dealt with using a variety of methods. For those interested in technical details please the .ipynb file in the repo. 

Some features/columns were dropped out of the analysis for reasons varying from ambiguity to irrelevance. Of the features that remained, many facets possibly contributing to the survivals of the organization were listed. Some of these included:
- Questions concerning their budgets: Who were their sponsors? What percentage of their budget came from certain sources? What was their revenue the previous year?
- Questions about their founders: What was their previous profession before starting the NP? How old where they? How many founders started it? How many of the original founders were still involved?
- Questions about members & founders: How many hours per month did they work? Were they paid? How many paid vs unpaid hours did they volunteer? How often do they attend religious services? What are their personal religious experiences? How much of an impact did family and friends play?
- Questions about the organization: What religious affiliation were they? What countries did they serve? What services did they offer?

## Findings

### Founders
![image](https://user-images.githubusercontent.com/77307911/115101678-c1371000-9f0b-11eb-8f48-225261eec77c.png)

The average age of the founders when starting a nonprofit ranged mainly from 40-50
