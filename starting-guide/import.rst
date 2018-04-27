==================
Import activities
==================
.. contents:: :local:

We know that you have a whole bunch of activities you would like to import.
RUNALYZE supports a wide range of file types and tries to fit all your needs.
Still, some file types can be tricky.

.. note::
          Use - if possible - the fit file format for importing activities

Devices
*******

What kind of device do you have?

* :doc:`/import/devices/apple`
* :doc:`/import/devices/garmin`
* :doc:`/import/devices/polar`
* :doc:`/import/devices/suunto`
* :doc:`/import/devices/tomtom`

Export from other Webservices
*******************************

Strava
---------

| \- Does not encode pauses [#encodepauses]_


**OneClick Activity Bookmark TCX Downloader**

Drag the following link to your bookmarks bar - Just click on it when you're on the activity page

.. raw:: html

    <a href="javascript:window.location=window.location.toString()+'/export_tcx'">Strava Connect-Export</a><br>

Runtastic
---------
|  \- Resampled file [#resampleddata]_
|  \- Does not encode pauses [#encodepauses]_


**Bulk export of all activities via command-line**

Use the `Runtastic Archiver tool which is available at github <https://github.com/Metalnem/runtastic/releases>`_  (`How-TO <https://github.com/Metalnem/runtastic/blob/master/README.md>`_)

.. raw:: html

    <iframe width="700" height="394" src="https://www.youtube.com/embed/EMYozDasOv8" frameborder="0" allowfullscreen></iframe>

sports-tracker.com
-------------------

Try to download all activities with the tool `by Olivian Daniel Tofan <http://daniel.toffee.ro/2014/04/25/liberate-sportstracker-workouts>`_

Trainingstagebuch.org
----------------------
**How to export all activities as .gpx files**

Drag the following link to your toolbar/bookmarks

.. raw:: html

     <a href="javascript:(function(){var arr = [], l = document.links;for(var i=0; i<l.length; i++) { if( l[i].href.indexOf('http://trainingstagebuch.org/workouts/show/') >= 0){ var newFrame = document.createElement('iframe'); document.body.appendChild(newFrame);  newFrame.style = 'width: 1px; height: 1px;'; link = 'http://trainingstagebuch.org/map/export/'+l[i].href.replace('http://trainingstagebuch.org/workouts/show/','')+'?view=gpx';  console.log(link);newFrame.src = link; }}})();" title="Download trainingstagebuch.org">Download trainingstagebuch.org</a>


Open the `activity list page <http://trainingstagebuch.org/workouts/list?rows=320>`_ at trainingstagebuch.org and click on the bookmark. The download of the acitivies will begin. Repeat this step for every activity list page.



Different file types
********************
We get a lot of questions regarding file types: Which one is better and which one contains more data?
To answer these questions we have created a table to show what we can import from each file type (as long as your device logged this data).

Please send us an example file if you think we are missing some data during the import.

  * N = No
  * M = Maybe
  * C = Will be calculated if not present
  * CC = Will be calculated when a condition is given

  .. warning:: TTBIN file format - We are using at third-party component to convert the ttbin files. Unfortunately `swim <https://github.com/ryanbinns/ttwatch/issues/62>`_ activities cannot be imported in the moment. Please checkout the linked issues and help us

  .. warning:: FIT file format - Heartrate from swim fit files cannot be saved in the moment (`Issue #1498 <https://github.com/Runalyze/Runalyze/issues/1498>`_)

  .. note::
            Distances may be recalculated in some cases, when there are no distance information for gps datapoints.

  .. note::
            If you need remove sections, combine files or fix corrupt times in FIT files then use the website _`Fit File Tools <https://www.fitfiletools.com/?=runalyze#/top>`_.


+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Type                            | FIT    | TCX/TTBIN | GPX     | PWX     | hrm & gpx  | Fitlog   | Logbook (3)  | kml/kmz | TRK     | sml     | slf     | xml(Suunto) | csv(Epson) | hrm  |
+=================================+========+===========+=========+=========+============+==========+==============+=========+=========+=========+=========+=============+============+======+
| Distance                        | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | ✓            | ✓       | ✓       | ✓       | ✓       | ✓           | ✓          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Startdate/time                  | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | ✓            | ✓       | ✓       | ✓       | ✓       | ✓           | ✓          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Duration                        | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | ✓            | ✓       | ✓       | ✓       | ✓       | ✓           | ✓          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Sporttype                       |        |           |         |         |            |          |              |         |         |         |         |             |            |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Name                            |        |           |         |         |            |          | ✓            |         |         |         | N       |             |            |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Notes                           |        | ✓         |         |         |            |          | ✓            |         |         |         | ✓       |             |            |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Heartrate                       | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | ✓            | ✓       | ✓       | ✓       | ✓       |             | ✓          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Calories                        | ✓/C    | ✓/C       | C       | C       | C          | ✓/C      | ✓/C          | ✓/C     | ✓/C     | ✓/C     | ✓/C     | C           | ✓          | C    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| GPS                             | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | N            | ✓       | ✓       | ✓       | ✓       |             | ✓          |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Altitude                        | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | N            | ✓       | ✓       | ✓       | N       |             | ✓          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Temperature                     | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | N            | N       | ✓       | ✓       | N       |             | ✓          | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Laps/Rounds                     | ✓      | ✓         | ✓       | ✓       | ✓          | ✓        | ✓            | N       | N       | ✓       | N       |             | ✓          |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Pauses                          | ✓      | ✓         | N       | N       | ✓          | ✓        | N            | ✓       | N       | N       | N       |             | ?          |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Cadence (spm/rpm)               | ✓      | ✓         | ✓       | ✓       | ✓          | N        | N            | N       | N       | ✓       | N       |             | ✓          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Power                           | ✓      | ✓         | N       | ✓       | ✓          | N        | N            | N       | N       | N       | N       |             |            |      |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Stride length                   | CC     | CC        | CC      | CC      | CC         | N        | N            | N       | N       | C       | N       |             | CC         | CC   |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Ground Contact Time             | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       |             |            | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Ground Contact Balance          | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       |             |            | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Vertical oscillation            | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       |             |            | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Vertical ratio                  | CC     | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       |             |            | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Swim Strokes                    | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       |             | N          | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| Swim Stroke type                | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       | N           | N          | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| HRV                             | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | ✓       | N       | ✓           | N          | ✓    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+
| FIT details [#fitdetails]_      | ✓      | N         | N       | N       | N          | N        | N            | N       | N       | N       | N       | N           | N          | N    |
+---------------------------------+--------+-----------+---------+---------+------------+----------+--------------+---------+---------+---------+---------+-------------+------------+------+




.. [#resampleddata] The idea of resampling data is to reduce the size of files and/or to simplify the process of generating the map for an activity. When you import such data it is nearly impossible to calculate the length of the activity. Sometimes the pace graph will show useless lines.

.. [#encodepauses] Pauses can be encoded in TCX/GPX files with closed tracks/tracks segements. If they are not encoded RUNALYZE has to guess where pauses took place. If you have problems you can disable the detection of pauses in (General settings -> Activity form -> Detect pause)

.. [#fitdetails] FIT files contain some Garmin-only values like recovery time, performance condition, hrv score and V02max estimate.

.. note::
          This site may contain affiliate links to support the development and infrastructure of RUNALYZE
