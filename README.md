# child name selector helper

set of scripts, that help to choose a reasonable name for a child, thanks to usage of historical data.
the aim is to select a name that is neither too popular (i.e. non-distinguishable) nor too uncommon (i.e. does not appear to be "from a different times").


## selector

python script for selecting names, that match given probability criteria.
for instance selecting name that is probable from 0.7% to 2.5%, based on males name, can be done like this:

./selector myinputdata.csv 0.7 2.5

actual input data for Poland, taken from GUS, are prepared in the 'input' directory, inside this repository.


## plot_name

shell script for plotting popularity of a given name in time.
requires bash and gnuplot to work.
example query, for name "BARTOSZ", from a given input file, can be seen:

./plot_name "myinputdata.csv "BARTOSZ" relative

last option can be "relative" or "absolute".

"relative" means OY axis is scaled, based on min/max values from a given query.
it is useful for precise monitoring of per-name trends.

"absolute" means OY axis is scaled, based on maximum birth count, of the most popular name of all years.
it is useful for comparing plots of different names.


## analyze_all

script that displays all the results for a given query.
for each name a separate window is opened, displaying per-name results.
