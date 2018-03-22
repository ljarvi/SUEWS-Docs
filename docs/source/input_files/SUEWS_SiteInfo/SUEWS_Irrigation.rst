SUEWS_Irrigation.txt
~~~~~~~~~~~~~~~~~~~~

SUEWS includes a simple model for external water use if observed data
are not available. The model calculates daily water use from the mean
daily air temperature, number of days since rain and fraction of
irrigated area using automatic/manual irrigation. The sub-daily pattern
of water use is modelled according to the daily cycles specified in
`SUEWS_Profiles.txt <#SUEWS_Profiles.txt>`__.

Alternatively, if available, the external water use can be provided in
the met forcing file (and set WaterUseMethod = 1 in
`RunControl.nml <#RunControl.nml>`__), in which case all columns here
except Code should be set to '-999'.

+-----+-----+-----------+---------+-----------+-----------+
| No. | Use | Column    | Example | Descripti |           |
|     |     | name      |         | on        |           |
+=====+=====+===========+=========+===========+===========+
| 1   | L   | Code      |         | Code      | SUEWS_Sit |
|     |     |           |         | linking   | eSelect.t |
|     |     |           |         | to        | xt]       |
|     |     |           |         | [[#SUEWS_ | for       |
|     |     |           |         | SiteSelec | irrigatio |
|     |     |           |         | t.txt     | n         |
|     |     |           |         |           | modelling |
|     |     |           |         |           | (Irrigati |
|     |     |           |         |           | onCode).  |
|     |     |           |         |           | Value of  |
|     |     |           |         |           | integer   |
|     |     |           |         |           | is        |
|     |     |           |         |           | arbitrary |
|     |     |           |         |           | but must  |
|     |     |           |         |           | match     |
|     |     |           |         |           | codes     |
|     |     |           |         |           | specified |
|     |     |           |         |           | in        |
|     |     |           |         |           | SUEWS_Sit |
|     |     |           |         |           | eSelect.t |
|     |     |           |         |           | xt.       |
+-----+-----+-----------+---------+-----------+-----------+
| 2   | MU  | Ie_start  | 1-366   | Day when  |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | starts    |           |
|     |     |           |         | [DOY]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 3   | MU  | Ie_end    | 1-366   | Day when  |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | ends      |           |
|     |     |           |         | [DOY]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 4   | MU  | InternalW | 0       | Internal  |           |
|     |     | aterUse   |         | water use |           |
|     |     |           |         | [mm       |           |
|     |     |           |         | h\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 5   | MU  | Faut      | 0-1     | Fraction  |           |
|     |     |           |         | of        |           |
|     |     |           |         | irrigated |           |
|     |     |           |         | area that |           |
|     |     |           |         | is        |           |
|     |     |           |         | irrigated |           |
|     |     |           |         | using     |           |
|     |     |           |         | automated |           |
|     |     |           |         | systems   |           |
|     |     |           |         | (e.g.     |           |
|     |     |           |         | sprinkler |           |
|     |     |           |         | s).       |           |
+-----+-----+-----------+---------+-----------+-----------+
| 6   | MD  | Ie_a1     | -84.54  | Coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | for       |           |
|     |     |           |         | automatic |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | model [mm |           |
|     |     |           |         | d\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 7   | MD  | Ie_a2     | 9.96    | Coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | for       |           |
|     |     |           |         | automatic |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | model [mm |           |
|     |     |           |         | d\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | °C\ :sup: |           |
|     |     |           |         | `-1`]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 8   | MD  | Ie_a3     | 3.67    | Coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | for       |           |
|     |     |           |         | automatic |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | model [mm |           |
|     |     |           |         | d\ :sup:` |           |
|     |     |           |         | -2`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 9   | MD  | Ie_m1     | -25.36  | Coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | for       |           |
|     |     |           |         | manual    |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | model [mm |           |
|     |     |           |         | d\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 10  | MD  | Ie_m2     | 3.00    | Coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | for       |           |
|     |     |           |         | manual    |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | model [mm |           |
|     |     |           |         | d\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | °C\ :sup: |           |
|     |     |           |         | `-1`]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 11  | MD  | Ie_m3     | 1.10    | Coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | for       |           |
|     |     |           |         | manual    |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | model [mm |           |
|     |     |           |         | d\ :sup:` |           |
|     |     |           |         | -2`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 12  | MU  | DayWat(1) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Sundays   |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 13  | MU  | DayWat(2) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Mondays   |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 14  | MU  | DayWat(3) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Tuesdays  |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 15  | MU  | DayWat(4) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Wednesday |           |
|     |     |           |         | s         |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 16  | MU  | DayWat(5) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Thursdays |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 17  | MU  | DayWat(6) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Fridays   |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 18  | MU  | DayWat(7) | 0 or 1  | Irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | allowed   |           |
|     |     |           |         | on        |           |
|     |     |           |         | Saturdays |           |
|     |     |           |         | [J11], if |           |
|     |     |           |         | not [0]   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 19  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (1)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Sundays   |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 20  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (2)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Mondays   |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 21  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (3)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Tuesdays  |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 22  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (4)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Wednesday |           |
|     |     |           |         | s         |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 23  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (5)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Thursdays |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 24  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (6)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Fridays   |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 25  | MU  | DayWatPer | 0-1     | Fraction  |           |
|     |     | (7)       |         | of        |           |
|     |     |           |         | propertie |           |
|     |     |           |         | s         |           |
|     |     |           |         | using     |           |
|     |     |           |         | irrigatio |           |
|     |     |           |         | n         |           |
|     |     |           |         | on        |           |
|     |     |           |         | Saturdays |           |
|     |     |           |         | [0-1]     |           |
+-----+-----+-----------+---------+-----------+-----------+