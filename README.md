# Does Green (Wealth) mean Green (Environment)?


## Project 1 - Team 15:

**Amir Ahanchian** - Scrum Master, Visualizations**

**Arzan Malegamwalla** - Visualizations and PowerPoint**

**Duy Duc Nguyen** - Cleaning Lead**

**Terry Schoch** - Data Set, API Retrieval and Cleaning Sub**

**Instructor:** Sunil



## Project Objective

    - To understand what true development means. 
    - Create Awareness - Equal distribution of responsibility to protect our planet 
    - To analyse the correlation (if any) between economical prosperity with environmental sustainability. 

*Is progress as a nation in terms of wealth and quality of life begetting a better world truly? Or does it come at a price we'd rather not admit or face? And if so, does it have to be mutually exclusive and who are the leaders in creating a better world with more than just their **own** betterment in mind.*


## Major Questions


**Does a wealthier/more developed nation mean it is 'greener' too?**

    1. Do developed countries recycle more than other developing countries?
        - Does GDP play a part ? 
    2. Do developed countries have a bigger carbon footprint? 
    3. Does a country’s GDP relate to its clean energy generation?


## Datasource and API

https://www.kaggle.com/datasets/lucafrance/the-world-factbook-by-cia

**The WorldFactbook:** an in depth data repository compiled and published for free use by the CIA.

>The World Factbook provides basic intelligence on the history, people, government, economy, energy, geography, environment, communications, transportation, military, terrorism, and transnational issues for 266 world entities. - cia.gov/the-world-factbook/


Our Data Analysis assignments were first divied up and broken down into a multi-step process.

1. Identify a datasource and locate an API version that allowed for search queries.
2. Apply various functions and techniques to properly clean the raw scraped data retrieved via the api requests.
3. Shape this newly cleaned data into effective visualizations in the form of charts and graphs to reveal a story.
4. Combine documentation and output of the first three steps into a team driven power point presentation.


## Visualizations

### Waste Generated per Country Type
![Waste Generated per Country Type](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%209%20Average%20Waste%20Generated%20per%20Country%20Type.png)


### Waste Recycled per Country Type
![Waste Recycled per Country Type](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%2010%20Average%20Waste%20Recycled%20per%20Country%20Type.png)


### Real GDP Per Capita 2020 vs Percent of Waste Recycled Annually
![GDP Per Capita vs Waste Recycled Annually](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%203%20Real%20GDP%20Per%20Capita%202020%20vs%20%25%20of%20Wasted%20Recycled%20Annually.png)

To initially determine a correlation between a country's wealth and it's commitment to a cleaner environment, we broke our cleaned data down into two pie charts showing the share of waste generated and waste recycled per *country type* *. This was achieved through a GroupBy function using country type as the grouping variable.

* The *country type*s being referenced are per the metrics used by the United Nations: 
- a) developed nations
- b) developing and 
- c) least developed countries (LCD) 

*While there are several variables that the UN uses to define these categories, GDP per Capita is indeed the main proponent. 

The charts revealed that although the waste generated on average in the developed world is a higher proportion than other parts of the world, their share of recycling is also drastically higher and suggests that higher GDP nations are indeed doing their part in at least cleaning up their own mess.

Linear regression backed up our theory and hope. While the correlation is considered "weak" with an r squared value of .32, it is definitely there. Moreover, our pearson correlation (0.56552) and p value (5.90404e-10) further backed up the relationship between a higher GDP and a better recycling infrastructure and effectively eliminted the null hypothesis on this metric.


### Air Pollutants vs GDP
![C02 Emissions per Country](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/map%20of%20countries%20and%20co2%20emission.png)

The following Map Plot references each country's c02 emissions by megaton which is depicted relationally  to the size of the circles (bigger = more). This method rather effectively shows the disproportionate affect some of the most advanced nations truly have toward total pollution. 


