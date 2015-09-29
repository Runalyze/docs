=======================
Import (old) activities
=======================

We know that you have a bunch of activities you would like to import to RUNALYZE. To make it quite simple we support a lot of different file types.
Some of them are sometimes a bit tricky.


Devices
*******
Garmin
------
There was a time when the Garmin Communicator was great to easily import activities from the different devices. But sadly they (had to) discontinued this tool due to the support of the browser manufactures.
Garmin stores the activities in the *.FIT format, which can be read by RUNALYZE since version 2.0.

When you are using Garmin Express or the old ANT-Agent from Garmin you can upload the files from your Windows, MacOS or Linux system.

^^^^^^^^^^^^^^^
Garmin Express
^^^^^^^^^^^^^^^
Windows 8::

    C:\ProgramData\Garmin\GarminConnect\[foldername can be different (name of the device)]\FIT_TYPE_4

Windows 7::

    C:\ProgramData\Garmin\CoreService\Devices\[ID]\Sync\FIT_TYPE_4

Mac OS X::

    ~/Library/Application Support/Garmin/GarminConnect/Device-UnitID/Upload/FIT_TYPE_4

^^^^^^^^^
ANT-Agent
^^^^^^^^^
Windows:
Open in the windows file explorer the following path::

    %appdata%\Garmin\Devices
Then you have to open the folder with a several different numbers. Then you should find the folder *Activities*

Mac OS X::

    Macintosh HD/Users/BENUTZERNAME/Library/Application Support/Garmin/Devices/DEVICE-ID

^^^^^
Linux
^^^^^
There is a tool called "antf-cli" which you can find on github (https://github.com/Tigge/antfs-cli)
That tool should work with any compliant ANT-FS device in theory, but is definitly working with the Garmin Forerunner (60, 405CX, 310XT, 610, 910XT), Garmin FR70, Garmin Swim

Polar
-----

TomTom
------

Suunto
------

Apps & Webservices
******************
.. note::
          In the future we will have an API to implement a continuing import of other webservices.
          Yes, we want to add our service to tapiriik.

Strava
---------
| \- Does not encode pauses [#encodepauses]_

Runtastic
---------
|  \- Resampled file [#resampleddata]_
|  \- Does not encode pauses [#encodepauses]_

Nike+
-------
|  \- Does not encode pauses [#encodepauses]_

MapMyRun
--------
|  \- Does not encode pauses [#encodepauses]_

iRunner
--------
|  \- Does not encode pauses [#encodepauses]_



Different file types
********************
We get a lot of questions regarding the file types. Which one is better and which one contain more data.
To clear up these question we will answer these question in the following section.

FIT
---
 \+ Contains data like cadence, swimtype (strokecount ...)

TCX
---
| \+ Pauses can exists
| \+ expandable format (May contain more data - RUNALYZE support some of these extension. If you think anything important is missing just open an issue or write a mail to us)

GPX
---
 + Pauses can exists

ttbin
-----

logbook & logbook3
------------------

slf
---

pwx
---

hrm/gpx (combined)
------------------



.. [#resampleddata] The idea of resampling data is to reduce the size of files and/or to simplify the process of generating the map for an activity. When you import such data it is nearly impossible to calculate the length of the activity. Sometimes the pace graph will show useless lines.

.. [#encodepauses] Pauses can be encoded in TCX/GPX files with closed tracks/tracks segements. If they are not encoded RUNALYZE has to guess where pauses took place. If you have problems you can disable the detection of pauses in (General settings -> Activity form -> Detect pause)

.. note::
          This site may contain affiliate links to support the development and infrastructure of RUNALYZE
