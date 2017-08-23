# GlobalTerroristAttack


Global Terrorist Attacks in 1970-2016 on a world map.
Data visualization created by D3.js.

Summary:

Terrorist attacks bring more casualties in the recent decades than before.
It could be due to more damage model weapons.
Terrorist attacks often happen in the same region over decades.

How to use:

1. run command python -m SimpleHTTPServer in your terminal
2. Open your browser and check it on http://localhost:8000/

Design:
I follow the "martini glass" narrative structure to organize the visualization.

1. plot the event on a world, most easiest way to see where the terrorist
attacks happen.
2. Use winkel3 map projection, events are mainly in countries close the equator
and not much in the north. Comparing to the most common map projection Marcator,
winkel3, which the north area are not enlarged, gives more reasonable visualization.
3. Use the size to circle to show the casualties of events. I think it is a reasonable
way to measure the severity of terrorist attacks.
Readers can explore for more information by move mouse over the circle.
4. Light blue color are the main color, comfortable to stare for a long time;
Circle are light orange, to draw attention.  
5. Animation starts at the beginning, shows what were happening.
Readers can choose which year to focus after the animation.
6. Quick animation, most readers are impatient. Most important, quick animation shows
the continuity， support the summary: terrorist attacks often happen in the same
region over decades.



Dataset:

The original data is available in https://www.kaggle.com/START-UMD/gtd
It contains 170350 entries, one for each terrorist attack event.
It is too show and heavy to show all the events in the map, hence I use
terroris-clean.ipynb file to do preprocess on the data. The events are
grouped by the year and country, and sum up the number of deaths and wounded
as an aggregated event for the country in a year. The place for the aggregated
event is the mean of the longitudes and latitudes. A circle with the size
Proportional to the number of casualties are placed on the right spot on map
by using longitude and latitude.



Feedbacks and updates:

person A
1, adjust speed of animation. updated, set a faster speed for impatient readers.

person B
2, meaning of circle. updated, The size of circle shows how many times and how many
casualties of terrorist attacks in a place given a certain year. Readers can move
the mouse over a circle to see more information.
3, circles should be sorted such that the smaller ones are on the top of the bigger
ones, thus reader can click all of them. updated. updated code on ipynb data clean
file.

person C
4, the title "mouse over a circle to see the number of casualties" should be shown
after the animation, to avoid distraction while reading the animation. Updated.


main feedbacks from reviewer:
1. add legend to help reader understand what does the circle mean at the beginner.
updated.
2. Instead of showing all events in 1970-2016 when choose "total" button, group
the event by countries, and when click "All casualties 1970-2016", so the total number
for each country. updated. see function show_all_year
3. all the button color should be reset when other button is select. updates.
4. the casualty number should show as an Integer rather than float. updated.


You can see the old version in first_submission.html
