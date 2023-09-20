# Final-Project-Tableau

## Project/Goals

#### Chosen Project: Option 2 --> V) Causes of Death - Our World In Data

My goal is to use the Causes of Death database, along with a few other sources in order to gain some insight and answer the following questions:
1. Does gdp (a measure of economic "health") of a country/region play a role in the number of deaths observed and mortality rate in that country/region?  I hypothesize that the higher the gdp, the lower the mortality rate.
2. Are there any outlier regions or countries that break this hypothesis?
3. What are the most common causes of death in countries that have a higher gdp and in those that have a lower gdp.  Are there reasons for this?
4. Determine what the fastest growing causes of death are in particular countries - mainly North American countries (which have the highest regional GDP in the world).

## Process

### 1. Collect and Reshape the necessary data

#### Causes of Death.csv
- The Causes of Death database happened to have a "cleaned" version available.  This table gives the death counts for each country for each year from 1990 - 2019 for the 33 unique cuases of death.

#### Population.csv
- In order to calculate mortality rate instead of simply using the number of deaths per year, I needed to find information on the population of each country for this date range. The reality is that, while the number of deaths is a valuable piece of data, it can be misleading as it doesn't consider the increase in population.  Mortality rate, on the other hand, considers both the number of deaths and the population.

#### Gdp.csv
- I also pulled in information for GDP for each country in this same date range.

#### Regions.csv
- Lastly, I pulled information that groups countries by region.

#### Reshaping:
- I had to reshape the Population and gdp tables to mimic the structure of the Causes of Death table.  This helps Tableau to be able to more easily connect the tables together.  I performed this task within Tableau by selecting all of the "year" columns and pivoting them to become rows instead.

### 2. Created Calculated Fields and Parameters
In order to gain the insights I am looking for, I needed to calculate some new fields and a parameter to use in my dashboards. Particularly:
- Mortality Rate (%)
- Total Deaths for varying years (LOD Calculation)
- YoY Change in Number of Deaths (%)
- Percent Change in number of deaths (for a date range specified by the user)
- Top N parameter

### 3. Created Informational Visuals that I believed would answer my questions
Some of the Visuals created for the 3 dashboards constructed for this project are:
- Mortality vs. Gdp for various regions around the globe - Truth be told, I really wanted to create a visual that was similar to the one presented by Hans Rosling on a Ted talk called "The Best Stats You've Ever Seen".
- Maps with colouring to indicate mortality rates - so we can quickly identify the regions that are "hot spots" for any particular causes of death
- Graphs using time (years) as an horizontal axis to see the change of mortality rate, number of deaths, YoY change, and gdp.  These can be particurly powerful when combining more than one of these to compare.
- Forcasting of Mortality Rates for the next 4 years
- Top N Bar Charts to indicate top causes of death per country/region


### 4. Answered And Refined Questions as I went along
As my dashboards were being constructed, I would have some of my answers reveal themselves quickly, but new ideas and questions would emerge.  Sometimes an anomoly in the data cuased me to create a new sheet/visual to pull on a new thread.  I actually found that my curiosity was increasing the more I played with the data, but at some point I had to realize that there are too many threads and leads to follow, so I had to narrow my scope of question down to what it's become above.


## Results
**I chose Option 2 --> V) Causes of Death - Our World In Data**

### Dashboard 1: "Mo Money Less Problems?" The Hans Rosling Visual
This visual is a bubble chart that is packed with information.  First of all, it's a graph that compares the GDP and the Mortality rate of every country.  Every bubble on the chart represents a country and the size of the bubbles represents the varying populations of those countries.  The colour of the country indicates which region of the world that country is in.  As the years are changed, these bubbles move in a fascinating "dance" as we observe the average GDP of countries increases over time and the average mortality rate decreasing over time.  Like a school of fish, these unique countries dart around the grid in it's own unique path, while the overall cluster moves together as a whole.

#### Key Take-aways
At first glance, my first question was answered.  "Does gdp (a measure of economic "health") of a country/region play a role in the number of deaths observed and mortality rate in that country/region?" - Yes!  When can clearly see the as the overall global GDP increases, the global mortality rate decreases.

