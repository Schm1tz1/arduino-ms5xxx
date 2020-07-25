arduino-ms5xxx
==============

Arduino Library with examples for using digital pressure sensors MS5607/MS5611 (and MS56xx, MS57xx, MS58xx) based on AN520 by manufacturer and the datasheets. This library has been tested extensively (over almost a year of datataking) with MS5607 and also tested newer MS5611 sensors. 

Please note the different I2C-addresses, calculations and correction functions between the different chips and series. One generic MS5xxx-class as well as a derived class MS5611 with the default I2C address and the new calculations have been implemented. Nevertheless you should check that the sensor's I2C address with some kind of [I2C-Scanner](https://gist.github.com/Schm1tz1/00c36cc94f544c0d00e4627e8a6a66d3) in case it doesn't connect and set the I2C-Address of the sensor before running the connect() method:
```
...
MS5xxx sensor(&Wire);
sensor.setI2Caddr(0x42); //change the 0x42 to the I2C address that was found by your scan.
...
if(sensor.connect()>0) {
...
```

The examples nicely show how to use this library with the standard MS5xxx-class. For usage with MS5611 chips just use the class MS5611 in the same way.
"Standard units" are Pascals for pressure and 0.01 °C for temperature as calculations are done exactly as shown in the manufacturers datasheet.
