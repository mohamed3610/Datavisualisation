# Datavisualisation
# The datasets used

We used the datasets athlete_events and noc_regions.
The athlete dataset has all the information about the olympics except their regions {ID, Name, Sex, Age, Height, Weight, Team, NOC, Games, Year, Season, City, Sport, Event, Medal}


The noc_regions has only the participants regions so we had to merge between both of them.

medals_df.It represents number of medals a team got.We merged our data and medals_df on region and Team/NOC.



# Our motivation:

Visualize the data and study how the performance is affected by varies factors. For example player's characteristics that increase performance in different sports.
Moreover,we tested if the country is hosting the olympics,would the performance increase? And if a team won a gold medal, does this affects the performance positively later on?

# Questions:


1) Does being the host improve the performance?
2) Is there characteristics that improve the chances of winning a medal?
3) Does the performance of a region improve after recieving their first Gold medal?


# Cleaning the data

1) We added the 2 datasets and merged them.
2) We dropped duplicates from the merged dataset.
3) We calculated the null_values_percentages for every column.
4) We divided the data into males and females and grouped them by region and sports then we calculated the mean of females' height and weight and males' height and weight .
5) We started dealing with outliers in height and weight,First, we dropped all rows with sports not having any weight or height ,second, we visualized the outliers on 4 boxplots "female height","male height",
"female weight","male weight",third we calculated the IQR and removed all the outliers in all the plots.
6) We added the null values of weight and height to new dataframes males and females and filled them with the means we calculated before to get the index of null to fill in the null values from the dataset to the mean (with respect to the region, sex, and sport). 
7) We concatenated the 2 frames males and females into 1 dataframe and calculated the null_values_percentages for every column again.


# To visualize data after cleaning:

1) We plotted a graph to show the participants' age.
2) We plotted a graph to show variation of Age for Male Athletes over time.
3) We plotted a graph to show variation of Age for Female Athletes over time.
4) We plotted a graph to show Height and Weight Variation between males and females.
5) We plotted a graph to show total Medals by Country
6) We plotted a graph to show Gender Distribution
7) We plotted a graph to show Variation of Female Athletes over time.
8) We plotted a graph to show Variation of Sports for Males over time.
9) We plotted a graph to show Variation of Sports for Females over time.


# Steps:

# 1) Does being the host improve the performance?

1) make a new column called Host_Country where it has the hosting country of each record

2) By applying the method host_country it takes the city the Olympics was hosted in and assigns the host country

3) In a new dataframe medals_hosting_or_not we get the number of Gold - Bronze - Silver - Total Medals for each year for each region and also having the host coutry at that year

4) Adds a new feature where Is_host is added to each record

5) show countries and number of medals they have won using: .head() function

6) visualize top 10 countries and average of medals they have won using: scatter plot

7) visualize total medals per years for hosting and non hosting countries using: scatter plot

8) comparing means when hosting and not hosting using: area graph

9) We added a new column to calculate the total medals for each country in each year, then we sorted it ascendingly in a new dataframe.

10) We plotted 3 graphs to prove how the countries' performance is affected due to their hosting.


# 2) Is there characteristics that improve the chances of winning a medal?

1) We plotted a graph to show the difference between males and females performance in Weightlifting with respect also to their weights.
2) We plotted a graph to show the relationship between performance and height in the Basketball sport.
3) We plotted a graph to show the relationship between performance and age in the Gymnastics sport and in all sports.
4) We plotted a graph to show Women medals per edition of the Games.
5) We plotted a graph to show men medals per edition of the Games.
6) We plotted a pie chart, 2 scatter plots to show the relationship between performance and season.

*   comparing number of females and males winning bronze, silver and gold medals using: 
violinplot
*   Games characteristics
    *   in Weightlifting game, determine weight and height characteristics to win medals among males and females using:
        violinplot
    *   in Basketball game, determine height characteristics to win medals using:
        pointplot
    *   in Gymnastics game, determine age characteristics to win medals among males and females using:
         scatterplot
*   Some characteristics
  *   determine age characteristics for athletic participants using:
        Bar chart
  *   determine age characteristics to win medals using:
        violinplot
  *   determine reogon characteristics to win medals using:
       Bar chart
  *   determine variation of females and males Athletes over time using: linear graphs
  *   determine variation of Sports for femlaes and males participants over time using: linear praphs
    *   determine variation of femlaes and males to win medals per edition of the Game: Bar chart
  *   determine season characteristics to win medals using:  Python turtle and scatterplot





# 3) Does the performance of a region improve after recieving their first Gold medal?

1) We get all rows in the cleaned data that had a gold medal
2) We then sort them by the year and groupby the region
3) We then get the first occurance of the gold medal in the history of the region
4) We then plot the total number of medals before receiving the first gold medal and then after 
5) Get the number of medals before receiving the first gold medal: lineplot
6) Get the number of medals after receiving the first gold medal: lineplot
7) determine number of medals won by Japan - Egypt - Armenia before and after winning gold medal using: lineplot



# Conclusions 
1) When we asked the first question (Does being the host improve the performance?) and by comparing the performance when the region is the host or not it was really obvious that being a host was a great advantage to the region

example:


![image](https://user-images.githubusercontent.com/85845088/147889670-9328b9a0-6574-41f4-9816-385810bc2f29.png)


2) When we asked the secomd question (Is there characteristics that improve the chances of winning a medal?) and after reviewing the correlation between some characteristics and winning medals (for example relation between weight and weightlifting w.r.t the Sex) we found out that there are some characteristics that increases the chance of winning and award

example:


![image](https://user-images.githubusercontent.com/85845088/147889549-23dbc48c-b859-46e3-8ec4-85cab4e2fc61.png)




3) When  we asked the third question (Does the performance of a region improve after recieving their first Gold medal?) We compared the data before receiving the regions' first gold medal and after and surprisingly we found that the performance decreases after winning the first gold medal 

example (Egypt's performance after receiving their first gold medal):


![image](https://user-images.githubusercontent.com/82681541/145730466-2ec49b71-25cb-412d-b82c-f7f2fb938cbe.png)
