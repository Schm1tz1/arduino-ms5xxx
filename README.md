arduino-ms5xxx
==============

Arduino Library with examples for using digital pressure sensors MS5607/MS5611 (and MS56xx, MS57xx, MS58xx) based on AN520 by manufacturer. This library has been tested extensively (over almost a year of datataking) with MS5607 and also newer MS5611 sensors. Note the different "standard" I2C addresses of the different chips (e.g. 0x76 for 5607 and 0x77 for 5611).

The examples nicely show how to use this library. "Standard units" are Pascals for pressure and 0.01 °C for temperature as calculations are done exactly as shown in the manufacturers datasheet.

<a href="http://dx.doi.org/10.5281/zenodo.11966"><img src="https://zenodo.org/badge/6485/Schm1tz1/arduino-ms5xxx.png"><a>