### Real GDP Per Capita 2020 vs Particulate Matter Emissions ug-m3)
![GDP Per Capita vs Particulate Matter Emissions](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%202%20Real%20GDP%20Per%20Capita%20vs%20Particulate%20Matter%20Emissions%20(ug-m3).png)

A scatter plot with a linear regression overlayed illustrates that there is actually a negative correlation between a nation's higher per capita GDP and a lower output of particulate matter emissions. While this would suggest that a more developed nation does pollute less in this regard, the correlation is very weak and frankly: hardly an endorsement of wealth leading to cleanliness or vice versa. Specifically, it must be noted that some of the biggest outliers on this chart happened to qualify well within the Developed nation benchmark of $27,000 GDP per Capita. The most egregious of these being the United States nestled well into the upper right of the chart. As seen below, the results were similar in regard to C02 emissions, but instead a very slight positive correlation presents itself further muddying the theory that wealth begets responsible management of the environment.

![GDP Per Capita vs C02 Emissions](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%201%20Real%20GDP%20Per%20Capita%202020%20vs%20CO2%20Emissions.png)


### Clean Energy per Country Type
![Average of Energy Produced Cleanly per Country Type](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%2011%20Average%20of%20Energy%20Produced%20Cleanly%20per%20Country%20Type.png)

What then are the rich countries doing to combat climate change at one of the root causes of the problem: power generation. Interestingly, this pie chart reveals that regardless of the developmental status of a country, the percent of energy produced through renewable means (such as wind, solar, hyroelectric, etc.) is pretty much equal across the board. 


### Real GDP Per Capita 2020 vs Electricity by Clean Energy (%)
![GDP Per Capita vs Electricity by Clean Energy](https://github.com/terryschoch/project-1-green-wealth/blob/main/Coding/output_data/Fig%204%20Real%20GDP%20Per%20Capita%202020%20vs%20Electricity%20by%20Clean%20Energy%20(%25).png)

Again, a scatter plot was used to dig deeper and verify any correlation present. And again, it was shown that despite being more advanced in several metrics, the developed nations and their greater GDP per capita did not correlate much at all to having cleaner energy production methods. 




## Conclusion

Ultimately, the final revelations borne from this project left us feeling unsatisfied. While the waste generated and waste recycled pie charts and correlation showed optimistically that wealthier countries do a far better job of cleaning up their own mess, they also have far larger messes to clean. The further we dug and the more visualizations we created, the further we ended up chipping away at this early hope for the leading countries to be leaders of the environment as well. 

A more serious issue also lay in the consistency and veracy of the information retrieved. While the CIA is itself an incredibly reputable organization, specifically when it comes to their skill in data retrieval, the full explanation and annotation of their sources and the trustworthiness of the numbers provided due to know fault of the CIA itself was a nagging question that would not go away. While having such a high rate of waste recycled seems excellent on the surface, what does that actually mean? Is that waste recycled within the country exclusively, or does that include several far looser definitions of "recycling" or dubious agreements where the wealthier nations take advantage of the more desperate by offloading their garbage upon them and calling it a day? If there is any merit in that question, it becomes a matter of sssentially brushing their problem under their neighbour's rug. And given that developing nations often tend to lag drastically far behind in terms of regulations, infrastructure to uphold what regulations do exist, and sometimes even basic resources to provide accurate information, how much of the real data lies hidden between the lines? 

Basically, it boiled down to a sense that the wealthiest nations are certainly acting responsibly in the framework of the world's expectations as they currently are and always have been in terms of the climate crisis and how seriously it has been taken historically to this point. But in terms of actually taking meaningful steps forward toward a shift in the greater expectations and ensuring not only a cleaner but literally brighter future, the evidence is simply not there and at times counter to the hope that it would be. The words of progress spoken ring fairly hollow when considering the actions taken. 

Ultimately, the real answer to our questions is, like the environmental situation itself, quite messy and there is, as of yet, no function to make the world truly clean.