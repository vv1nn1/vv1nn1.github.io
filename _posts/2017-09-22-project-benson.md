---
layout: post
title:  Project Benson - Hacking the MTA
date:   2017-09-22
excerpt: “Exploratory data analysis on MTA turnstile data”
project: true
tag: 
- project
- recommendation
- exploratory data analysis

comments: false
---
 
      
## Project Description
WomenTechWomenYes (WTWY), a fictional charity, hosts an annual gala in NYC at the beginning of the summer each year. The organizers want to put street team at the entrances of subway stations to collect emails and send out free gala tickets as an effort to build awareness and reach. The main task of this project is to utilize MTA data to optimize the placement of street teams.

---
## Approach

Before starting any data analysis, we have to understand the goal that the client wants to achieve. WTWY wants optimize street team placement to get as much email signups as possible. But more importantly, WTWY wants people to attend the gala and donate to the cause. Keeping the client in mind, we approach the project with the following steps:
1. Identify target neighborhoods
2. Identify target stations
3. Identify the time of day/day of week with the highest traffic

---
## MTA Turnstile Data



---
## Solution

**Identify target neighborhoods**

With some research, we found that the most giving people in New York City are in the age group 25-44. We decided to find the zip codes where people in this age group lives using the US Census data. The neighborhoods where our targeted age group lives in are marked in light purple on the map below. We also wanted to target people in the tech industry so we look for neighborhoods that have a high density of tech start-ups. The neighborhoods are marked in gray on the map below. 
	

![target-neighborhoods](/assets/img/benson/target_neighborhoods.png){:class="img-responsive"}


**Identify target stations**

After narrowing down the neighborhoods, we looked for the stations that have the highest weekly total ridership using MTA turnstile data from May 2017. Since the gala is held in early summer, we thought the month of May makes more sense for the WTWY street team to collect emails and distribute event tickets. May is not too close to or too far away from the event date for people to plan for attendance. The stations with the heaviest traffic in May 2017:
- UNION SQUARE
- GRAND CENTRAL
- PENN STATION
- HERALD SQUARE


![target-stations](/assets/img/benson/target_stations.png){:class="img-responsive"}


**Identify the time of day/day of week with the highest traffic**

We used a heat map to visualize the traffic at the target stations by day of week and time of day.


![heatmap](/assets/img/benson/heatmap.png){:class="img-responsive"}


---
## Recommendation

|**Stations** | **Time of Day** | **Day of Week**|
|:--------|:-------:|--------:|
|GRAND CENTRAL |5pm – 9pm | Wed - Fri|
|UNION SQUARE |1pm – 5pm | Mon - Fri|
|HERALD SQUARE |4pm – 8pm | Wed - Fri|
|PENN STATION |4pm – 8pm | Wed - Fri|


---
## Sources

- MTA Turnstile Data [http://web.mta.info/developers/turnstile.html]
- NYC Zip Code GeoJson: Civic Dashboards NYC Zip Code Tabulation Data
- NYC Subway Station Location Data: NYC Open Data Subway Entrances
- How America Gives [http://www.philanthropy.com] 
- Ultimate Guide to NYC’s Booming Tech Neighborhoods [http://www.builtinnyc.com] 
