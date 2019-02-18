---
layout: post
title: "Book AirBnb for Seattle or Boston in these months to get the bang of our buck"
date: 2019-02-12
---

![](/images/Seattle_Boston.jpg)

Some travelers have a tight budget. Some others travel not to go sightseeing but to spend
time with family or friends. They do not need the weather to be gorgeous. They want to 
travel with a low cost. We obtained some AirBnb lodging price data for Seattle and Boston 
via Udacity, an online learning platform and we explore the data to gain insights. If you
fit in the aforementioned traveling types, read on. We have a treat for you. We will tell
you, based on the analysis we perform, what are the best months to travel to these two 
cities and the type of properties that will save you money on lodging. 


# - If money is an issue, visit Seattle in May and September and visit Boston in August and late October.
Seattle is known for its rain and extended days of overcast. In summer, the weather clears up and travelers
flock to Seattle to get close to nature. The AirBnb lodging prices are the highest in summer months (Jun-Aug)
but if visit in May or September and are lucky, you may also experience great weather there. Similarly, in 
Autumn months, travelers flock to New England to see the fall foilage and to enjoy the New England seafood. 
Therefore, in Boston, AirBnb lodging prices are highest in September and October. Visiting in August and late
October/early November will on average, save $40 a night compared to the peak season and also have a chance to
see the early sign or late phase of the fall foliage.

![](/images/2019-02-12_12-51-37.png)

# - Data that we have does not suggest that month is a good predictor for price. 
Based on the data we get, we try to build a predictive model for price on month, property 
type (condominium, villas, dorms etc) and other variables that we thought would be good
predictors for price. However, we do not find month to be good predictors when we aim to
predict prices of individual properties. The graph that was presented earlier was produced 
by aggregating all properties. 

# - Book B&B, Cabin, Chalet, Dorm, or Townhouse to save money in Seattle. 
We performed statistical tests on the variables that we selected for Seattle. Unsurprisingly, 
the number of bathrooms, bedrooms, beds and number of guests a property can accommodate are
all positively correlate to the price. The larger the property and the more guests the 
property can accommodate, the higher the price. We also found a variable that also has strong
predictive power -- the property type. The model tells us that among all the property types,
the price of lodging in dorms are cheapest, then in increasing order, tents, townhouses, houses,
chalets, Other, B&B, cabins, and Bungalows. On the other hand, the price of lodging in Boats 
are the most epxensive, then in decreasing order, Campers/RVs, lofts, condominiums, treehouses
and yurts. Since we have processed our numerical variables, to avoid confusion, in the following 
table, we do not provide the regression coefficients of the numerical variables. We instead 
provide the regression coefficients of each property type along with their p-values. The way 
to interpret the coefficient of each property type is that, imagine everything being equal (i.e.
same number of rooms, same number of beds etc), there is an "average" price, represented by the
model line. The coefficient of each property is then added (if positive) or subtracted (if negative)
from the average price to arrive at the predicted price. That way, we know the more negative a 
coefficient for a corresponding property type, the more money a fellow traveler can save by 
booking such property type. The p-value, on the other hand, tells the fellow traveler how important,
or in statistical terms, how significant, each property type contributes to the final predicted price.
The closer the p-value is to 0, the more significant it is. Any p-value above 0.05 is considered 
statistically insignificant. 

| Property type   | Coefficient | p-value |
|-----------------|-------------|---------|
| Bed & Breakfast | -19.96      | 0.07    |
| Boat            | 102.87      | 0       |
| Bungalow        | -6.50       | 0.72    |
| Cabin           | -10.40      | 0.47    |
| Camper/RV       | 13.76       | 0.44    |
| Chalet          | -27.31      | 0.54    |
| Condominium     | 10.55       | 0.13    |
| Dorm            | -308.68     | 0       |
| House           | -32.19      | 0       |
| Loft            | 12.75       | 0.22    |
| Other           | -21.32      | 0.12    |
| Tent            | -48.82      | 0.13    |
| Townhouse       | -38.75      | 0       |
| Treehouse       | 9.77        | 0.79    |
| Yurt            | 1.75        | 0.98    |
# - Book B&B, Campers/RVs, dorms, entire floor, houses, townhouses, or villas to save money in Boston.
Similar to the lodging prices in Seattle, the lodging prices in Boston also positively correlate to
numbe of bathrooms, bedrooms, beds and the number of guests the property can accomodate. In addition,
property type also plays an essential role in the price of the lodging properties. The model tells us
that among all the property types, the price of lodging in Campers/RVs are cheapest, then in 
increasing order: properties offering the entire floor, dorms, houses, villas, townhouses, B&B, 
and boats. On the other hand, the price of lodging in guesthouses are the most expensive, then in 
decreasing order, lofts, condominiums, and other. Similar to the analysis we provided for Seattle, in 
the following table, we provide the regression coefficient and the p-value of each property type. 

| Property type   | Coefficient | p-value |
|-----------------|-------------|---------|
| Bed & Breakfast | -27.27      | 0.17    |
| Boat            | -15.52      | 0.67    |
| Camper/RV       | -163.89     | 0.19    |
| Condominium     | 7.62        | 0.43    |
| Dorm            | -64.22      | 0.60    |
| Entire Floor    | -93.06      | 0.19    |
| Guest House     | 67.37       | 0.59    |
| House           | -61.72      | 0       |
| Loft            | 42.71       | 0.06    |
| Other           | 7.22        | 0.83    |
| Townhouse       | -28.63      | 0.11    |
| Villa           | -37.68      | 0.67    |


Our analysis also reveals that currently, based on the variables we have, the model still does not have
very strong predictive power. We hope to further incorporate more variables, such as amenities provided, 
into the models and see if we can gain greater insights into the data.

<Disclaimer> The first Boston and Seattle picture is downloaded from https://www.cnbc.com/2015/01/29/who-wins-super-bowl-of-housing-seattle-or-boston.html. 
