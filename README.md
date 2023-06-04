# Kids-ChoreChart

This is a project where I followed a great guide which can be read here https://community.home-assistant.io/t/created-a-chore-tracker-with-points-system-in-home-assistant/316175 
I played around with different ways to show the information as it's being displayed on a vertical screen much like a mobile device. I have this on 2 dashboards, they are identical except for 
one difference being the parents dashboard has the option of enabling and disabling extra chores which the kids dashboard does not have, this is the same for things like enabling wifi 
for their devices etc.

Tostart off with I created helper toggles for each childs chores, for the extra chores I created a toggle for the parents to enable and a chore for each child, in terms of icons for their actual
chores the icon was selected as something that resembled the chore, for the extra chores it showed a male and femal face so they could select who did the extra chore or in some cases they could both do the chore.

I have automations setup that will increment and decrement the daily and monthly counters whenever they mark a chore as done however this has a condition that the time cannot be between 23:30 and 1:30 (2 hours is probably overkill but they not doing chores at this time) This is so I can reset the chores without at midnight without impacting their totals, I also added an additional helper for daily and monthly chores to be updated with the daily value or monthly value at month end, this was because sometimes they could enable a chore and then don't do it so they disable it again, if I use the max value for the graph that would be counted, to avoid that I just read the value at the end of the day and use that helper for my graphs.

I also have automations for things like the dishwasher, once 1 child does the dishwasher after an hour the chore will move to the next child, I never had this initially until I ended up having the dishwasher unpacked twice in one day so needed to find a way to match my wifes strict cleaning routines :) 


