============
Garmin
============

Direct sync with Garmin
========================

The easiest way is to connect your Garmin account directly within RUNALYZE. Just click on the "Automatic Sync" button next to "Add workout" and connect your account with Garmin. If your RUNALYZE account is connected to Garmin, all future activities and those of the last 30 days will be transferred. To start the initial sync you need to track at least one new activity at Garmin. Afterwards Garmin will send us the last 30 days of activities. This can take some time (hours up to one day).


Garmin Connect
--------------

**General information**

If you want to download individual activities make sure you download the "original" file. That's a zip file which contains a fit file. You can just take the zip file as we support the import of zip files.
We do not support the import of the "activities" csv file you can download on the general activity page as it only contains average values. These values does not make sense when you want to you the prognosis and calculation features in RUNALYZE.

**Bulk download**

Garmin provides an option to download all your data you have ever provided to Garmin Connect. Just go to `Garmin Datamanagement <https://www.garmin.com/en-US/account/datamanagement/exportdata/>`_ and request your files. You will receive a mail with a download link shortly.
In the folder "DI_CONNECT"-> "DI-Connect-Fitness" you will find one or multiple zip files (beginning with "UploaedFiles").
Just extract that archive and upload that files to runalyze

.. note::
    You can write a support message to mail@runalyze.com with an attached backup of your files. We will import them into your account. Don't forget to mention your username.



**How to download all activites via script**
You need to be a bit more technique affin for this. Python and the python package `mechanize` must be installed on your system.
Now you need to `download the script at <https://github.com/JohannesHeinrich/garmin-connect-export>`_.
Execute the `download.py` script::

    python gcexport.py -d activities -c all -f original -u --username <Username> --password <Password>

Or if you just want to download the last 3 activitivies

    python gcexport.py -d activities -c 3 -f original -u --username <Username> --password <Password>

**OneClick Activity Bookmark FIT Downloader**

Drag the following link to your bookmarks bar - Just click on it when you're on the activity page

.. raw:: html

    <a href="javascript:window.location=window.location.toString().replace('activity/','proxy/download-service/files/activity/')">Garmin Connect-Export</a><br>


Local files
--------------
Some years ago, it was easy to sync your Garmin device via the so called *Garmin communicator*.
We did not remove this option so far but the browser plugin itself is officially discontinued.

Newer Garmin devices can be used as ordinary usb mass storage. Just pick your \*.fit file from a directory called *ACTIVITIES* or similar.
If your device synchronizes with Garmin Connect automatically you can download your activity as zipped \*.fit file from the activity's page (look for the "*original format*").

.. raw:: html

    <iframe width="700" height="394" src="https://www.youtube.com/embed/TU0ZDUEbWIY" frameborder="0" allowfullscreen></iframe>


If you are using Garmin Express or the old ANT-Agent you can upload the files from your Windows, MacOS or Linux system. Just look for the files in the following directories.

^^^^^^^^^^^^^^^
Garmin Express
^^^^^^^^^^^^^^^
Windows 8::

    C:\ProgramData\Garmin\GarminConnect\[foldername can be different (name of the device)]\FIT_TYPE_4

Windows 7::

    C:\ProgramData\Garmin\CoreService\Devices\[ID]\Sync\FIT_TYPE_4

Mac OS X::

    ~/Library/Application Support/Garmin/GarminConnect/Device-UnitID/Upload/FIT_TYPE_4

or::

    ~/Library/Caches/Garmin/Express/<Device-UnitID>/History


^^^^^^^^^
ANT-Agent
^^^^^^^^^
Windows:
Open in the windows file explorer the following path::

    %appdata%\Garmin\Devices
Then you have to open the folder with your device ID as name and find the folder *Activities*.

Mac OS X::

    Macintosh HD/Users/BENUTZERNAME/Library/Application Support/Garmin/Devices/DEVICE-ID

^^^^^
Linux
^^^^^
There is a tool called `antf-cli <https://github.com/Tigge/antfs-cli>`_.
That tool should work with any compliant ANT-FS device in theory and it certainly does for Garmin Forerunner (60, 70, 405CX, 310XT, 610, 910XT) and Garmin Swim.
