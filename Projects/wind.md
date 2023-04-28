## Wind speeds

**Project description:** 
For the past 10 years or so I have chased wind and waves for kitesurfing and surfing. For some time, I have had this hypothesis that the distribution of wind speed has changed in Denmark. 

<img src="images/kite.png?raw=true"/>

### 1. Data source

I used the open data API from [DMI](https://www.dmi.dk/) to access a whole lot of weather data. The data contained observations from each day since 2011 from all weather stations across Denmark. 

I used SQL to access and analyse the data and python to visualise it. 

### 2. The analysis

For each day since 2011 I found the average wind speed and compared the distributions for each year using an ANOVA test. Spoiler alert, the distributions have not changed significantly. 

To visualize this, I have plotted the inverse cumulative probability distribution for each year, which essentially tells us the probability of observing a day with a specific (or higher) mean wind speed, and as it can be seen the distributions are quite similar. 
<br><br>

<img src="images/wind.png?raw=true"/>

<br><br>

### 3. Future work

The visualization provides a clear illustration of how the wind has not significantly changed over time. However, it would very interesting to to make the same test with more data from across the world. 


