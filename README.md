# Tableau-Project
# Project 2: 

# Team Name and Members 
Group 9 <be>

Claire Friers - cef19295@uga.edu <br/>
Anastasia Draughn - agd82889@uga.edu <br/>
Justin Tran - jat966554@uga.edu <br/>
Jack Saylor - jds56127@uga.edu <br/>
Ayaan Godil - aag53475@uga.edu

# Description of Data Set
This dataset contains real estate transactions in Conneticut from 2001 through 2022. The data was obtained from the Conneticut State Department of Housing's open data resources. It includes 1,097,629 rows and 14 columns, with each row representing a property sale. 

Each sale in the dataset is identified by a unique serial number and includes the list year and the date the sale was recorded. The dataset also gives location information such as the town and street address where the sale was made. Financial data includes the assessed value of the property at the time of the sale, the actual sale amount, and the sales ratio.

The dataset also categorizes the properties by type. This inlcudes Residential, Commercial, or Vacant Land, and specifies residential further into Single Family, Two Family, Three Family, and Four Family homes. 

Some sparsley populated fields include Non Use Code, Assessor Remarks, and OPM Remarks. These provide optional context or notes relevant to special use cases.

Data types include integers for identifiers and years, floating-point numbers for monetary values, and string/object types for descriptive attributes.

Overall, this dataset offers a comprehensive view of two decades of property sales in Connecticut and is well-suited for time-series analysis, price distribution studies, and housing market segmentation.

# Manipulation of Data Set 

![Screenshot 2025-04-28 at 6 32 28 PM](https://github.com/user-attachments/assets/a066956b-6b5f-42c9-a9ed-7a62c0f2b3dc)

To break up differing wealth classes in tableau, we had to create the above calculated field in Tableau. This takes the results from our box and whisker plot that breaks down the average home sales amounts across towns and puts them into one of the four categories we defined.

![calc](https://github.com/clairefriers/Project2/blob/main/calc.png)

To conduct the analysis of my second question, we had to create the above calculated field in Tableau. This is a year over year growth rate in median home sale prices across the filtered towns. The importance of using this calculation is because we want to assess relative changes across towns rather using the absolute numbers since there can be a lot of variation in the towns.
The next thing we did was make it so we were only analyzing data from 2005 through 2011. This enables us to keep the graph readable and easy to signal in on the years that are important for answering our question in a short term impact analysis. Which in this case is looking at the 3 years before, the year or and the 3 years after the 2008 recession.
Finally we also chose to only look at 9 towns, filtering 3 low price, 3 middle price and 3 high price towns. Since we put these each on 3 different graphs, I edited the y axis ranges to keep the visualizations consistent to enable fair comparisons. 


# Question 1 
“How has the number of houses bought in each wealth class changed over the years?”

We created a calculated field that categorizes properties into Lower, Lower-Middle, Upper-Middle, and Upper Class based on the quartiles determined from a box-and-whisker plot in Tableau.

![image](https://github.com/user-attachments/assets/f28b79da-d33c-40ad-b2e5-b1bbc36dfed2)


![image](https://github.com/user-attachments/assets/4383b9cf-2746-4fee-93e0-83046f524052)


# Analysis and Results of Question 1

The box-and-whisker plot shows the distribution of average home sale amounts across towns. The Lower Whisker starts at $135,413, marking the boundary for the Lower Class. The Lower Hinge (Q1) is $230,620, setting the cutoff between Lower and Lower-Middle Class. The Median (Q2) is $285,470, showing the midpoint of the data. The Upper Hinge (Q3) at $386,607 marks the divide between Upper-Middle and Upper Class properties, while the Upper Whisker extends to $608,379. The data is right-skewed, meaning most towns fall in the middle ranges, with a few very high-priced towns pulling up the average.

This line graph shows the number of houses sold each year, separated by wealth class (Lower, Lower-Middle, Upper-Middle, and Upper Class), based on the quartiles determined from the box-and-whisker plot. Each line represents the total count of sales in that class, helping us see how economic conditions impacted home buying across different income levels. We also filtered to only show residential housing.

Over time, home buying across wealth classes in Conneticut has fluctuated significantly. The 2008 recession caused a noticeable dip in purchases across all price levels, though the decline was most noticeable in the Upper and Upper-Middle Classes. In the years that followed, especially around 2012, home sales gradually rebounded, with steady growth seen across all income levels. Notably, from 2018 to 2020, Upper and Upper-Middle Class home buying spiked, peaking in 2020, while Lower and Lower-Middle Class purchases saw only slight increases. After 2020, home sales dropped sharply in every class, particularly among Lower and Lower-Middle Class buyers—likely due to rising interest rates, economic uncertainty (Covid-19), and reduced inventory of affordable housing. Despite the downturn, Upper-Middle and Upper Class segments maintained relatively higher activity, suggesting continued market strength in higher price brackets.

The bottom bar chart shows that although Lower Class homes (those priced under $135,000) have the fewest sales, they consistently maintain the highest sales ratios. In 2019, the average sales ratio for this class reached 1.749, meaning these homes were selling for nearly 75% more than their assessed value. While the number of homes sold in this category decreased from 2019 to 2021, the sales ratio remained elevated, only dropping slightly during the pandemic years. This suggests that despite limited transaction numbers, buyer demand for affordable housing remained high. The high sales ratio in this segment is likely driven by the scarcity of homes available under $135,000, creating competitive bidding conditions. On the other hand, Upper and Upper-Middle Class homes experienced more sales but had lower sales ratios, often below 1, indicating weaker pricing power. This imbalance between availability and demand helps explain why Lower Class homes command relatively higher prices relative to their assessed value. The top line graph reflects this trend, where sales volumes in the Lower Class remain suppressed even during periods of broader market activity, yet the high sales ratios signal continued pressure in the affordable housing segment.



# Question 2 
How have year-over-year growth rates in median home sale prices varied across different neighborhoods from 2001 to 2022, and which neighborhoods experienced the most significant growth or decline following the 2008 financial crisis and the COVID-19 pandemic? 

![low](https://github.com/clairefriers/Project2/blob/main/low.png)
![mid](https://github.com/clairefriers/Project2/blob/main/middle.png)
![high](https://github.com/clairefriers/Project2/blob/main/high.png)

# Analysis and Results of Question 2
The three graphs of YoY growth rates from 2005 to 2011 provide clear differences in how towns of differing price tiers (low, middle, high) responded to the 2008 recession. High priced towns experienced way steeper and greater volatile declines in sale prices around 2008 compared to the others. Middle priced towns showed a medium amount of change, with smaller decreases during the crisis and steadier recovery patterns. Lower priced towns demonstrated greater resistence to the recession, with smaller negative growth rates during 2008 and generally more stable trends overall. After looking at these results, I have come to the conclusion that wealthier housing markets were more sensitive to the recession, while affordable markets exhibited more stability in the face of the crisis.

Some reasons that this could be the case include that the luxury (high price towns) housing market is much more elastic compared to others. This means that home buyers are much less likely to purchase a non basic housing need in a time of recession. Another potential reason is that wealthier homeowners have much more investments tied to the stock market, so when there is something like a recession there wealth is greatly effected. 




