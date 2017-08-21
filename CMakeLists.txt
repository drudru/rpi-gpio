#
# project: rpi-gpio
#

if (NOT FIPS_IMPORT)
    cmake_minimum_required(VERSION 2.8)
    get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
    include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    fips_setup()
    fips_project(rpi-gpio)
endif()

#-[ libs ]---------------------------------------------------------------------

fips_begin_lib(rpi-gpio)
    include_directories(rpi-gpio)
    fips_dir(rpi-gpio)

    fips_files(
        mmapGpio.hpp
        mmapGpio.cpp
    )
fips_end_lib()

#if (NOT FIPS_IMPORT)
#    fips_finish()
#endif()

