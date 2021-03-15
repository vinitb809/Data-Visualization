# Data-Visualization

Abstract-

Olympics is one of the largest sporting events in which thousands of athletes participate in various sports with the participation of more than 200 nations. The Olympic Games take place every four years with Summer and winter games. In my analysis, I have explored the below questions.
1. How many medals won by the countries participated over the 120 years?	
2. What is the range of age for the winning individual medal in respective competitions, including the youngest and oldest age medal winner?	
3. What is the count of medals won by male and females over the years of time? 

Dataset-

•	The dataset used for visualisation is of Olympic Games including the games from the year 1896 to 2016. 
•	Dataset has been downloaded from www.kaggle.com and originally it is scrapped from www.sports-reference.com.
•	The Dataset includes the 271116 entries with different 15 attributes where each row corresponds to an individual participant competing in an individual Olympic event. Below are the attributes present in the Dataset. 	

      1.	ID - Unique number for each athlete
      2.	Name - Athlete's name
      3.	Sex - M or F
      4.	Age – Integer
      5.	Height - In centimetres
      6.	Weight - In kilograms
      7.	Team - Team name
      8.	NOC - National Olympic Committee 3-letter code
      9.	Games - Year and season
      10.	Year – Integer
      11.	Season - Summer or Winter
      12.	City - Host city
      13.	Sport – Sport
      14.	Event – Event
      15.	Medal - Gold, Silver, Bronze, or NA

2. Data Exploration, Processing, Cleaning and/or Integration - 

•	While preparing the dataset for graphs which includes “Medal” as one of the attributes first I had to remove the ‘NA’ values from the column as not all the participants won the medal.  Used ‘dropna’ method from the pandas library. 
•	Now the dataset has the only fields that have won medals. Then I must count the number of medals won by each country, so I counted and stored the result in another column using ‘groupby’ and ‘transform’ function.
•	Also, for the one of the graphs which has ‘Age‘ as one of the attributes in which age of some participants was not available. To remove this type of ‘NA’ I have entered the value for the ‘NA’ according to the previous entry of age using forward fill method from pandas.
•	As it is Olympics data over the 120 years. For visualisation, I tried to choose different types of attributes, According to NOIR (Stanley Stevens), I chose ‘Sports’ and ‘Gender’ as Nominal value, ‘Medal’ as Ordinal and ‘Age’ as Ratio.
 
Visualisation-
1.  Choropleth graph: 
•	A Choropleth graph is the most suitable option to visualise the total medal win counts for the countries over the 120 years in the Olympics. 
• Colour used to show medal counts is ‘Green’ with the colour scale, the lighter the shade the lower is the medal count whereas darker the shade higher is the count.
•	Country Borders are clearly kept as black to get highlighted and separate the regions. Also removed unnecessary lines such as coastlines and frame to keep the focus on the main part of the graphs.
•	Labels are placed to color scale and title of the graph to describe, which makes understanding easy.
•	Tools and libraries used: Jupyter Notebook, Pandas and Plotly.


2. Box and Whisker graph: 
•	A Box and Whisker Plot is perfectly suitable to show the range of ages of medal winners in different sports including the youngest and oldest medal winner’s age. 
•	Box and whisker plot found to be perfect for this scenario which includes minimum value as well as maximum values within the Quartiles. 
•	In this graph apart from age and sports I have considered other attributes too such as Name, Year and Medal (Gold/Silver/Bronze) 

-	In the graph for highlighting medals, I tried to give colour for each medal (Gold, Silver, Bronze) a relevant colour also kept the shape of the medal shape to the circle.
-	Used horizontal box plot for better understanding as there are many sports and cannot be seen properly in normally.
-	Both X and Y axis are labelled horizontally for better reading the sports content including graph chart heading.
-	Tools Used – Tableau


3.  The third choice of Graph is the part of the animation in tableau it demonstrates that how the difference of medals wins between males and females change over the period.            (Refer the video for more explanation)
*Note- In video part of this graph X-axis didn’t got captured but it is present as seen in below screenshot
•	Tool used: Tableau

 

Observations and Conclusions-
•	While exploring these questions I found out that in “Art competitions” and “Archery” have a wider age group for winning the medals. From age 17 to 73 and 14 to 68 respectively. The youngest participant who won a medal is 10 years old whereas the eldest participant is 73. 
•	The United States (US) has won the highest number of medals with a total of 5219. 
•	The difference between medals won by males and females get reduced over the period. 

Limitations
•	In choropleth graph, I wanted to add the classification of medals won by the different countries.
•	As the data set limited for the individual participation and sports, I could not visualise the sports which got participated with the teams.
•	In animation part, I wanted to include Country wise Male/Female medal winning count. It is not possible to plot this in 2D graph.

References-
1.	Dataset: 
https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results

2.	Plotly Library:
https://plot.ly/python/choropleth-maps/

3.	Data Visualisation checklist:
https://loop.dcu.ie/pluginfile.php/2986345/mod_resource/content/1/DataVizChecklist_May2016.pdf

4.	Examples those contributed in my work
https://www.kaggle.com/heesoo37/olympic-history-data-a-thorough-analysis

