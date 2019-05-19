# Introduction
I dread time transaction-type time series data. Typically in such a data set, an entire history of customers' actions and behavior
is recorded. There is structure in the data but it takes great effort to understand the structure and pull the necessary 
information out for analysis. In my data analysis career up to this point, I know for sure it is a great weakness in my skill set.

Pain usually accompanies growth. However, after such growth happens, the reward can be very satisfying. As a result, as a CapStone
project for my [Udacity](http://www.udacity.com) Data Scientist NanoDegree program, among other choices, I pickedd the Starbucks
project. I know this weak link in my analysis ability needs to be addressed. 

In this blog entry, instead of repeating what I already disscussed in the readme file of my github repository (link will be 
provided in the end), I want to discuss about the lessons I learned from this Starbucks project. Hopefully these insights that
were not immediately obvious to me before can also help you in your future data analytics work. 

# Lessons learned
As expected, processing the data does cause some pain. However, I learned the following valuable lessons.
1. **In time-series analysis, the data should be processed as a whole**. My first attempt to build flags to tell if certain events
are considered valid is to separate the data based on events. Next, I stack each event type back and added the necessary flags in 
between. Doing so **severely limits the algorithm to see the whole picture and causes inefficiency**. If only a limited history 
is seen, the algorithm cannot efficiently mark the flags by taking past relevant events into consideration. Also, once the data
is stacked back together, more fixes will be required to accomplish the correctness. It came as a painful truth after I spent a
considerable amount of time on processing and marking the data separately. I realized that localized view of data causes the 
algorithm to incorrectly mark certain events and I will need to develop patches to fix that. Unhappy with the result, I developed
a new algorithm with the full history of a customer in mind. The newly developed algorithm is correct and efficient. The 
resulting code is more readable and it only takes a few hours to write the code.

2. 

# Github repository
You can find the Jupyter notbook and the HTML rendition in my [github repository](https://github.com/paihuang/Starbucks). The
[README.md](https://github.com/paihuang/Starbucks/blob/master/README.md) file contains all necessary techical details and 
discussion as well as the visualization and conclusion developed during the analaysis. 

# Conclusion
