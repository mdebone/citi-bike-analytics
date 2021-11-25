 citi-bike-analytics


potential projects:
-------------------------

So going to look at monthly covid usage of citi bike, to the 3 year running average prior to the pandemic, as new york was empty, I bet there was a dramatic drop in usage.
Also going to look at seasonality of citi bike, so need either 4 quarters or 2 half year benchmarks.

The movement of bikes from one location to another during off hours, ie, i bet the direction of many bikes is one directional, that is, more people take one to work and then use other transit to get home.

Holiday peak usage, does it drop dramatically? we can look at major us holidays, so new years jan 1st, memorial day, may 31st, independence day july 4th, labor day september 6th, october 31st,
last week of the calendar year, versus whenever new york public schools have their spring break? need to find that out()

So holidays, let's grab those for the same year.
And then we'll just track general monthly trends, which I think is a seperate site NYC Department of Transit or something, it was back one page. may 6th may 26th 2019, 2020

There are operations reports, we are going to have to look at regular usage to see if there is an uptick in holiday usage, so maybe a date a week before and a date week after to provide context, we are using 2019 2020 dates.

Okay so after looking at the data:
---------------------

Not much of this is achievable, after looking at the data, I decided the three year running after was too cumbersome, and decided to change to a two-year, calendar year, month to month change by a variety of metrics. 
Looking through the dataset, there are two complete years, 2020 & 2019. I would have gone with 2020-21, but the December data has not been published.

Nor were the holiday dates, I think out of 6 holidays I searched for, the closest I got was july 3rd, to any of them. 
Given a cursor analysis, there was some information regarding the dates of the files. 
These have arbitrary names but when you look at them for long enough they are all offset by one month, at least insofar that January is month 12 of the previous year.

This isn't because these reports are delayed by a month, like a monthly operating report published in December is typically everything that went on in November, no these are daily reports on the number of uses. 
But what is interesting is that they appear to be totally random, for the 12 months of 2019, I got ten weekdays, and two weekends, (they are fridays), but I expect that there might be something to glean from that. 
2020 was 7 weekdays, 5 weekends, and one full weekend day, a sunday on July 5th.

This isn't because these reports are delayed by a month, like a monthly operating report published in December is typically everything that went on in November, no these are daily reports on the number of uses. But what is interesting is that they appear to be totally random, for the 12 months of 2019, I got ten weekdays, and two weekends, (they are fridays), but I expect that there might be something to glean from that. 2020 was 7 weekdays, 5 weekends, and one full weekend day, a sunday on July 5th.

First analysis is Start time, plotting that as a bar, columns with HOUR(Starttime), 2019 on the whole shows two peaks (really 4, but allow me to explain), people leaving at 8 to get to work by 9, and people leaving at 9. 
The idea of commuters in 2019 makes sense and the end time analysis bares some of this out, the endtime peak hours are 17 and 18, 5 oclock and 6 oclock respecisicitvely.

Third analysis, is Birth Year, which is a shmorgishborg of BirthYears' like, looking at it as a range, the number of people who were biking in 2019, that were born before Lincoln gave his Emancipation Proclamation, 
is like 50 riders a day. And then the values continue like that all the way to 1945, which is where I decided in the remotes sense, there might be an outside chance of someone over 65, who bikes for leisure, 
but even that is suspect. How I chose to get around this was by group, Birth Year into bins, 17 and younger, 18-24, 25-34, 35-44, 45-54, and 65 and above (it goes to 75). 
But when I revisit this Im probably going to drop the 65 and older age group cause It doesn't make sense, but I would say that the rest of it does, there is a pretty decent distribution that varies between all 4 remaining, 
and I need to look at what the corporate policy of Citi Bike is on adolescents. 
Their number is low, so do they have a policy as to you have to be a certain age to ride a bike, liability I am sure, rather than ability to do so would be driving that decision.

Start Station and End Station (4 & 5), the next two views, allow one to see the distribution of popular to least popular stations. 
Overwhelmingly its Manhattan, Brooklyn shows up as second, Queens has a trickle, and the Bronx and Staten Island aren't even represented.

UserType's Impact on Trip Duration(6) is next, Usertype is broken down between two groupings, Customers and Subscribers. 
On Load, was reversed with a SUM rather than average, but I realized that I could tell a lot in one graph and so that's why there aren't multiple of these. 
Generally, the Subscribers travel more, on the order of five times more across all months analyzed. 
That is to be expected, but Customers, travel, on average, tend to double and in a few instances even triple the trip duration of subscribers (because they're commuting to work) and customers  
who see no benefit in paying? to become a subscriber on a vacation trip because when would they ever use it again.

Gender(7), tends to play out as a 3 to 1 male to female breakdown, with Non-respondents at no more than 10% across all 24 months analyzed.

The last four analyses(8-11) are Top 20 Starting and Ending Stations, and Bottom 20 Starting and Ending Stations. 
Start Station Name and Ending Station Name were called in the first two, as a dimension, and sorted by the field of the Number of Records. 
The Same goes for Bottom 20 Starting and Ending Stations, except ordered ascending, and I made the choice to filter out all the null and no data stations on this list. 
Start Top and Bottom are included simply to show a sense of scale, the end grouping tends to have at most 300 people over average but can typically start as much less.

And realizing that it was intended to be a report to the Mayor, rather than shareholders or board members of CitiBike, 
where it would be easy to say hey offer a coupon on these low revenue generating stations for a year and see if that increases the usage, 
because the infrastructure is already there. 
But if it's to a city official, you know 
recommendations would be: hey, make sure that these well-trafficked stations have adequate security, are well lit, and maybe recommendations on bike lane maintenance (if already in place), 
and if not, could be a suggestion towards public policy.









