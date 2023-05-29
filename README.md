# NMEA barometer sensor

Measures temperature and pressure from a BMP280 sensor and sends it to a NMEA 2000 network.

## How to use example

Follow this guide to setup ESP-IDF to build and flash your esp32 board:

- [ESP32 Get Started](https://docs.espressif.com/projects/esp-idf/en/v4.4.4/esp32/get-started/index.html#get-started-get-esp-idf)
  
Note: The latest version of ESP-IDF is not compatible with the Ardunio library used. THe above link is for version 4.4.4. 

## Debugging CMake

The main branch will build. It does not include the NMEA 2000 library. 

The NMEA2000_subdirectory branch adds the [NMEA2000 library](https://github.com/ttlappalainen/NMEA2000) as a git submodule and as a subdirectory in the project's CMakeLists.
That branch builds after the NMEA2000 is cloned, but will not build once added as a subdirectory in CMakeLists.

The NMEA2000_include branch includes the NMEA library in NMEAB_Barometer.cpp and uses it to set the CAN message buffer size. 
This does not build.


