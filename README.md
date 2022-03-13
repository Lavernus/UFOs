# Analysis of UFO Sightings Webpage
## Overview
The client has provided data pertaining to UFO sightings in a JavaScript array. They need a responsive webpage that will take user input to filter and display a table containing the UFO data.
### Purpose
Utilizing JavaScript and Bootstrap, I will create a webpage that displays an article the client has written as well as a table containing UFO data that users can filter with multiple criteria.
## Results
The webpage displays the heading: "The Truth Is Out There" at the top of the page with the article's title, tagline, and content below. Underneath this, a table appears containing all the data pertaining to UFO sightings that was provided in the Javascript array. Next to this is a "Filter Search" bar with five separate criteria that the user can use to find specific sightings.
![Base_Page.png](https://github.com/Lavernus/UFOs/blob/main/Ref/Base_Page.png)
As you can see from the base page, each search bar contains default text that suggests to the user how they should type their search into the bar. Everything must be in lowercase, with the city and state abbreviated and the date in month/day/year format. 

To start a search, the user could choose to filter by the location the sighting occured in. Searching by country isn't that useful, as most of the data occurs in the United States, so searching by the state would be a good place to start. If they choose to see all the data pertaining to California, they would type "ca" into the "Enter State" search and hit the enter key. The table will refresh to show only the sightings occuring in California:
![Filter_State.png](https://github.com/Lavernus/UFOs/blob/main/Ref/Filter_State.png)

If the user wanted to narrow the search even more, they could enter which city's data they would like to see. Typing "el cajon" into the "Enter City" search and hitting the enter key will refresh the table to show only the sightings occuring in El Cajon. Since the user kept the state search as "ca" it will only show the data of the El Cajons that exist in California.
![Filter_City.png](https://github.com/Lavernus/UFOs/blob/main/Ref/Filter_City.png)

Narrowing it further by the shape of the UFO is possible by typing the desired shape into the "Enter Shape" search and hitting the enter key. If the user keeps the previous searches as is and enters "light" into the search they will have narrowed the table down into only two sightings:
![Filter_Shape.png](https://github.com/Lavernus/UFOs/blob/main/Ref/Filter_Shape.png)

The user can also narrow the search with the date the sighting occured on. Typing "1/4/2010" into the "Enter Date" search without deleting any of the previous searches will produce a table containing sighting data that occured on 1/4/2010.
![Filter_Date.png](https://github.com/Lavernus/UFOs/blob/main/Ref/Filter_Date.png)



## Summary
This setup accounts for multiple criteria in the searches, allowing the user to narrow the scope of their search to specific instances of UFO sightings. One drawback of this webpage, however, is that it is not apparent to the users the limitations of the dataset. This means that they could be fruitlessly searching for sightings that occured in Mexico or Ireland without realizing that the data for these countries aren't included in the dataset. 

One way to fix the aforementioned problem would be to create drop-down lists for the searches that have a smaller number of options to choose from. The only countries included in the dataset, for example, are the United States and Canada, so when clicking on the search bar for "Enter Country" a drop-down list could appear containing those two options, letting the user know their search is limited to only them.

Another way to improve the webpage would be expanding the search capabilities to duration of sighting. Users could access a drop-down menu of time ranges that would search for sightings that had a duration occuring within that range. This would require regex development within the code to categorize each sighting's duration within a different time range, with an additional bin to contain the miscellaneous entries such as "from dusk to dawn" or "not sure".
