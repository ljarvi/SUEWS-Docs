SUEWS_Profiles.txt
~~~~~~~~~~~~~~~~~~

SUEWS_Profiles.txt specifies the daily cycle of variables related to
human behaviour (energy use, water use and snow clearing). Different
profiles can be specified for weekdays and weekends. The profiles are
provided at hourly resolution here; the model will then interpolate the
hourly energy and water use profiles to the resolution of the model time
step and normalize the values provided. Thus it does not matter whether
columns 2-25 add up to, say 1, 24, or another number, because the model
will handle this. Currently, the snow clearing profiles are not
interpolated as these are effectively a switch (0 or 1).

If the anthropogenic heat flux and water use are specified in the met
forcing file, the energy and water use profiles are not used.

Profiles are specified for the following

-  Anthropogenic heat flux (weekday and weekend)
-  Water use (weekday and weekend; manual and automatic irrigation)
-  Snow removal (weekday and weekend)
-  Human activity (weekday and weekend) **- not used in v2017a**.

+------+-----+--------+---------+-----------+-----------+
| No.  | Use | Column | Example | Descripti |           |
|      |     | name   |         | on        |           |
+======+=====+========+=========+===========+===========+
| 1    | L   | Code   |         | Code      | SUEWS_Sit |
|      |     |        |         | linking   | eSelect.t |
|      |     |        |         | to the    | xt]]:     |
|      |     |        |         | following | -  Energy |
|      |     |        |         | columns   | UseProfWD |
|      |     |        |         | in        | :         |
|      |     |        |         | [[#SUEWS_ | Anthro    |
|      |     |        |         | SiteSelec | pogenic   |
|      |     |        |         | t.txt     | heat      |
|      |     |        |         |           | flux,     |
|      |     |        |         |           | weekda    |
|      |     |        |         |           | ys        |
|      |     |        |         |           | -  Energy |
|      |     |        |         |           | UseProfWE |
|      |     |        |         |           | :         |
|      |     |        |         |           | Anthro    |
|      |     |        |         |           | pogenic   |
|      |     |        |         |           | heat      |
|      |     |        |         |           | flux,     |
|      |     |        |         |           | weeken    |
|      |     |        |         |           | ds        |
|      |     |        |         |           | -  WaterU |
|      |     |        |         |           | seProfMan |
|      |     |        |         |           | uWD       |
|      |     |        |         |           | :         |
|      |     |        |         |           | Manual    |
|      |     |        |         |           | irriga    |
|      |     |        |         |           | tion,     |
|      |     |        |         |           | weekda    |
|      |     |        |         |           | ys        |
|      |     |        |         |           | -  WaterU |
|      |     |        |         |           | seProfMan |
|      |     |        |         |           | uWE       |
|      |     |        |         |           | :         |
|      |     |        |         |           | Manual    |
|      |     |        |         |           | irriga    |
|      |     |        |         |           | tion,     |
|      |     |        |         |           | weeken    |
|      |     |        |         |           | ds        |
|      |     |        |         |           | -  WaterU |
|      |     |        |         |           | seProfAut |
|      |     |        |         |           | oWD       |
|      |     |        |         |           | :         |
|      |     |        |         |           | Automa    |
|      |     |        |         |           | tic       |
|      |     |        |         |           | irriga    |
|      |     |        |         |           | tion,     |
|      |     |        |         |           | weekda    |
|      |     |        |         |           | ys        |
|      |     |        |         |           | -  WaterU |
|      |     |        |         |           | seProfAut |
|      |     |        |         |           | oWE:      |
|      |     |        |         |           | Automa    |
|      |     |        |         |           | tic       |
|      |     |        |         |           | irriga    |
|      |     |        |         |           | tion,     |
|      |     |        |         |           | weeken    |
|      |     |        |         |           | ds        |
|      |     |        |         |           | -  SnowCl |
|      |     |        |         |           | earingPro |
|      |     |        |         |           | fWD       |
|      |     |        |         |           | : Snow    |
|      |     |        |         |           | cleari    |
|      |     |        |         |           | ng,       |
|      |     |        |         |           | weekda    |
|      |     |        |         |           | ys        |
|      |     |        |         |           | -  SnowCl |
|      |     |        |         |           | earingPro |
|      |     |        |         |           | fWE:      |
|      |     |        |         |           | Snow      |
|      |     |        |         |           | cleari    |
|      |     |        |         |           | ng,       |
|      |     |        |         |           | weeken    |
|      |     |        |         |           | ds        |
|      |     |        |         |           | -  Activi |
|      |     |        |         |           | tyProfWD: |
|      |     |        |         |           | Human     |
|      |     |        |         |           | activi    |
|      |     |        |         |           | ty,       |
|      |     |        |         |           | weekda    |
|      |     |        |         |           | ys        |
|      |     |        |         |           | -  Activi |
|      |     |        |         |           | tyProfWE: |
|      |     |        |         |           | Human     |
|      |     |        |         |           | activi    |
|      |     |        |         |           | ty,       |
|      |     |        |         |           | weeken    |
|      |     |        |         |           | ds        |
|      |     |        |         |           | -  Value  |
|      |     |        |         |           | of        |
|      |     |        |         |           | intege    |
|      |     |        |         |           | r         |
|      |     |        |         |           | is        |
|      |     |        |         |           | arbitr    |
|      |     |        |         |           | ary       |
|      |     |        |         |           | but       |
|      |     |        |         |           | must      |
|      |     |        |         |           | match     |
|      |     |        |         |           | codes     |
|      |     |        |         |           | specif    |
|      |     |        |         |           | ied       |
|      |     |        |         |           | in        |
|      |     |        |         |           | SUEWS_    |
|      |     |        |         |           | SiteSelec |
|      |     |        |         |           | t.txt.    |
+------+-----+--------+---------+-----------+-----------+
| 2-25 | MU  | 0-23   |         | Multiplie |           |
|      |     |        |         | r         |           |
|      |     |        |         | for each  |           |
|      |     |        |         | hour of   |           |
|      |     |        |         | the day   |           |
|      |     |        |         | [-] for   |           |
|      |     |        |         | energy    |           |
|      |     |        |         | and water |           |
|      |     |        |         | use. For  |           |
|      |     |        |         | SnowClear |           |
|      |     |        |         | ing,      |           |
|      |     |        |         | set those |           |
|      |     |        |         | hours to  |           |
|      |     |        |         | 1 when    |           |
|      |     |        |         | snow      |           |
|      |     |        |         | removal   |           |
|      |     |        |         | from      |           |
|      |     |        |         | paved and |           |
|      |     |        |         | roof      |           |
|      |     |        |         | surface   |           |
|      |     |        |         | is        |           |
|      |     |        |         | allowed   |           |
|      |     |        |         | (0        |           |
|      |     |        |         | otherwise |           |
|      |     |        |         | )         |           |
|      |     |        |         | if the    |           |
|      |     |        |         | snow      |           |
|      |     |        |         | removal   |           |
|      |     |        |         | limits    |           |
|      |     |        |         | set in    |           |
|      |     |        |         | the       |           |
|      |     |        |         | SUEWS_Non |           |
|      |     |        |         | Veg.txt   |           |
|      |     |        |         | (SnowLimR |           |
|      |     |        |         | emove     |           |
|      |     |        |         | column)   |           |
|      |     |        |         | are       |           |
|      |     |        |         | exceeded. |           |
+------+-----+--------+---------+-----------+-----------+