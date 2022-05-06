# Analysing the air pollution levels of Barcelona during the COVID-19 pandemic lockdowns
``To visualize the article properly, open the [web version](https://dibuja.github.io/sdav-project/)``

### Intro goes here
### Analysis goes here:

Different rules were implemented during the COVID-19 pandemic lockdown in the city of Barcelona. These rules severely limited the mobility of people throughout the city, clearly reducing the emissions caused due to road transport[^1]. We want to know how their impact was on the air pollution of the city.

For that we will describe and analyse the general behaviour of NO2 concentration levels on normal days and try to understand the data before moving on to finding correlations between the different variables.  

Additionally to the restrictions that caused a decrease in the generation of air pollutants, we know that meteorological and topographic conditions highly influence the air pollution levels observed in the city since they determine the transport, chemical transformation and deposition of air pollutants$^1$. We have decided to take into account specifically wind speeds and precipitations for this project.  


#### Weekly evolution of NO2 concentrations  

We started this analysis by understanding the trend in pollution levels by hour and day of the week in order to understand the patterns of NO2 concentration.

In order to analyse the pattern in NO2 pollution during a day, we are plotting the hourly pollution levels on 15th - 21st of April, 2019. In the dataset we have two types of measuring stations: traffic & background stations. Both types of stations present the same patterns but with slightly higher or lower values, due to their proximity to large roads.

``——— Map of where the stations are.``

![Weekly plot](/plots/weekly.png)

In the previous graph we can observe the peaks in NO2 concentration levels happening in the mornings of the working days during that week (friday was a holiday). Additionally, smaller peaks emerge during the afternoons of working days and the overall concentration levels decrease during weekends. These results go hand-in-hand with the mobility patterns of the population since the pollution levels are in their majority influenced by the road traffic.

#### COVID-19 Restrictions

We have also built a dataframe containing the most important restrictions implemented in terms of mobility and their duration. A horizontal barchart with the periods of entry into force of each restriction is shown below.

<embed type="text/html" src="./plots/rules.html" height="450" width="840">

Some of the restrictions, such as the total lockdown that prohibited for all individuals to go out of their homes besides to do essential work or tasks, lasted for very small periods of time. Other restrictions like the first emergency state lasted for a few months. We will compare these restrictions with the changes in NO2 concentration levels to try to find the correlation between them.

#### Full Time Series

<embed type="text/html" src="./plots/2020.html" height="450" width="840">

While the first emergency state seems to have had a high impact on the NO2 concentration levels if we only take into account the previous visualization, it is not evident that the third emergency state had the same impact. It is easy to understand why: the third emergency state only limited mobility in a small extent, with recommended remote work and possibility to go out freely to work and to do leisure activities.  

However, we cannot state that the values of NO2 concentration were not affected by it, to be able to do that we must remove the effects caused by meteorological causes.





(Analysis)

[^1]: Footnote 1.