BUT!  That's just the average GDP and mortality rate.  While this is a fascinating discovery, I can't help to wonder if any countries do not abide by this discovery.  I mean, if an increase in GDP means that mortality rate decreases, then with a high enough GDP, can people just live forever?  Certainly not.  Some countries or regions must not be experiencing this trend.  And if not, why?

The dynamic bubble chart is a great "big picture" tool, but we need to drill down into specific countries and regions to get a better sense of which countries might violate this observed trend.

### Dashboard 2: Regional Mortality Dashboard
This visual is intended to zoom in a little closer to mortality rates and GDP for specific Regions.  This includes a direct comparison between the timeline trend of the GDP and the mortality rate over the years.  In order to find the regions that do not fit this initial observation, I needed to find a chart where GDP is increasing and mortality rate is also increasing.

It turns out that regions who have had a higher overall GDP throughout the years (North America, Europe, Central Asia) happen to have a increasing GDP, but also an increasing mortality rate.  Whereas the regions that are not as "developed" and have lower GDPs do experience a drop in mortality rate.  I believe that as these developing regions have more improved economies, the health care systems and access to those systems improve.  However, what is happening with these more developed countries?  With higher GDPs and likely higher average incomes, what kinds of causes of death plague these countries that don't necessarily plague the others?

In order to answer these questions, I needed to focus in on the specific causes of death for each country.

### Dashbaord 3: Top Causes and Emerging Causes
This dashbord focuses in on the top N causes of death for specific countries and for a specific range of time.  It not only shows the top causes of death, it also breaks down the number of deaths per year, as well as the year over year change.  It includes a visual of the ratio of deaths for each of the top N causes in order to identify how each cause compares to the others in the context of total deaths.  Likely one of the most important pieces of information this dashboard contains is the Percent Change in deaths.  This may seem like a simple thing, but this allows us to pinpoint which causes of death are on the rise. In other words, there may be causes of death that claim the most lives year over year, but they may not be the fastest growing causes of death.  

With this dashboard and information, we can finally get some insight into the countries that didn't fit our initial hypothesis.  We see that in countries with higher GDPs, we have problems like Cardiovascular Disease and Neoplasms (Cancers).  With more money, we tend to buy and consume different (more rich, fatty, sugary) foods and with larger distances to travel and easy access to transportation, we don't move around as much - we are less active.  These top causes are likely a reflection of that lifestyle.  The reality is that these causes of death are also on the top N list of many countries, even ones with lower GDPs, but they are not as pervasive, and in many cases, they are far from the top two.  Some issues that plague some lesser gdp countries are HIV/Aids, Diarrheal Diseases, Malaria, Tuberculosis, and Neonatal Disorders, to name a few.  This is not true of all of them, but certainly too many of them.  This is sad because these are some things that wouldn't even show up on the list with improved and more accessible health care.

Likely one of the most interesting findings is the fastest growing causes of death in come countries.  The fastest growing cause of death in North America is drug use.  Drug use and overdoses has increased by nearly 1000% in the last 30 years!!  While the number of deaths is nowhere near the that of Cardiovascular disease and neoplasms, the rate of change of drug-use related deaths is absolutely staggering.  I'd love to know what is causing this ... are we bored?  Are we depressed?  What are we escaping from?  

No time to answer these now, but maybe next time! 

## Challenges 
1. Coming up with my initial questions - solved by simply playing with the data for a while.
2. Connecting the sheets with common filters in order for them to work correctly with eachother on the dashboard.  
3. Using LOD calculations - still a little shaky on these.
4. Knowing where the balance between not enough and too much detail on a single dashboard.
5. How to structure a dashboard - I feel like I still have alot to learn here.
6. Knowing when to stop.  The curiosity is endless and the more threads I pulled on, the more questions emerged.


## Future Goals
1. I would explore more into the emerging causes of death for certian countries.  Then try and find out why these are the fastest growing causes.
2. I'd clean up my dashboards a little more.
3. Try different types of visuals that I didn't get around to trying.

