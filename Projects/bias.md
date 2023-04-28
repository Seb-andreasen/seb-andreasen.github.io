## Limits of digital data for modelling population movements

**Project description:** 
Understanding how we move as individuals and as society is essential for crisis man­agement and understanding the spread of diseases. Analysing vast amounts of mobile phone network data is often the go to method, but the increase of mobile phone applica­tions tracking our movements might change this. Facebook is currently releasing highly aggregated data on population displacement and movements based on Facebook app usage to help researchers better understand the spread of COVID­19. I have investigated population and data collection biases in this data across 60 countries.

### 1. Data source

The data stems from [Data for Good](https://dataforgood.facebook.com/). I got access to more than 500 Gb data showing the amount of people moving in and out geographic areas at given times throughtout the day.

The maps are provided on the so called tile level, where the world is divided into a series of grids at different resolutions following the Bing Maps tile system. In short the world is divided in quad tiles, where the size depends on the chosen resolution. At level 1 the world is divided into 4<sup>1</sup> tiles, level 2 is 4<sup>2</sup>, level 3 is 4<sup>3</sup> and so forth. The maps are most often provided in tile level 10-16 depending on the country.

<img src="/images/Bias/urban_rural_nordjylland.png?raw=true"/>

### 2. The analysis

In this analysis I used the tile level maps to calculate the amount of people seen by Facebook in each tile and then use machine learning to understand the potential differences between countries.

The plot shows the fraction of a population seen in the Facebook maps. This is caluclated by finding the ratio between the actial population and the population shown in the Facebook maps. 

<img src="/images/Bias/coverage_country.png?raw=true"/>

In addition, we see quite large regional differences.

<img src="/images/Bias/coverage_region.png?raw=true"/>

The question is if we can explain these differences? 

I used a regression analysis to explain the differences and achieved a pearson correlation of 75%.

<img src="/images/Bias/ridge_results_scatter.png?raw=true"/>
 
The feature importance is explained using SHAP.

<img src="/images/Bias/ridge_shap.png?raw=true"/>

The above findings indicate population biases in the displacement maps as representa­tiveness differs by magnitudes per country and by socioeconomic status. 

### 3. Future work

Based on the findings I propose establishing a closer relation between re­searchers and Facebook to increase transparency in the data collection process and to mitigate biases.


