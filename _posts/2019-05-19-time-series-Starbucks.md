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

2. **Pick the right tool when you derive a variable whose information needs to be carried forward**. When we create a variable and
want to carry information forward we need to strategically put the right values in certain rows. In the rows that need such
information propagated, we need to assign a missing value (or NaN). My first attempt to do that was to use logical statements to 
create boolean indices and then assign the rows the correct type of information. The code is hard to read and look cumbersome. Not
happy with the result, I then use the right tool: **pandas dataframe apply() function with a powerful lambda function**. The 
resulting code looks clear and accomplishes everything I need to do in one step. If the lambda function grows long, then 
**consider develop a named function as a utility function and pass it into the apply() function** to enhance readability. 

# Github repository
You can find the Jupyter notbook and the HTML rendition in my [github repository](https://github.com/paihuang/Starbucks). The
[README.md](https://github.com/paihuang/Starbucks/blob/master/README.md) file contains all necessary techical details and 
discussion as well as the visualization and conclusion developed during the analaysis. 

# Conclusion
Growth is not easy. It requires introspection to understand one's own weakness and the motivation to address it. In the CapStone
project there are other choices: image classification for dog breeds and customer segmentation data from Avarto. These projects
are by no means any simpler than the Starbucks project but choosing these projects will put me right in my comfort zone: I have
worked on image classification problem and the customer segmentation project in my first term of Udacity Data Scientist NanoDegree
program. I would go back to my early code and start by copying and pasting. This would have been the easier route for me. However
I know that if I don't spend time with time-series transaction data, this weakness will haunt me and quite possibly will cost me
a carrer opportunity in the future. I took myself out of the comfort zone and spend time to understand the data. In several 
occassions, I was unhappy with the efficicy of the code I write and then developed another algorithm or startegy to accomplish
both space and computational efficiency. Was it painful? Yes, of course. But the sense of accomplishment, the actions that were
undertaken to address the technical weakness and the results as well as the growth after the work completion makes the pain all
worthwhile.
