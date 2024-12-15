### Group members for this project: Rena Takahashi, LJ Friedman

This page is for a coding project done by Rena Takahashi and LJ Friedman for the purpose of exploring the relationship between finance and general happiness. Click [here](Final_Project_—_Happiness_Data.ipynb) to read through the code.
The following is the write-up for this code.

<br>

# Analysis

In this section, the group members will be referred to as “person 1” and “person 2” for the sake of simplicity.

## Introduction

Our data consists of a [List of Happiest Countries Rankings in 2024](https://worldpopulationreview.com/country-rankings/happiest-countries-in-the-world) and [Cost of Living Rankings by Country in 2024](https://worldpopulationreview.com/country-rankings/cost-of-living-by-country) from World Population Review; and the [Health Expenditure per Capita by Country in 2021](https://data.worldbank.org/indicator/SH.XPD.CHEX.PC.CD?locations=1W), the [Average Annual Precipitation by Country in 2021](https://data.worldbank.org/indicator/AG.LND.PRCP.MM?most_recent_value_desc=true), and the [Percentage of Land Dedicated for Agriculture in 2021](https://data.worldbank.org/indicator/AG.LND.AGRI.ZS?most_recent_value_desc=true&view=map) from World Bank Group. Using this data, we attempted to explore the relationship between finances and overall happiness. To answer this question, we divided finance into four categories – cost of living, healthcare expenditure per capita, annual precipitation, and percentage of land occupied for agriculture.

<br>

## Methods and Results

### Concerns and Issues

We faced several challenges when working on this project, namely the data collection. We initially intended to work with a Youth Risk Behavior Surveillance System (YRBSS), but it proved to be difficult when the download formats were not of the CSV format, and there were not enough data columns that would be useful for any analyses that we wanted to do.   
On the more technical side, Google Colab proved to be a hindrance when we tried to work on a shared Colab sheet because only one of us could upload the relevant CSVs to Colab (in other words, both of us uploading the CSVs would have resulted in a very messy Colab). In the end, person 1 had to do most of the analysis since if person 2 also tried to do it, person 1 would have to run the cells that person 2 also typed in for the functions to execute the way they were supposed to. This led to time-consuming and inefficient productivity so in the end, person 1 did the brunt of the coding process while person 2 worked on the analysis write-up.  
In addition, “overall happiness” is a rather arbitrary variable that is hard to quantify. So while the data used and the conclusions derived from it more or less make sense, the reproduction of the same analysis may slightly vary from person to person if they use a different data source for the same variable. Moreover, all of the data other than happiness scores and cost of living are from 2021, which may skew the accuracy of our results.


### Analysis

The first thing we did to analyze the data in regard to our variables was create choropleth maps for the entire world. It gave us insight into which of the category(ies) of finance may have the most impact on happiness.  
The visualization below (Fig 1\) constructs the rankings of the happiest countries in the world in the form of a choropleth map. While the map in itself can give us a brief idea about how “happy” people are in each country, it will be compared with other maps to interpret the potential factors that contribute to happiness.

  {% include_relative scattermap.html %}
Fig 1\. Choropleth map of the rankings of the happiest countries in the world. The lighter the color, the higher the happiness score. Data was taken from [Happiest Countries in the World 2024](https://worldpopulationreview.com/country-rankings/happiest-countries-in-the-world).

The second visualization (Fig 2\) displays the cost of living in 2024 around the world in a similar choropleth map. While not definite, comparing Fig 1 and Fig 2 tells us that it is possible that cost of living impacts the citizens’ happiness. The lower the cost of living, the happier the people are. For example, if we compare South America in both of the figures, the happiness score is relatively high and the cost of living is in the lower range. The visualization below Fig 2 (Fig 3\) shows a scatterplot between happiness scores and the cost of living. However, if we look at Fig 3, we can see that the general trend is an upward curve, i.e., the higher the happiness score, the more expensive the cost of living appears to be. This is reflected in Fig 1 and Fig 2 for North America and Australia. While the cost of living is on the expensive side, they seem to be two of the happiest regions in the world.

Fig 2\. Choropleth map of the cost of living in the world in 2024\. The redder the country, the more expensive the cost of living is in it. Data for the map was taken from [Cost of Living Rankings by Country in 2024](https://worldpopulationreview.com/country-rankings/cost-of-living-by-country).

Fig 3\. Scatterplot with happiness scores as the y-axis and the cost of living as the x-axis, where each dot represents a different country and each color a different quartile. Data for the happiness scores was taken from [Happiest Countries in the World 2024](https://worldpopulationreview.com/country-rankings/happiest-countries-in-the-world) and the cost of living was taken from [Cost of Living Rankings by Country in 2024](https://worldpopulationreview.com/country-rankings/cost-of-living-by-country).

In the fourth visualization (Fig 4), we see the choropleth map of health expenditure per capita in 2021 for the world. Below it, Fig 5 represents the scatterplot between health expenditure per capita and the happiness rankings. If we only compare Fig 2 and Fig 4, it makes sense that the countries with lower healthcare expenditure leads to a lower cost of living. However, if we factor in Fig 1 and Fig 5, it starts to raise questions. How does lower healthcare expenditure lead to higher happiness scores?  
Fig 4\. Choropleth map of health expenditure per capita in 2021\. The darker the color, the higher the expenditure for the country. Data for this map was taken from [Health Expenditure per Capita by Country](https://data.worldbank.org/indicator/SH.XPD.CHEX.PC.CD?locations=1W).

Fig 5\. Scatterplot with happiness scores as the y-axis and health expenditure per capita as the x-axis, where each dot represents a different country, and each color a different quartile. Data for the happiness scores was taken from [Happiest Countries in the World 2024](https://worldpopulationreview.com/country-rankings/happiest-countries-in-the-world) and the health expenditure was taken from [Health Expenditure per Capita by Country](https://data.worldbank.org/indicator/SH.XPD.CHEX.PC.CD?locations=1W).

We then have Fig 6, which displays the amount of annual precipitation in 2021 as a choropleth map. Below it is Fig 7, which is a scatterplot between annual precipitation and happiness scores. Fig 6 shows that most of the regions are on the lower range for the amount of precipitation received in 2021\. However, Fig 7 tells us that annual precipitation and happiness do not give us a general trend for their relationship. The dots are relatively scattered throughout the graph, with some countries having a low amount of precipitation with a happiness score of 4 but other countries having a happiness score of 5\. Hence, the results of these two visualizations make more sense when combined with the visualizations for the percentage of land occupied for agriculture.

Fig 6\. Choropleth map of amount of annual precipitation (in mm) in 2021\. The darker the color, the larger the amount of precipitation there was in the country. Data for this map was taken from [Average Annual Precipitation by Country in 2021](https://data.worldbank.org/indicator/AG.LND.PRCP.MM?most_recent_value_desc=true).

Fig 7\. Scatterplot with happiness scores as the x-axis and annual precipitation (mm) as the y-axis, where each dot represents a different country and each color a different color quartile. Data for the happiness scores was taken from [Happiest Countries in the World 2024](https://worldpopulationreview.com/country-rankings/happiest-countries-in-the-world) and the annual precipitation was taken from [Average Annual Precipitation by Country in 2021](https://data.worldbank.org/indicator/AG.LND.PRCP.MM?most_recent_value_desc=true).

	Finally, for the last pair of visualizations, we have Fig 8 with the choropleth map for the amount of land occupied for agriculture (in %), and Fig 9 with the scatterplot between happiness scores and land occupied. If we compare Fig 8 and Fig 9 with Fig 6 and Fig 7, we can observe that areas with higher annual precipitation such as South America tend to have more land occupied for agriculture. Although countries such as the Unites States and China’s annual precipitation was on the lower end of the spectrum, it makes sense that they have a large amount of land reserved for agriculture due to the culture of mass production. This leads to a higher cost of living, which is reflected in Fig 2\. The interesting here is that a large country like Canada is in the group with the least amount of agricultural land, even though it is high in the cost of living and health expenditure, as well as its happiness score.  
Fig 8\. Choropleth map for percentage of land occupied for agriculture (%) in each country in 2021\. The darker the color, the more land used in the respective country. Data for this map was taken from [Percentage of Land Dedicated for Agriculture in 2021](https://data.worldbank.org/indicator/AG.LND.AGRI.ZS?most_recent_value_desc=true&view=map).

Fig 9\. Scatterplot with happiness scores as the x-axis and percentage of land occupied for agriculture (%) in 2021 as the y-axis, where each dot represents a different country and each color a different quartile. Data for the happiness scores was taken from [Happiest Countries in the World 2024](https://worldpopulationreview.com/country-rankings/happiest-countries-in-the-world) and the percentage of land occupied for agriculture was taken from [Percentage of Land Dedicated for Agriculture in 2021](https://data.worldbank.org/indicator/AG.LND.AGRI.ZS?most_recent_value_desc=true&view=map).

### Conclusion

	Linking the observations from all of the visualizations, we come to the conclusion that finance has a significant impact on the happiness score of a country. The amount of agricultural land and annual precipitation have direct ties to the cost of living, which in turn affects the country’s happiness score. While we divided finance into four categories (cost of living, health expenditure, annual precipitation, and amount of agricultural land), it may be more helpful to consider health expenditure, annual precipitation, and amount of agricultural land as factors that impact the cost of living rather than the happiness score. This could possibly be the reason why these factors, especially annual precipitation and agricultural land, have very spread out scatterplots. In the future, if we analyze the relationship between these factors and the cost of living, we may see a tighter grouping of data points in our visualizations. Overall, the relationship between the cost of living and happiness was the clearest, with a higher cost of living corresponding to a higher happiness score. 

# Group Assessment

As much as I would like to say that it was 50% on both of our contributions, I think it is more accurate and honest to say that LJ had done 60% of the work and I have done 40%. The nature of our shared Colab sheet, as described in the introduction, made both of us trying to contribute to the coding be rather inefficient and nearly impossible. Although I have instead written up the entire analysis document from the beginning to the end, it was based on the coding that LJ had constructed. I believe that the initial coding takes more time and effort than the write-up for the analysis. Hence to why I say 60% LJ and 40% myself.
