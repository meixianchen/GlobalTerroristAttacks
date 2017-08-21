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

1, adjust speed of animation. updated, set a faster speed for impatient readers.
2, meaning of circle. updated, The size of circle shows how many times and how many
casualties of terrorist attacks in a place given a certain year. Readers can move
the mouse over a circle to see more information.
3, the title "mouse over a circle to see the number of casualties" should be shown
after the animation, to avoid distraction while reading the animation. Updated.
