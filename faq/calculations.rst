==========================
Calculations
==========================

What are calculations and prognoses?
--------------------------------------
RUNALYZE is more than just a logbook to track all your activities.
In addition to well known basic features RUNALYZE offers you statistics like effective VO2max and prognoses for your upcoming races.
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

TRIMP calculation without heartrate
-------------------------------------
Average heart rate will be used as fallback for calculations like TRIMP if no heart rate data is available.

How is power calculated if there is no power data in activity files
--------------------------------------------------------------------
Performance is always automatically "calculated" (or estimated) for the sport of cycling if there is no data in the file itself. The formulas primarily take into account speed and gradient. Rolling resistance (crr = 0.004), drag coefficient (cw = 0.5) and frontal surface of the rider (a = 0.5), density (rho = 1.226) as well as the weight of the bicycle (10 kg) are assumed. However, other influences such as aerodynamics, changing subsoils and above all the wind cannot be taken into account. The formulas are based on `blog.ultracycle.net <http://www.blog.ultracycle.net/2010/05/cycling-power-calculations>`_ 



