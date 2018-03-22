SUEWS_Soil.txt
~~~~~~~~~~~~~~

SUEWS_Soil.txt specifies the characteristics of the sub-surface soil
below each of the non-water surface types (Paved, Bldgs, EveTr, DecTr,
Grass, BSoil). The model does not have a soi store below the water
surfaces. Note that these sub-surface soil stores are different to the
bare soil/unmamnaged surface cover type. Each of the non-water surface
types need to link to soil characteristics specified here. If the soil
characteristics are assumed to be the same for all surface types, use a
single code value to link the characteristics here with the SoilTypeCode
columns in `SUEWS_NonVeg.txt <#SUEWS_NonVeg.txt>`__ and
`SUEWS_Veg.txt <#SUEWS_Veg.txt>`__.

Soil moisture can either be provided using observational data in the met
forcing file (smd_choice = 1 or 2 in
`RunControl.nml <#RunControl.nml>`__) and providing some metadata
information here (OBS\_ columns), or modelled by SUEWS (smd_choice = 0
in `RunControl.nml <#RunControl.nml>`__). **- Note, the option to use
observational data is not operational in the current release!**

+-------------+-------------+-------------+-------------+-------------+
| No.         | Use         | Column name | Example     | Description |
+=============+=============+=============+=============+=============+
| 1           | L           | Code        | 331         | Code        |
|             |             |             |             | linking to  |
|             |             |             |             | the         |
|             |             |             |             | SoilTypeCod |
|             |             |             |             | e           |
|             |             |             |             | column in   |
|             |             |             |             | SUEWS_NonVe |
|             |             |             |             | g.txt       |
|             |             |             |             | (for Paved, |
|             |             |             |             | Bldgs and   |
|             |             |             |             | BSoil       |
|             |             |             |             | surfaces)   |
|             |             |             |             | and         |
|             |             |             |             | SUEWS_Veg.t |
|             |             |             |             | xt          |
|             |             |             |             | (for EveTr, |
|             |             |             |             | DecTr and   |
|             |             |             |             | Grass       |
|             |             |             |             | surfaces).  |
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
| 2           | MD          | SoilDepth   | 350         | Depth of    |
|             |             |             |             | sub-surface |
|             |             |             |             | soil store  |
|             |             |             |             | [mm] i.e.   |
|             |             |             |             | the depth   |
|             |             |             |             | of soil     |
|             |             |             |             | beneath the |
|             |             |             |             | surface     |
+-------------+-------------+-------------+-------------+-------------+
| 3           | MD          | SoilStoreCa | 150         | Capacity of |
|             |             | p           |             | sub-surface |
|             |             |             |             | soil store  |
|             |             |             |             | [mm] i.e.   |
|             |             |             |             | how much    |
|             |             |             |             | water can   |
|             |             |             |             | be stored   |
|             |             |             |             | in the      |
|             |             |             |             | sub-surface |
|             |             |             |             | soil when   |
|             |             |             |             | at maximum  |
|             |             |             |             | capacity.   |
|             |             |             |             |             |
|             |             |             |             | -  SoilStor |
|             |             |             |             | eCap        |
|             |             |             |             |    must not |
|             |             |             |             |    be       |
|             |             |             |             |    greater  |
|             |             |             |             |    than     |
|             |             |             |             |    SoilDept |
|             |             |             |             | h.          |
+-------------+-------------+-------------+-------------+-------------+
| 4           | MD          | SatHydrauli | 0.0005      | Hydraulic   |
|             |             | cCond       |             | conductivit |
|             |             |             |             | y           |
|             |             |             |             | for         |
|             |             |             |             | saturated   |
|             |             |             |             | soil [mm    |
|             |             |             |             | s\ :sup:`-1 |
|             |             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 5           | MD          | SoilDensity | 1.16        | Soil        |
|             |             |             |             | density [kg |
|             |             |             |             | m\ :sup:`-3 |
|             |             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 6           | O           | Infiltratio | -999        | Infiltratio |
|             |             | nRate       |             | n           |
|             |             |             |             | rate [mm    |
|             |             |             |             | h\ :sup:`-1 |
|             |             |             |             | `]          |
|             |             |             |             |             |
|             |             |             |             | -  Not      |
|             |             |             |             |    currentl |
|             |             |             |             | y           |
|             |             |             |             |    used     |
+-------------+-------------+-------------+-------------+-------------+
| 7           | O           | OBS_SMDepth |             | Depth of    |
|             |             |             |             | soil        |
|             |             |             |             | moisture    |
|             |             |             |             | measurement |
|             |             |             |             | s           |
|             |             |             |             | [mm]        |
|             |             |             |             |             |
|             |             |             |             | -  Use only |
|             |             |             |             |    if soil  |
|             |             |             |             |    moisture |
|             |             |             |             |    is       |
|             |             |             |             |    observed |
|             |             |             |             |    and      |
|             |             |             |             |    provided |
|             |             |             |             |    in the   |
|             |             |             |             |    met      |
|             |             |             |             |    forcing  |
|             |             |             |             |    file and |
|             |             |             |             |    smd_choi |
|             |             |             |             | ce          |
|             |             |             |             |    = 1 or   |
|             |             |             |             |    2.       |
|             |             |             |             | -  **Use of |
|             |             |             |             |    observed |
|             |             |             |             |    soil     |
|             |             |             |             |    moisture |
|             |             |             |             |    not      |
|             |             |             |             |    currentl |
|             |             |             |             | y           |
|             |             |             |             |    tested** |
+-------------+-------------+-------------+-------------+-------------+
| 8           | O           | OBS_SMCap   |             | Maxiumum    |
|             |             |             |             | observed    |
|             |             |             |             | soil        |
|             |             |             |             | moisture    |
|             |             |             |             | [m:sup:`3`  |
|             |             |             |             | m\ :sup:`-3 |
|             |             |             |             | `           |
|             |             |             |             | or kg       |
|             |             |             |             | kg\ :sup:`- |
|             |             |             |             | 1`]         |
|             |             |             |             |             |
|             |             |             |             | -  Use only |
|             |             |             |             |    if soil  |
|             |             |             |             |    moisture |
|             |             |             |             |    is       |
|             |             |             |             |    observed |
|             |             |             |             |    and      |
|             |             |             |             |    provided |
|             |             |             |             |    in the   |
|             |             |             |             |    met      |
|             |             |             |             |    forcing  |
|             |             |             |             |    file and |
|             |             |             |             |    smd_choi |
|             |             |             |             | ce          |
|             |             |             |             |    = 1 or   |
|             |             |             |             |    2.       |
|             |             |             |             | -  **Use of |
|             |             |             |             |    observed |
|             |             |             |             |    soil     |
|             |             |             |             |    moisture |
|             |             |             |             |    not      |
|             |             |             |             |    currentl |
|             |             |             |             | y           |
|             |             |             |             |    tested** |
+-------------+-------------+-------------+-------------+-------------+
| 9           | O           | OBS_SoilNot |             | Fraction of |
|             |             | Rocks       |             | soil        |
|             |             |             |             | without     |
|             |             |             |             | rocks [-]   |
|             |             |             |             |             |
|             |             |             |             | -  Use only |
|             |             |             |             |    if soil  |
|             |             |             |             |    moisture |
|             |             |             |             |    is       |
|             |             |             |             |    observed |
|             |             |             |             |    and      |
|             |             |             |             |    provided |
|             |             |             |             |    in the   |
|             |             |             |             |    met      |
|             |             |             |             |    forcing  |
|             |             |             |             |    file and |
|             |             |             |             |    smd_choi |
|             |             |             |             | ce          |
|             |             |             |             |    = 1 or   |
|             |             |             |             |    2.       |
|             |             |             |             | -  **Use of |
|             |             |             |             |    observed |
|             |             |             |             |    soil     |
|             |             |             |             |    moisture |
|             |             |             |             |    not      |
|             |             |             |             |    currentl |
|             |             |             |             | y           |
|             |             |             |             |    tested** |
+-------------+-------------+-------------+-------------+-------------+