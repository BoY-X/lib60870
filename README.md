# README lib60870-C                      {#mainpage}

lib60870 library for IEC 60870-5 based protocols in C

The current implementation contains code for the IEC 60870-5-101 (application layer and serial link layer) and IEC 60870-5-104 (protocool over TCP/IP) specifications.

Features:
- support for all application layer message types
- master and slave
- balanced and unbalanced link layers
- portable C99 code

Please also consider the User Guide.


## Compiling and running the examples:


In the lib60870-C folder build the library with

`make`

Go to the examples folder and build the examples with

`make`

in each examples' directory.

The library and examples can also be build with _CMake_.

To build the library in a separate folder create a new folder as subdirectory of
the project folder and run cmake to create the build files:

`mkdir build`
`cd build`
`cmake ..`

## Building without common code and HAL

The library contains some common code and a platform abstraction layer (HAL) that is shared with
other protocol libraries of MZ Automation (e.g. libiec61850). In order to simplify using these 
protocol libraries together it is possible to compile the library without the common parts.

This can be done by using the *WITHOUT_HAL* and *WITHOUT_COMMON* defines when calling make:

`make WITHOUT_HAL=1 WITHOUT_COMMON=1`

## Building with TLS support

The library can be build with support for TLS. In order to do so you have to download mbedtls version 2.6.0.

Unpack the mbedtls tarball in the dependencies folder so that a folder

dependencies/mbedtls-2.6.0

exists.

The cmake build system will automatically detect the mbedtls source and build the library with TLS support and mbedtls included

When using make you have to call make with WITH_MBEDTLS=1

`make WITH_MBEDTLS=1`

## Contact:

The library is developed and supported my MZ Automation GmbH.

For bug reports, hints or support please contact info@mz-automation.de

## Licensing

This software can be dual licensed under the GPLv3 (https://www.gnu.org/licenses/gpl-3.0.en.html) and a commercial license agreement.

## Commercial licenses and support

Support and commercial license options are provided by MZ Automation GmbH. Please contact info@mz-automation.de for more details.


## Contributing

If you want to contribute to the improvement and development of the library please send me comments, feature requests, bug reports, or patches.

For more than trivial contributions I require you to sign a Contributor License Agreement. Please contact info@mz-automation.de.
