
<!-- README.md is generated from README.Rmd. Please edit that file -->

<!--[![Travis-CI Build Status](https://travis-ci.org/SMAC-Group/imudata.svg?branch=master)](https://travis-ci.org/SMAC-Group/imudata)-->

[![Project Status:
Active](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![Licence](https://img.shields.io/badge/licence-CC%20BY--NC--SA%204.0-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.en.html)
[![minimal R
version](https://img.shields.io/badge/R%3E%3D-3.4.0-6666ff.svg)](https://cran.r-project.org/)
[![packageversion](https://img.shields.io/badge/Package%20version-0.1.0-orange.svg?style=flat-square)](commits/develop)
[![Last-changedate](https://img.shields.io/badge/last%20change-2018--05--16-yellowgreen.svg)](/commits/master)

# `imudata` Overview <a href="https://smac-group.com/"><img src="man/figures/logo.png" align="right" style="width: 20%; height: 20%"/></a>

This package is meant to serve as a data collection tool for IMU data.
This data can be used as a means to assess and test methods designed to
analyse IMU error signals (i.e. long and complex autocorrelated
signals). An example method used for this kind of data is implemented in
the `gmwm` R package which can also model the latent models that often
characterize this data.

The datasets available within the package are:

  - `imu6` - A MTi-G MEMS-IMU dataset with 6 columns corresponding to
    the stochastic error measurements coming from the X, Y and Z axes
    for gyroscopes and accelerometers respectively and taken from a
    sensor calibrated in stationary conditions for 2 hours at 100Hz.
  - `cont.imu1` - A MTi-G MEMS-IMU dataset with 1 column corresponding
    to the stochastic error measurements coming from the X-axis
    gyroscope and taken from a sensor calibrated in stationary
    conditions for 2 hours at 100Hz and possibly suffering from some
    contaminated measurements (e.g. outliers).
  - `navchip` - A Navchip MEMS-IMU dataset with 6 columns, Axis: X,Y,Z -
    Type: Gyroscope & Accelerometer, from a stationary sensor run for 4
    Hours
  - `imar.gyro` - An IMAR MEMS-IMU dataset with 3 columns, Axis: X,Y,Z -
    Type: Accelerometer, from a stationary sensor run for 4 Hours
  - `ln200.gyro` - A LN200 MEMS-IMU dataset with 3 columns, Axis: X,Y,Z
    - Type: Gyroscope, from a stationary sensor run for 6 Hours
  - `ln200.accel` - A LN200 MEMS-IMU dataset with 3 columns, Axis: X,Y,Z
    - Type: Accelerometer, from a stationary sensor run for 6 Hours
  - `kvh1750.acc` - Six samples collected from KVH1750 IMU at 100Hrz
    Axis: X,Y,Z - Type: Acce, from a stationary sensor run for 3 hours
  - `kvh1750.gyro` - Six samples collected from KVH1750 IMU at 100Hrz
    Axis: X,Y,Z - Type: Accelerometer, from a stationary sensor run for
    3 hours
  - `mtig1khrz` - Six samples collected from MTI-G-710 IMU at 1000 Hz
    Axis: X,Y,Z - Type: Gyroscope & Accelerometer, from a stationary
    sensor run for 10 minutes
  - `adis16405` - Six samples collected from ADIS 16405 IMU at 100Hrz
    Axis: X,Y,Z - Type: Gyroscope & Accelerometer, from a stationary
    sensor run for 3 hours

The first 6 datasets can be used as examples for the functions
`auto.imu()`, `gmwm.imu()`, `wvar.imu()`, and `imu()` of the `gmwm` R
package. Note that the `cont.imu1` data can be used as an illustration
of the robustness properties of the robust version the Generalized
Method of Wavelet Moments (GMWM). Here is a simple
example:

<center>

![](https://raw.githubusercontent.com/smac-group/imudata/master/img/demo.gif)

</center>

# Install Instructions

To install the package you can use:

``` r
# Install R devtools
install.packages("devtools")

# Install the package from github
devtools::install_github("SMAC-Group/imudata")
```

# Licensing

The license this source code is released under is the Creative Commons
Attribution NonCommercial ShareAlike (CC-NC-SA). In some cases, the GPL
license does apply. However, in the majority of the cases, the license
in effect is the Creative Commons Attribution NonCommercial ShareAlike
(CC-NC-SA) as the computational code is heavily dependent on armadilllo,
which has an MIT license that enables us to recast our code to the
Creative Commons Attribution NonCommercial ShareAlike (CC-NC-SA). See
the LICENSE file for full text. Otherwise, please consult [TLDR
Legal](https://tldrlegal.com/license/creative-commons-attribution-noncommercial-sharealike-\(cc-nc-sa\))
or [CC](https://creativecommons.org/licenses/by-nc-sa/4.0/#) which will
provide a synopsis of the restrictions placed upon the data and code.
