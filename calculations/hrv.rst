===
HRV
===

Heart rate variability
**********************
Heart rate variability (HRV) is the physiological phenomenon of variation in the time interval between heartbeats and is measured by the variation in the beat-to-beat interval.
It is well known that HRV is directly related to the body's interdependent regulatory systems and can be a powerful measure for an athlete's recovery status.

HRV during exercise
*******************

It is best practice to measure you heart rate variability on a daily basis e.g. each morning after waking up while still in bed.
Unfortunately, that's not what is contained in all that data you upload to Runalyze.
Instead, you go out for a run or a ride and measure your heart rate (and its variability) during exercise.

HRV analysis can be done for HRV during exercise as well but values are less reliable and vary alot between different intensities.

.. note::
    Please be cautious while interpreting your values.

HRV in Runalyze
***************

Runalyze offers HRV analysis for all files that contain exact R-R intervals, i.e. the exact times between all heartbeats.
This can be the case for \*.fit files from Garmin (if respectively configured), \*.hrm files from Polar [#polar]_ and \*.xml/\*.sml files from Suunto.

.. note::
    Most devices using an optical sensor for measuring heart rate are not accurate enough (e.g. Mio Alpha, see [#baddevices]_),
    but there are ways to achieve good accuracy with opical measurements, see [#camerahrv]_.


Time-domain methods
*******************

Runalyze uses `time-domain methods <https://en.wikipedia.org/wiki/Heart_rate_variability#Time-domain_methods>`_ from v2.2 on:

avg. R-R interval
  average R-R interval, directly related to average heart rate
RMSSD
  root mean square of successive differences
lnRMSSD
  natural logarithm of *RMSSD*
SDNN
  standard deviation of R-R intervals
5 min-SDANN
  standard deviation of the average R-R intervals calculated over 5 minutes
pNN50
  proportion of successive R-R intervals that differ by more than 50 ms
pNN20
  proportion of successive R-R intervals that differ by more than 20 ms

Especially *RMSSD* (and its equivalent *lnRMSSD*) and *pNN50* are said to be strong indicators for parasympathetic activity [#hrvlexikon]_
and thus large values indicate a better recovery status.

From v2.6 on, RUNALYZE does use only R-R intervals that differ from the preceding or following interval by less than 75 % (as suggested in [#ediss1118]_, 2.4.2.1).


Further readings
****************

A look at a few months of hrv data
----------------------------------
Marco Altini, a data scientist and creator of multiple hrv based apps, measured his hrv every morning for a few months
and `presents the results on his blog <http://www.marcoaltini.com/blog/a-look-at-a-few-months-of-hr-and-hrv-measurements>`_.

Heart rate variability explained
--------------------------------
Andrew Flatt, who did a lot of research on HRV, `explains HRV <http://hrvtraining.com/2012/01/16/heart-rate-variability-explained-part-1/>`_

References
**********

.. [#polar] http://www.polar.com/us-en/support/Heart_Rate_Variability__HRV_
.. [#baddevices] http://www.marcoaltini.com/blog/heart-rate-variability
.. [#camerahrv] http://www.marcoaltini.com/blog/heart-rate-variability-using-the-phones-camera
.. [#hrvlexikon] http://www.hrv24.de/HRV-Lexikon.htm
.. [#ediss1118] http://www.zhb.uni-luebeck.de/epubs/ediss1118.pdf
