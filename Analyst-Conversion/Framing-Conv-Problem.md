# Framing the Problem
## Business Context
The Google March Shop is Google's ecommerce site offering branded-merchandise across various product categories such as apparel, lifestyle, and stationery. The brands represented include Google and google applications (e.g. Google Maps) as well as additional titles* such as Youtube and Android.

[Something about the purpose of such stores for big brands. Revenue always important but obviously not a large revenue driver so there would be other reasons for doing it]

## The Objective
1) Uncover the differences in the buyer's journey for users who convert and who do not, determine where to prioritize marketing spend to boost conversions
2) Enable forecasting of expected conversions on a rolling basis based on data from 3-months-to-date


### Variables of Interest at User Level
visitorid, 1st visit channel, last visit channel, total number of visits, # of visits organic search / social/ direct/ referral/ paid search / affiliates / display / other, continent, subcontinent, country,  # of visits per device category, total hits OR total page views, first session hits OR first session page views, campaign vs not binary 






# Rough Work

## Hypotheses
1. There is a difference between the buyers journey of customers who convert and do not convert in terms of the marketing channels they interact with
2. There is a difference between the buyers jounrey of customers in North America / outside of it? (think i need more EDA before saying something like this)

## Business Objective of Conversion Analytics Initiative
[What are the top conversion paths?]
[Multichannel attribution, optimizing cost per conversion / cost per conversion]
[Understanding buyer's jounrey / profile of users that convert]
[How would creating a predictive model differ from simply doing descriptive statistics?]
[How can we get some of these customers who aren't converting to convert? Who are the customers at the tipping point and how can we get them to purchase? Can bolster this with some research about repeat purchase probabilities or something]


## What exactly are we building that would go into production?
1) A tool which analyzes the data as at this time to predict number of conversions expected within the next month? not sure how to really think of the time horizon detail. 


### Findings from Research
Business would be interested in heuristics like
* First click source (or first visit source in our case) and last click source
* We could transform the dataset to make it per user. Create features for number of visits as at end of observation, first visit channel, last visit channel, binary for if a given channel was used 
* High vs low value question? (as opposed to regression or simple binary classification i guess)
* Could we use Markov chains? Create transition matrix? Except that may not apply since the "conversion" state may never occur, right?
* Could we try that representative sampling based on clustering that we saw in class? Could turn it into kmeans
* Need some meaningful grouping for stuff like region, etc.



### Potential Business Questions
Top Choice (Currently)
What does the buyer journey from first visit to conversion look like? Could we move users through this journey more quickly?


Brainstorm
* What levers within our control can be adjusted to boost expected conversion rates? 
* How could we optimize ad spend based on findings? (this might not be suited to conversion? wouldn't the amount of revenue matter here? or no?)
* Which user profiles should be target ad-spend on? (same question here, not sure if revenue-or-not is enough to direct ad-spend Feels like we should be looking for something that is not sensitive to **how much** we make from them, but just if we make something or not)
* Consumers who are similar to those who convert but don't convert, what's different about them? 