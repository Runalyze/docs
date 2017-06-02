==========================
Frequently Asked Questions
==========================

If you have a concrete concept for a new feature, don't hesitate to submit and discuss your idea at our `Forum <https://forum.runalyze.com>`_ or at `GitHub <https://github.com/Runalyze/Runalyze/issues/new>`_.
This is the best place to discuss ideas and future features with other users and developers.

Please keep in mind that RUNALYZE is an open source project, at present based mainly on two developers offering their free time for this tool.

.. note:: Annoyed by phrases like *some day* and *probably*?
    Strengthen our team (development, design, communication, pr, docs, ...) to speed up development.

.. contents:: :local:

General questions
*******************

Will there be a synchronisation with other platforms?
--------------------------------------------------------
Yes, definitely! Our first concern is providing an API to work with `tapiriik <https://tapiriik.com/>`_.
Still, there are some months of work waiting for us until this is realizable. With every new release we are getting closer to this feature. Current schedule for this feature is in late 2017.

Will there be an app for smartphones?
--------------------------------------
Some day, probably. So far, this is not a high priority as there are many other areas requiring our full attention.

Can I publish my running diary?
--------------------------------
Fundamentally, RUNALYZE is in the moment not designed to be an athletes community.
Our main focus is on analyzing your training.

Anyway, you can mark single activities as public and share them by publishing a public url, or publish your entire list of activities.
Have a look at your privacy configuration for detailed information.
Furthermore, you can export any activity as html snippet or iframe and share them on twitter/facebook/google+.

What are calculations and prognoses?
--------------------------------------
RUNALYZE is more than just a logbook to track all your activities.
In addition to well known basic features RUNALYZE offers you statistics like VDOT and prognoses for your upcoming races.
We are using some formulas to estimate your current shape based on the ratio of heart rate and pace.
Still, these estimates must be handled with great caution. Don't rely on them and listen to your body.

Runalyze shows an incorrect total duration
-------------------------------------------
Most file types do not contain information about pauses. Especially tcx- and gpx-files provide no information if and when you stopped your device, e.g. at traffic lights or if you're using 'auto pause' on your device.
Runalyze offers the ability to detect such breaks automatically and can remove them without further notice.
Still, it's difficult or even impossible to exactly match your device's total duration.

You can enable/disable our automatic detection of pauses in your configuration.
In addition, we have an `open ticket <https://github.com/Runalyze/Runalyze/issues/913>`_ for a more flexible solution such that a specific threshold can be defined for each file separately.
Feel free to leave a '+1' at GitHub.

Runalyze says that there are not enough results for good predictions
---------------------------------------------------------------------
To get good predictions you need to have at least one race.

Where can I change my maximum heart rate?
-------------------------------------------
You can edit your maximum heart rate in the "Body values" panel. You may need to activate that panel (Configuration -> Panels)

Is there an impact when I change the sport relevance?
-------------------------------------------------------------
The categorization as 'main sports' and 'alternative sports' is just a preparation for future analyses. It's planned that one can group alternative sports and handle them as additional but less important training load.

The translation is missing
----------------------------
Translations are maintained by our users and we cannot guarantee that everything has been translated when we roll out a new version. :doc:`You can help us! <translation>`.

File import
************

The file import seems buggy? Incorrect values?
------------------------------------------------
Send us an email with your sample file and a detailed description of what your expected results.
We'll have a look at your issue and will try to fix it.


The file type \*.XYZ is not supported
--------------------------------------
Just send us an email with some sample files and we'll have a look at this.

Negative time step at index x
-------------------------------
There are some apps and devices which produces malformed files. In this case they contain negative time jumps, which we cannot process in the moment.

Activities
************

Power graph/Power data seems to be wrong
------------------------------------------
This is maybe a bit confusing and we will change this behaviour in a later version. To import the power from your files you should disable the manual power calculation in your configuration (Activity form -> Calculate power)

My activity does not show up in my race results
-------------------------------------------------
Every activity of any sport can be marked as a race by simply checking the respective checkbox. It is not enought to change the activity type to "race". :doc:`Read more <starting-guide/races>`.
