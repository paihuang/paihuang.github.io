---
layout: post
title: "Book AirBnb for Seattle or Boston in these months to get the bang of our buck"
date: 2019-02-12
---

Some travelers have a tight budget. Some others travel not to go sightseeing but to spend
time with family or friends. They do not need the weather to be gorgeous. They wan to 
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
and yurts.

# - Book B&B, Campers/RVs, dorms, entire floor, houses, townhouses, or villas to save money in Boston.
Similar to the ledging prices in Seattle, the lodging prices in Boston also positively correlate to
numbe of bathrooms, bedrooms, beds and the number of guests the property can accomodate. In addition,
property type also plays an essential role in the price of the lodging properties. The model tells us
that among all the property types, the price of lodging in Campers/RVs are cheapest, then in 
increasing order: properties offering the entire floor, dorms, houses, villas, townhouses, B&B, 
and boats. On the other hand, the price of lodging in guesthouses are the most expensive, then in 
decreasing order, lofts, condominiums, and other. 

Our analysis also reveals that currently, based on the variables we have, the model still does not have
very strong predictive power. We hope to further incorporate more variables, such as amenities provided, 
into the models and see if we can gain greater insights into the data.
