DNS Analysis Scripts
==========

A collection of scripts used to detect Fast-Flux domains and DGA domains.

Based on research conducted for [MSc thesis](http://contentpro.seals.ac.za/iii/cpro/app?id=4780004999704752&itemId=1007739&lang=eng&service=blob&suite=def), related research papers are available from the following locations:
* [ISSA 2011](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6027531 "A framework for DNS based detection and mitigation of malware infections on a network")
* [ISSA 2012](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6320433 "Geo-spatial autocorrelation as a metric for the detection of Fast-Flux botnet domains")
* [Botconf 2013](https://www.botconf.eu/wp-content/uploads/2013/08/09-EtienneStalmans-paper.pdf "Spatial Statistics as a Metric for Detecting Botnet C2 Servers")

Basic Usage
----------

To analyse a single domain:

```python FFanalyse.py -d exampledomain.com```

To analyse multple domains:

```cat domains.txt | xargs -I {} python FFAnalyse.py -d {}```

The URLAnalyse and Geolocate scripts can also be used in isolation, please see the documentation for each of these for usage info.

**Dependencies**
These can all be installed with a simple *easy_install <package name>*
* pygeoip
* mgrs
* dnspython
* pytz

**Note about MaxMind Databases:**
*For Geographic analysis you require the MaxMind databases. These are not included here, please get these from MaxMind.*
* GeoIPCity.dat
* GeoIPASNum.dat
* GeoLiteCity.dat

