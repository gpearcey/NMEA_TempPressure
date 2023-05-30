# The following lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)

#
# Find the Espressif IDF (IoT Development Framework) path, which
# contains CMake descriptions of the Espressif toolchain.
#
find_path(IDF_PATH tools
          DOC "Espressif IoT Development Framework directory"
          PATHS $ENV{IDF_PATH})

if(NOT IDF_PATH)
    message(FATAL_ERROR "Cannot find IDF tools; try setting IDF_PATH env var")
endif()

include(${IDF_PATH}/tools/cmake/project.cmake)
#set(EXTRA_COMPONENT_DIRS /home/gracepearcey/esp/external/NMEA2000)
#add_subdirectory(/home/gracepearcey/esp/NMEA_TempPressure/external/NMEA2000/)
project(NEMA_TempPressure)
