# Predicting Foot Traffic on Hiking Trails 
## Project Proposal, Metis Project #2 (Luther)

## Kristin Mussar

### Scope: 
Hiking is one of the most popular summer activities for Seattleites. Understandably, as the city grows, the trails are experiencing more traffic. It can be difficult to find a trail that is not crowded and one which has parking available. I am proposing a tool which will allow users to see a score of the predicted foot traffic for a given trailhead and day. Users can use this to plan their trip accordingly, whether that means choosing a different trail, a different day to hike, or a different time to arrive. This data could also be used by urban planners to optimize new bus routes to popular trails in the area. 

### Methodology: 
1. Scrape trip report data from WTA 
2. Build linear regression model MVP: 
        Use prev. trip report data to predict future # of trip reports. 
3. Get weather data for both the trail area as well as Seattle weather. Add these features to dataset. 
4. Improve linear regression model

**Potential additional step:**

5. Create score for traffic of selected trail on selected day in comparison to a)trail history and/or b) other trails in the area. 

### Data Sources:
* Washington Trail Association - Trail reports per trail - www.WTA.org
* NOAA - weather data
* National Park Service - Traffic counts at park entrances by month: 
* Traffic count at each entrance by month: 
https://irma.nps.gov/Stats/SSRSReports/Park%20Specific%20Reports/Traffic%20Counts?Park=OLYM
* National Park Service - # Trail users by area of park per month: https://irma.nps.gov/Stats/SSRSReports/Park%20Specific%20Reports/Park%20YTD%20Version%202?Park=OLYM

### Target: 
* MVP: # of trip reports for a trail for a day
* Goal: Score showing relative traffic (to either trail history or trails in the area)

### Features: 
* Number of trip reports written
* Date 
    - Day of week
    - Month/time of year
    - Year
    - Holidays/events
* Trail conditions
    - Snow
    - others
* Weather (local)
    - Temperature
    - Precip.
* Weather (Seattle)
    - Temperature
    - Precip.


### Things to consider: 
* Trail reports are only an approximation of foot traffic to trails. There may be differences in demographics of hikers on different days of the week or in different seasons that cause some demographics to over-represent their visits with trail reports, or vice-versa. This can be partially confirmed with NPS's data on trail users/month. 
* I'm not sure which would be a more informative score: 
    - Trail's current crowdedness vs average/max crowdedness  
    - Trail's current crowdedness vs crowdedness of other trails in the area
* Hiking group posts and news articles promoting certain hikes will cause spikes in the number of people visiting certain trails. Incorporating this information into my model seems too sophisticated at the moment. (And I don't think Facebook likes scraping). 
