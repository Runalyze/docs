====
VDOT
====

VDOT in RUNALYZE
*****************
According to the originally definition the VDOT can only be calculated from race results. This means you can get a prognosis for a half marathon after a 10k race. You can only use the VDOT in this case if you had a race result under perfect conditions.

But in general you want to know your current training pace in your preparation and a prognose for the next race.

Therefore RUNALYZE estimates your current VDOT form based on your activities. (It's an estimation - No exact calculation).
This estimation is based on your heartfrequency and training pace where by Jack Daniels has a VDOT-table in his book, which we use as a rough basis.

This VDOT estimation is not that easy. The maximal heartrate must be known and the heartrate in your activity should not go haywire due to a defect heart rate strap or other influences.
As mentioned before Jack Daniels table or rather the derived formula is just a rough basis.

Therefore you have the option to exclude an activity from the VDOT calculation. (e.g. for activities with long pauses)
You can also add a manual correction factor (Configuration -> General settings -> VDOT) to match your heart rate behaviour.


General
********

VDOT is the shortform of V-dot-O2Max, the maximum rate of oxygen flow.	This value is a good measurement for the possible performance of a runner.	Due to some additional factors, one talks about a pseudo V-dot-O2Max, which is equal for all runners at the same level.

Jack Daniels' famous Running formula serves some tables estimating the VDOT value. These formulas are used to estimate your VDOT and predict your race performances.

Your personal VDOT value is estimated based on the ratio of heart rate and pace in every of your runs.	The average over a given period is considered as your current shape.

Each VDOT value of an activity in RUNALYZE is marked with an arrow, to show if this value is (much) higher than your current shape, equal to it or (much) lower.

.. note::
    Of course, pauses, walking and other factors can heavily influence the ratio of heart rate and pace.	Activities with known influences or strange results can be ignored for the calculation of your shape.

In RUNALYZE you have the option to change the VDOT calculation, so that it is adapted to your requierements.

VDOT settings
**************

Manual correction factor
-------------------------
If you think your VDOT correction factor, which is based on your best competition is wrong/not perfect, you can add a manual correction factor. A correction factor between 0.85 and 0.95 should be realistic

Adapt VDOT for elevation
------------------------
If you make many vertical meters in your actitivies the VDOT may have a negative influence to your form. You can enable the adaption for elevation in the VDOT settings. You can set the correction per positive and negative elevation.
