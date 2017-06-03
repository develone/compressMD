clone https://github.com/develone/compressMD.git
cd compressMD

./demo.sh

This requires java.
Tested on RaspBian

java -version
java version "1.8.0_65"
Java(TM) SE Runtime Environment (build 1.8.0_65-b17)
Java HotSpot(TM) Client VM (build 25.65-b01, mixed mode)

This should create several new windows
The Meteorological Models create forecasts out to 72 hours of various 
Parameters T, barometric press, Water Vapor Winds UVW
With the Cubes of Data for each 4 hours the data is compressed using JPEG 2000 in the horizontal
and either the KLT or DTW in the veritical directions.

The error in the numerical data is maitained for each of the parameters.
The input data can be either GRIB or netcdf.
Images are pgx format for each layer of various Met parameters.
The cube starts at the surface at 1013 millibars to a height of 10 millibars.
