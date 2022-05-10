# Analysing the air pollution levels of Barcelona during the COVID-19 pandemic lockdowns
*To visualize the article properly, open the [web version](https://dibuja.github.io/sdav-project/).*  
*Data & Jupyter Notebook can be found [here](https://github.com/dibuja/sdav-project/tree/main/data-and-notebook).*

The state of alarm established in Spain on the 14th of March of 2020 as a result of the COVID–19 Pandemic completely changed the life of everyone in the country. The economy got parallized and all the social relations and face-to-face interactions switched to a cold and electronic exchange of words through an artificial screen. During the  lockdown, the only real social life experience with human beings that didn’t belong to your home place would be the fast and nervous chat between the supermarket worker and maybe your neighbor while you were taking out your dog. And all of that with a double face mask covering half of your face and the constant panic of being too exposed.  

This life-changing situation also brought strict mobility restrictions where citizens were obliged to study and work from home. This exceptionality became routine and that really affected a southern tourist city like Barcelona, where going out everyday to work, study, do leisure activities and meet friends was the most common pattern.  

While domestic activity increased, the mobility on the streets faded away. Just a few cars would drive through the streets and the thousands of motorbikes that were constantly going around were all parked.  

Some days after the first lockdown something happened. From the top of Collserola, one of the highest points in Barcelona, a surprisingly clear view of the whole city appeared. There was no fog, smoke or smog. The low transit activity allowed the city to clean itself leaving a fantastic view that was not often possible to see. And that, people realized, was the first positive effect the pandemic had given to us. Things were brighter and colorful. After some weeks people were even saying that they could hear the birds singing louder, and the trees growing greener.  

We have studied the NO2 emissions in Barcelona between 2019 – 2022 to analyze how the restrictions imposed during the state of alarm changed the levels of pollution in Barcelona, comparing it to other relevant factors such as wind or precipitation, and try to discover the most influential restrictions.

### Background

Different rules were implemented during the COVID-19 pandemic lockdown in the city of Barcelona. These rules severely limited the mobility of people throughout the city, clearly reducing the emissions caused due to road transport [^1]. We wanted to know how these emissions impacted the air pollution of the city so we decided to describe and analyse the general behaviour of NO2 concentration levels on normal days and try to understand the data. That could give us a sense of how a standard day in the sunny city of Barcelona was in levels of pollution.

Additionally to the restrictions that caused a decrease in the generation of air pollutants, we know that meteorological and topographic conditions highly influence the air pollution levels observed in the city since they determine the habits of the population (e.g. taking the car instead of the bike because it is raining) and the transport, chemical transformation and deposition of air pollutants [^2].

We are aware that during this analysis we are working with causal elements –wind speeds, precipitation, lockdown rules– and the effect –NO2 concentration levels– of the consequences of such elements: decreased mobility. A more rigorous analysis would contain data on mobility, however that data was not possible to find by the authors. Having said that, let’s get to it!

### NO2 Concentration

We are measuring NO2 concentration levels in the air thanks to 7 measuring stations placed throughout the city, as can be seen in the following map.  

<embed type="text/html" src="./plots/stations.html" height="450" width="840">

The stations in Eixample and Gràcia correspond to traffic stations and the rest are background stations. This means that the traffic stations measure NO2 concentration next to big roads while the others are in residential areas. Both types of stations present the same patterns but with slightly higher or lower values, due to their proximity to large roads.  

**NO2 concentration levels in Barcelona are a public health problem**. High NO2 concentration levels are responsible for the acid rain that pollutes the environment as well as for health effects on the population, such as increased asthma cases, increased inflammation in the airways, reduced lung function, and other respiratory conditions [^3]. The United Nations as well as the European Union have both established limits to how much NO2 concentration can be in the air. How did Barcelona fulfill these limits between 2019 – 2020? You can see it in the following graph.
  
  
<embed type="text/html" src="./plots/yearly_average.html" height="450" width="840">
  
During the last years, the yearly average of NO2 concentration levels stayed under the acceptable limit established by the European Union (40 μg/m3) for all the stations besides 43, which is a traffic station. However, if we take into account the guideline of the World Health Organisation (10 μg/m3)[^4], we can see that Barcelona does not comply with such standards on any of the stations.
  
### Weekly evolution of NO2 concentrations  

Let’s first understand the trend in pollution levels by hour and day of the week. For that, we have made a plot that contains the average global NO2 concentration at levels every hour of the week. We have also added the same measure but for the months in which the first and third states of alarm were enforced.

<embed type="text/html" src="./plots/weekly_average.html" height="450" width="840">

We can observe that during normal conditions there are two peaks of NO2 concentration during the day, the biggest one around 09:00 and another one around 20:00, which aligns with the time in which people tend to drive to work and back [^5]. It is also evident how, during the weekends, the trend in NO2 concentration completely changes: the peaks of pollution happen around 20:00 instead of in the mornings due to the changes in the mobility of people.  

The second line shows the same values during the first state of alarm. During these days, the peak remained around 09:00, while the trend changed significantly. Overall, we can see an evident decrease in concentrations, going from a range between 13–47 μg/m3 to 6–33 μg/m3.  

During the third state of alarm we can also observe a decrease in NO2 concentrations with respect to normal mobility conditions, but not as big as during the first state of alarm. The trend remains similar while the range of measurements becomes 7–41 μg/m3.  



### Restrictions during the pandemic

The pandemic restrictions seem like a thing in the past that, hopefully, is fading out from our memories, so let’s remember the most impactful restrictions that were put in place as well as their time periods.

<embed type="text/html" src="./plots/rules.html" height="450" width="840">

We have compiled the most impactful restrictions in terms of mobility:

- First state of alarm excluding relaxation periods: during the first state of alarm mobility was only allowed for basic services and working. Remote work was deemed mandatory when possible. Although the emergency state finished on June 21, only the dates until the beginning of relaxation of restrictions are included since the rules start changing after.
- All schools closed: during this period, all schools, highschools, universities were closed and only worked remotely.
- Total lockdown: All activity in the country besides essential work (supermarket, road cargo, healthcare, etc.) was paralized during two weeks.
- Relaxing phases 1, 2 and 3: After May 25, Barcelona started relaxing the restrictions in a scheme with different phases that implied different levels of mobility.
- Third state of alarm: A new state of alarm was put in place. Remote work was “recommended”. All leisure activities closed and a night curfew from 22:00 to 06:00 was imposed.
- Night curfew from 01:00 to 06:00: New night curfew imposed for a small period of time.

Some of the restrictions, such as the total lockdown that prohibited all individuals to go out of their homes besides to do essential work, was enforced for a relatively small period of time (2 weeks) while other restrictions such as the first emergency state lasted for a few months. We will compare these restrictions with the changes in NO2 concentration levels to try to find the correlation between them. The following graph shows the entire period of time analysed and gives the possibility to zoom-in, select specific stations, and observe specific data points.

<embed type="text/html" src="./plots/full-time-series.html" height="450" width="840">

While the first state of alarm seems to have had a high impact on the NO2 concentration levels if we take into account the previous visualization, it is not evident that the third state of alarm had the same impact. That can be explained by the fact that the third state of alarm limited mobility to a smaller extent, with recommended remote work, and closing of leisure activities but with the possibility to move freely (excluding curfews).  

We have therefore tried to understand and model the impact that each of the collected features had in the evolution of NO2 concentration levels. In order to do that we have collected data on meteorological conditions in the city of Barcelona, specifically maximum wind speed at 10m of height and total precipitation in 24h. We have created a correlation plot, which shows how similar the trends are for each couple of variables. Zero means no correlation, while 1 or -1 mean total correlation.  

<embed type="text/html" src="./plots/correlation.html" height="450" width="840">

As shown in the previous plot, the variables that are most correlated with the NO2 concentration are the wind at 10m height (- 0.48!), the variable related to the first emergency state and the variable connected to the closure of schools.  

In order to further down on our analysis of impacts, we have modelled a ML learning algorithm (Random Forest) to try to infer the levels of NO2 concentration at a certain time. Although we have not managed to make a model that has a high level of accuracy (R2 ≈ 0.3) we believe that the interpretation of the feature importance that the model presents can be representative of the influence created by the different lockdown restrictions. In other words, we think that the importance that our model gave to each variable can be a limited picture of the importance that each variable actually had for influencing the NO2 concentration levels. In the future plot a ranking of the importance of each variable is shown.

![](/plots/shap.png)

According to the previous plot, in order to infer the measured NO2 concentration levels, the most important variable is, as expected, the wind, followed by the variable corresponding to the third state of alarm and the first state of alarm. The variables corresponding to total lockdown, etc. did not seem to play a big influence in the model.  

### Conclusions & limitations
  
During this analysis we have understood the NO2 concentration trends as well as how these numbers have changed during the period of restrictions that occurred between 2020 and 2022 as a consequence of the pandemic. We could see how the NO2 concentration levels decreased heavily during the first state of alarm and not so much during the third state of alarm.  

Additionally, we could see that, even though the specific rules in place and the meteorological conditions influence the levels of NO2 concentration, they are clearly not enough to explain the specific levels at each time. Other variables, such as data on mobility, are essential to be able to make a model with a higher accuracy and therefore fully explain the impact of each restriction.  

We can conclude that the reduction in mobility caused a decrease in pollution levels that gave Barcelona the best air quality in years. Perhaps it is time to rethink the way mobility works in the city, to reduce the impact on the environment and public health.

------------

[^1]: [Air Quality in Europe 2020 Report, European Environmental Agency](https://www.eea.europa.eu/publications/air-quality-in-europe-2020-report)
[^2]: [Air Quality Status Briefing 2021, European Environmental Agency](https://www.eea.europa.eu/publications/air-quality-in-europe-2021/air-quality-status-briefing-2021)
[^3]: [Nitrogen Dioxide, American Lung Association](https://www.lung.org/clean-air/outdoors/what-makes-air-unhealthy/nitrogen-dioxide)
[^4]: [Analysis of air pollution in Barcelona, Eldiario.es (spanish)](https://www.eldiario.es/catalunya/barcelona/radiografia-contaminacion-barcelona-infringiendo-ue_1_1186806.html)
[^5]: [Ambient Air Pollution, World Health Organisation](https://www.who.int/news-room/fact-sheets/detail/ambient-(outdoor)-air-quality-and-health)
