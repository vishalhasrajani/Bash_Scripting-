## Exercise
Compose a BASH script to correlate the location number to the actual location name. If you look at the file BTemperature_Stations.txt, each station, numbered 1 to 338, has a proper name. For example, station number 28 is KELOWNA, and station 241 is TORONTO. If you consider the line of the file corresponding to TORONTO, it looks like:

241 6158355 TORONTO           ON  1840  3  2012 12      43.67    -79.40     113       Y

where the location/station number is first (241), followed by the station ID code (6158355), followed by the station name (TORONTO), followed by province (ON), year the measurements begin (1840), month in 1840 (3 - March), final year of measurements in the dataset (2012), final year month (12 - December), and additional information, including the latitude and longitude of the site location.

Your BASH script, findtemp.sh, should filter the output of query.sh to produce an output with the proper name of the site, rather than a file name. Your script should be used as follows:

$ ./findtemp.sh 1948 318

MONTICELLO

1948

-9.5

## Exercise
Now, compose a BASH script to create a file, testdata.dat, which contains climate data for a specific site over a number of years. Your script, called testgen.sh, should be used as follows:

$ ./testgen.sh 218 1948 1997 

where 218 represents the site location, 1948 the start year, and 1997 the final year. The generated file, testdata.dat, should look something like:

$ cat testdata.dat

KAPUSKASING

1948

-3.6


KAPUSKASING

1949

-5.2


.
.
.


KAPUSKASING

1997

2.6


-9999

-9999

-9999


where the three rows of -9999 are included to indicate the end of the valid data. These will be useful for our C-code.
