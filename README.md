# Faith Based Nonprofit Survivability

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

This data was extremely limited (less than 100 NPs) and was very unbalanced (We had less than 100 NPs that had closed in the dataset). This means that our findings are not necessarily representative of the population and can be very misleading. Though I will state my findings regardless, please keep this all in mind.

## Findings

### Founders
![image](https://user-images.githubusercontent.com/77307911/115101678-c1371000-9f0b-11eb-8f48-225261eec77c.png)

The average age of the founders when starting a nonprofit ranged mainly from 40-50.

![image](https://user-images.githubusercontent.com/77307911/115101718-225ee380-9f0c-11eb-8dfd-bb3aca9d5917.png)

Nonprofits that stayed open had an average number of hours worked a month that was 3x higher than nonprofits that ended up closing

![image](https://user-images.githubusercontent.com/77307911/115101745-55a17280-9f0c-11eb-970d-23eec0da557c.png)

Founders who came from the professions; Legal, Police, Firemen or Financial professions were more likely to have their Nonprofits close than those from other professions

### Budget

Nonprofits that created a budget were 2.6 times more likely to stay open than those who did not. The budget/revenue of a NP is very important when determining survivability

![image](https://user-images.githubusercontent.com/77307911/115101822-d3657e00-9f0c-11eb-898e-c248712c461e.png)

Nonprofits that served their own financial supporters where more likely to close than those that served people outside of their financial supporters.

![image](https://user-images.githubusercontent.com/77307911/115101897-42db6d80-9f0d-11eb-9c7d-876a5146da58.png)

Nonprofits that did not have any portion of their budget coming from private gifts/donations had a close rate of 16.35% vs 2.51% of NPs that did receive revenue from this source

![image](https://user-images.githubusercontent.com/77307911/115101941-8afa9000-9f0d-11eb-9380-a838db9ff8e3.png)

This was an obvious one, but NPs with a higher overall revenue were more likley to stay open

![image](https://user-images.githubusercontent.com/77307911/115101954-ad8ca900-9f0d-11eb-9c82-390b525d03ba.png)

NPs that remained open obtained funding from a more diverse range of sponsors, and had a large part of their revenue coming in from the sale of goods, unlike those NPs that  closed

### miscellaneous 

![image](https://user-images.githubusercontent.com/77307911/115102164-de211280-9f0e-11eb-9417-e9e7c36d3626.png)

NPs that serve South America and Africa are 2-3 times more likely to close than others.

![image](https://user-images.githubusercontent.com/77307911/115102220-0e68b100-9f0f-11eb-9423-ac9f2025e77f.png)

NP whose workers attend religious services on a regular basis are way more likely to stay open

Additionally we found that NPs that:
- Have a Facebook account
- Have a Twitter account
- Have a website
- Have opened a bank account
- Have gained tax exempt status from the IRS
- Have a physical space for their NP
Are more likely to stay open

## Predicting Survivability
We were able to produce a Random Forest model that could predict the survivability of a Nonprofit with an accuracy of 96.01% which was slightly better than the baseline model

## Conclusions
There just wasnt enough data in this dataset, nor a good enough spread of closed to open NPs (even when using oversampling techniques to counteract this), to accurately provide feedback and recommendations, let alone come to any solid conclusions. The findings are interesting at best. 

We did, however, manage to produce a very accurate model that could be implemented into production to predict the survival of any NP.

## Recommendations
Since the data in this project is misleading, my recommendations will not be focussed on them. Instead I recommend:
- That Nonprofits be educated as to the importance of proper data collection, storage and analysis. They need to understand the benefits to themselves and the community at large that would come from this endevour. 
- We need to work with NPs to help them formulate effective surveys/data collection. Bad data = Bad models and erroneous recommendations. One idea is to make surveys 100% online to reduce user error, illegibility, and the occurance of missing values (We can do this by making it impossible to move on to the next question without completing the current one.
- We can create incentives for survey takers. Most people hate surveys, but everyone loves free stuff. Offer survey takers a free gift or a small gift card.
- Lastly, once this data is obtained, make it freely and easil available to the public and other Non-profits so that the community at large can benefit from it.

