FlightPlot
==========

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/DrTon/FlightPlot?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Build Status](https://travis-ci.org/PX4/FlightPlot.svg?branch=master)](https://travis-ci.org/PX4/FlightPlot)

Universal flight log plotter

Docs and releases can be found on [pixhawk.org/dev/flightplot](http://pixhawk.org/dev/flightplot).

Development
-----------

IntelliJ IDEA IDE was used to develop FlightPlot, project files already exist in repo.

### Supported formats:
 - PX4 log (.px4log, .bin)
 - APM log (.bin)
 - ULog (.ulg)

### Features:
 - Data processing: low pass filtering, scaling, shifting, derivative, integral, etc.
 - Track export in KML and GPS format
 - Saving plot as image

Binaries for Linux, Mac OS, Windows can be found on the [project homepage](https://github.com/PX4/FlightPlot/releases).

Building from source
--------------------

Requirements:
 -  Java 6 or newer (JDK, http://www.oracle.com/technetwork/java/javase/downloads/index.html)
 -  ant
 -  安装依赖：
```
sudo apt-get install ant openjdk-8-jdk openjdk-8-jre -y

```
Clone the repository. The `--recursive` flag is required to pull in the [jMAVlib](https://github.com/PX4/jMAVlib) submodule).
```
git clone --recursive https://github.com/PX4/FlightPlot.git
```

Build:
```
cd FlightPlot
ant
```

If you want to create deb file for ubuntu, use gen_deb.
```
cd FlightPlot
ant gen_deb
sudo dpkg -i out/production/FlightPlot.deb
```

Run:
```
java -jar out/production/flightplot.jar
```

## mac下载链接
[mac download](https://github.com/PX4/FlightPlot/releases/download/0.3.2/flightplot.app.zip)

## linux jar 下载链接
[linux download](https://github.com/PX4/FlightPlot/releases/download/0.3.2/flightplot.jar.zip)