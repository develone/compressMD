clone https://github.com/develone/compressMD.git
cd compressMD

./demo.sh
The VM is started with compressMD,jar

java -Xmx128m -Xms128m -jar dist/compressMD.jar MEL_navo-3950-o.tar

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

The software uses the following jars

dom4j-1.5.2.jar             jcommon-1.0.0.jar
forms-1.0.7.jar             jfreechart-1.0.1.jar
freehep-base.jar            jh.jar
freehep-graphics2d.jar      looks-2.0.4.jar
freehep-graphicsio-emf.jar  ncCore-2.2.16.jar
freehep-graphicsio.jar      poi-2.5.1-final-20040804.jar
freehep-graphicsio-pdf.jar  SPCLAB_colt.jar
freehep-graphicsio-ps.jar   SPCLAB_jj2000.jar
GribLib.jar                 SPCLAB_UI.jar
gui-commands-1.1.37.jar     visad.jar
jaxen-1.1-beta-4.jar
