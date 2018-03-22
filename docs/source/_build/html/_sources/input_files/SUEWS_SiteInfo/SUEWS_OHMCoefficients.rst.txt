SUEWS_OHMCoefficients.txt
~~~~~~~~~~~~~~~~~~~~~~~~~

OHM, the Objective Hysteresis Model (Grimmond et al. 1991) [G91OHM]_
calculates the storage heat flux as a function of net all-wave radiation
and surface characteristics.

-  For each surface, OHM requires three model coefficients (a1, a2, a3).
   The three should be selected as a set.
-  The **SUEWS_OHMCoefficients.txt** file provides these coefficients
   for each surface type.
-  A variety of values has been derived for different materials and can
   be found in the literature (see:
   [http://urban-climate.net/umep/TypicalValues#OHM_Coefficients\ \|
   Typical Values]).
-  Coefficients can be changed depending on:

:# surface wetness state (wet/dry) based on the calculated surface
wetness state and soil moisture.

:# season (summer/winter) based on a 5-day running mean air temperature.

-  To use the same coefficients irrespective of wet/dry and
   summer/winter conditions, use the same code for all four OHM columns
   (OHMCode_SummerWet, OHMCode_SummerDry, OHMCode_WinterWet and
   OHMCode_WinterDry).

Note, **AnOHM** does not use the coefficients specified in
SUEWS_OHMCoefficients.txt but instead requires three parameters to be
specified for each surface type (including snow): heat capacity, thermal
conductivity and bulk transfer coefficient. These are specified in
`SUEWS_NonVeg.txt <#SUEWS_NonVeg.txt>`__,
`SUEWS_Veg.txt <#SUEWS_Veg.txt>`__,
`SUEWS_Water.txt <#SUEWS_Water.txt>`__ and
`SUEWS_Snow.txt <#SUEWS_Snow.txt>`__. No additional files are required
for AnOHM.

**Note AnOHM is under development in v2017a and should not be used!**

+-------------+-------------+-------------+-------------+-------------+
| No.         | Use         | Column name | Example     | Description |
+=============+=============+=============+=============+=============+
| 1           | L           | Code        | 331         | Code        |
|             |             |             |             | linking to  |
|             |             |             |             | the         |
|             |             |             |             | OHMCode_Sum |
|             |             |             |             | merWet,     |
|             |             |             |             | OHMCode_Sum |
|             |             |             |             | merDry,     |
|             |             |             |             | OHMCode_Win |
|             |             |             |             | terWet      |
|             |             |             |             | and         |
|             |             |             |             | OHMCode_Win |
|             |             |             |             | terDry      |
|             |             |             |             | columns in  |
|             |             |             |             | SUEWS_NonVe |
|             |             |             |             | g.txt,      |
|             |             |             |             | SUEWS_Veg,t |
|             |             |             |             | xt,         |
|             |             |             |             | SUEWS_Water |
|             |             |             |             | .txt        |
|             |             |             |             | and         |
|             |             |             |             | SUEWS_Snow. |
|             |             |             |             | txt         |
|             |             |             |             | files.      |
|             |             |             |             | Value of    |
|             |             |             |             | integer is  |
|             |             |             |             | arbitrary   |
|             |             |             |             | but must    |
|             |             |             |             | match code  |
|             |             |             |             | specified   |
|             |             |             |             | in          |
|             |             |             |             | SUEWS_SiteS |
|             |             |             |             | elect.txt.  |
+-------------+-------------+-------------+-------------+-------------+
| 2           | MU          | a1          |             | Coefficient |
|             |             |             |             | for Q\*     |
|             |             |             |             | term [-]    |
+-------------+-------------+-------------+-------------+-------------+
| 3           | MU          | a2          |             | Coefficient |
|             |             |             |             | for dQ*/dt  |
|             |             |             |             | term [h]    |
+-------------+-------------+-------------+-------------+-------------+
| 4           | MU          | a3          |             | Constant    |
|             |             |             |             | term [W     |
|             |             |             |             | m\ :sup:`-2 |
|             |             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+