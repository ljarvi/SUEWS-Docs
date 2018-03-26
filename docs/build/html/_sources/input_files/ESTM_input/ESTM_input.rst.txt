ESTM-related files
-----------------------------





SUEWS_ESTMCoefficients.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~

**Note ESTM is under development in v2017a and should not be used!**

The Element Surface Temperature Method (ESTM) (Offerle et al., 2005)
calculates the net storage heat flux from surface temperatures. In the
method the three-dimensional urban volume is reduced to four 1-d
elements (i.e. building roofs, walls, and internal mass and ground
(road, vegetation, etc)). The storage heat flux is calculated from the
heat conduction through the different elements. For the inside surfaces
of the roof and walls, and both surfaces for the internal mass
(ceilings/floors, internal walls), the surface temperature of the
element is determined by setting the conductive heat transfer out of (in
to) the surface equal to the radiative and convective heat losses
(gains). Each element (roof, wall, internal element and ground) can have
maximum five layers and each layer has three parameters tied to it:
thickness (x), thermal conductivity (k), volumetric heat capacity
(rhoCp).

If ESTM is used (QSchoice=4), the files
`SUEWS_ESTMCoefficients.txt <#SUEWS_ESTMCoefficients.txt>`__,
`ESTMinput.nml <#ESTMinput.nml>`__ and
`SS_YYYY_ESTM_Ts_data_tt.txt <#SS_YYYY_ESTM_Ts_data_tt.txt>`__ should be
prepared.

SUEWS_ESTMCoefficients.txt contains the parameters for the layers of
each of the elements (roofs, wall, ground, internal mass).

-  If less than five layers are used, the parameters for unused layers
   should be set to -999.
-  The ESTM coefficients with the prefix *Surf\_* must be specified for
   each surface type (plus snow) but the *Wall\_* and *Internal\_*
   variables apply to the building surfaces only.
-  For each grid, one set of ESTM coefficients must be specified for
   each surface type; for paved and building surfaces it is possible to
   specify up to three and five sets of coefficients per grid (e.g. to
   represent different building materials) using the relevant columns in
   `SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__. For the model to
   use these columns in site select, the ESTMCode column in
   `SUEWS_NonVeg.txt <#SUEWS_NonVeg.txt>`__ should be set to zero.

+-----+-----+-----------+---------+-----------+-----------+
| No. | Use | Column    | Example | Descripti |           |
|     |     | name      |         | on        |           |
+=====+=====+===========+=========+===========+===========+
| 1   | L   | Code      | 331     | Code      | SUEWS_Sit |
|     |     |           |         | linking   | eSelect.t |
|     |     |           |         | to the    | xt]]      |
|     |     |           |         | ESTMCode  | will be   |
|     |     |           |         | column in | used      |
|     |     |           |         | SUEWS_Non | instead.  |
|     |     |           |         | Veg.txt,  |           |
|     |     |           |         | SUEWS_Veg |           |
|     |     |           |         | ,txt,     |           |
|     |     |           |         | SUEWS_Wat |           |
|     |     |           |         | er.txt    |           |
|     |     |           |         | and       |           |
|     |     |           |         | SUEWS_Sno |           |
|     |     |           |         | w.txt     |           |
|     |     |           |         | files.    |           |
|     |     |           |         | \* For    |           |
|     |     |           |         | buildings |           |
|     |     |           |         | and paved |           |
|     |     |           |         | surfaces, |           |
|     |     |           |         | **set to  |           |
|     |     |           |         | zero** if |           |
|     |     |           |         | there is  |           |
|     |     |           |         | more than |           |
|     |     |           |         | one ESTM  |           |
|     |     |           |         | class per |           |
|     |     |           |         | grid and  |           |
|     |     |           |         | the codes |           |
|     |     |           |         | and       |           |
|     |     |           |         | surface   |           |
|     |     |           |         | fractions |           |
|     |     |           |         | specified |           |
|     |     |           |         | in        |           |
|     |     |           |         | [[#SUEWS_ |           |
|     |     |           |         | SiteSelec |           |
|     |     |           |         | t.txt     |           |
+-----+-----+-----------+---------+-----------+-----------+
| 2   | MU  | Surf_thic | 0.2     | Thickness |           |
|     |     | k1        |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | for roofs |           |
|     |     |           |         | (building |           |
|     |     |           |         | surfaces) |           |
|     |     |           |         | and       |           |
|     |     |           |         | ground    |           |
|     |     |           |         | (all      |           |
|     |     |           |         | other     |           |
|     |     |           |         | surfaces) |           |
+-----+-----+-----------+---------+-----------+-----------+
| 3   | MU  | Surf_k1   | 0.5     | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 4   | MU  | Surf_rhoC | 840000  | Volumetri |           |
|     |     | p1        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 5   | O   | Surf_thic | -       | Thickness |           |
|     |     | k2        |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 6   | O   | Surf_k2   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 7   | O   | Surf_rhoC | -       | Volumetri |           |
|     |     | p2        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 8   | O   | Surf_thic | -       | Thickness |           |
|     |     | k3        |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 9   | O   | Surf_k3   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer[W   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 10  | O   | Surf_rhoC | -       | Volumetri |           |
|     |     | p3        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer[J   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 11  | O   | Surf_thic | -       | Thickness |           |
|     |     | k4        |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 12  | O   | Surf_k4   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer[W   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 13  | O   | Surf_rhoC | -       | Volumetri |           |
|     |     | p4        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 14  | O   | Surf_thic | -       | Thickness |           |
|     |     | k5        |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 15  | O   | Surf_k5   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 16  | O   | Surf_rhoC | -       | Volumetri |           |
|     |     | p5        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 17  | MU  | Wall_thic | -       | Thickness |           |
|     |     | k1        |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | for       |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only; set |           |
|     |     |           |         | to -999   |           |
|     |     |           |         | for all   |           |
|     |     |           |         | other     |           |
|     |     |           |         | surfaces  |           |
+-----+-----+-----------+---------+-----------+-----------+
| 18  | MU  | Wall_k1   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 19  | MU  | Wall_rhoC | -       | Volumetri |           |
|     |     | p1        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 20  | O   | Wall_thic | -       | Thickness |           |
|     |     | k2        |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 21  | O   | Wall_k2   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 22  | O   | Wall_rhoC | -       | Volumetri |           |
|     |     | p2        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 23  | O   | Wall_thic | -       | Thickness |           |
|     |     | k3        |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 24  | O   | Wall_k3   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 25  | O   | Wall_rhoC | -       | Volumetri |           |
|     |     | p3        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 26  | O   | Wall_thic | -       | Thickness |           |
|     |     | k4        |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 27  | O   | Wall_k4   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer[W   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 28  | O   | Wall_rhoC | -       | Volumetri |           |
|     |     | p4        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 29  | O   | Wall_thic | -       | Thickness |           |
|     |     | k5        |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 30  | O   | Wall_k5   | -       | Thermal   |           |
|     |     |           |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer[W   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 31  | O   | Wall_rhoC | -       | Volumetri |           |
|     |     | p5        |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 32  | MU  | Internal_ | -       | Thickness |           |
|     |     | thick1    |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | for       |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only; set |           |
|     |     |           |         | to -999   |           |
|     |     |           |         | for all   |           |
|     |     |           |         | other     |           |
|     |     |           |         | surfaces  |           |
+-----+-----+-----------+---------+-----------+-----------+
| 33  | MU  | Internal_ | -       | Thermal   |           |
|     |     | k1        |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 34  | MU  | Internal_ | -       | Volumetri |           |
|     |     | rhoCp1    |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | first     |           |
|     |     |           |         | layer[J   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 35  | O   | Internal_ | -       | Thickness |           |
|     |     | thick2    |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 36  | O   | Internal_ | -       | Thermal   |           |
|     |     | k2        |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 37  | O   | Internal_ | -       | Volumetri |           |
|     |     | rhoCp2    |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | second    |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 38  | O   | Internal_ | -       | Thickness |           |
|     |     | thick3    |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 39  | O   | Internal_ | -       | Thermal   |           |
|     |     | k3        |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 40  | O   | Internal_ | -       | Volumetri |           |
|     |     | rhoCp3    |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | third     |           |
|     |     |           |         | layer[J   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 41  | O   | Internal_ | -       | Thickness |           |
|     |     | thick4    |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 42  | O   | Internal_ | -       | Thermal   |           |
|     |     | k4        |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 43  | O   | Internal_ | -       | Volumetri |           |
|     |     | rhoCp4    |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fourth    |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 44  | O   | Internal_ | -       | Thickness |           |
|     |     | thick5    |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [m] |           |
|     |     |           |         | (if no    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer,    |           |
|     |     |           |         | set to    |           |
|     |     |           |         | -999.)    |           |
+-----+-----+-----------+---------+-----------+-----------+
| 45  | O   | Internal_ | -       | Thermal   |           |
|     |     | k5        |         | conductiv |           |
|     |     |           |         | ity       |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [W  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -1`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 46  | O   | Internal_ | -       | Volumetri |           |
|     |     | rhoCp5    |         | c         |           |
|     |     |           |         | heat      |           |
|     |     |           |         | capacity  |           |
|     |     |           |         | of the    |           |
|     |     |           |         | fifth     |           |
|     |     |           |         | layer [J  |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -3`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 47  | MU  | nroom     | -       | Number of |           |
|     |     |           |         | rooms per |           |
|     |     |           |         | floor for |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 48  | MU  | Internal_ | -       | Albedo of |           |
|     |     | albedo    |         | all       |           |
|     |     |           |         | internal  |           |
|     |     |           |         | elements  |           |
|     |     |           |         | for       |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 49  | MU  | Internal_ | -       | Emissivit |           |
|     |     | emissivit |         | y         |           |
|     |     | y         |         | of all    |           |
|     |     |           |         | internal  |           |
|     |     |           |         | elements  |           |
|     |     |           |         | for       |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only      |           |
+-----+-----+-----------+---------+-----------+-----------+
| 50  | O   | Internal_ |         | Bulk      | ESTMinput |
|     |     | CHwall    |         | transfer  | .nml]]    |
|     |     |           |         | coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | of        |           |
|     |     |           |         | internal  |           |
|     |     |           |         | wall [W   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -2`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
|     |     |           |         | (for      |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only and  |           |
|     |     |           |         | if        |           |
|     |     |           |         | IbldCHmod |           |
|     |     |           |         | == 0 in   |           |
|     |     |           |         | [[#ESTMin |           |
|     |     |           |         | put.nml   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 51  | O   | Internal_ |         | Bulk      | ESTMinput |
|     |     | CHroof    |         | transfer  | .nml]]    |
|     |     |           |         | coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | of        |           |
|     |     |           |         | internal  |           |
|     |     |           |         | roof [W   |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -2`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
|     |     |           |         | (for      |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only and  |           |
|     |     |           |         | if        |           |
|     |     |           |         | IbldCHmod |           |
|     |     |           |         | == 0 in   |           |
|     |     |           |         | [[#ESTMin |           |
|     |     |           |         | put.nml   |           |
+-----+-----+-----------+---------+-----------+-----------+
| 52  | O   | Internal_ |         | Bulk      | ESTMinput |
|     |     | CHbld     |         | transfer  | .nml]]    |
|     |     |           |         | coefficie |           |
|     |     |           |         | nt        |           |
|     |     |           |         | of        |           |
|     |     |           |         | internal  |           |
|     |     |           |         | building  |           |
|     |     |           |         | elements  |           |
|     |     |           |         | [W        |           |
|     |     |           |         | m\ :sup:` |           |
|     |     |           |         | -2`       |           |
|     |     |           |         | K\ :sup:` |           |
|     |     |           |         | -1`]      |           |
|     |     |           |         | (for      |           |
|     |     |           |         | building  |           |
|     |     |           |         | surfaces  |           |
|     |     |           |         | only and  |           |
|     |     |           |         | if        |           |
|     |     |           |         | IbldCHmod |           |
|     |     |           |         | == 0 in   |           |
|     |     |           |         | [[#ESTMin |           |
|     |     |           |         | put.nml   |           |
+-----+-----+-----------+---------+-----------+-----------+





**Note ESTM is under development in v2017a and should not be used!**

The following input files are required if ESTM is used to calculate the
storage heat flux.

ESTMinput.nml
~~~~~~~~~~~~~

ESTMinput.nml specifies the model settings and default values.

-  The file contents can be in any order.

+-------------+-----------------------+-----------------------+
| Name        | Description           |                       |
+=============+=======================+=======================+
|             |                       |                       |
+-------------+-----------------------+-----------------------+
| TsurfChoice | Source of surface     |                       |
|             | temperature data      |                       |
|             | used.                 |                       |
+-------------+-----------------------+-----------------------+
| 0           | \*Tsurf in            | SSss_YYYY_ESTM_Ts_dat |
|             | [[#SSss_YYYY_ESTM_Ts_ | a_tt.txt]]            |
|             | data_tt.txt           | used for **all**      |
|             |                       | surface elements.     |
+-------------+-----------------------+-----------------------+
| 1           | \*Tground, Troof and  | SSss_YYYY_ESTM_Ts_dat |
|             | Twall in              | a_tt.txt]]            |
|             | [[#SSss_YYYY_ESTM_Ts_ | used.                 |
|             | data_tt.txt           | -  Input surface      |
|             |                       | temperature are       |
|             |                       | different for         |
|             |                       | ground, roof and      |
|             |                       | wall.                 |
+-------------+-----------------------+-----------------------+
| 2           | \*Tground, Troof,     | SSss_YYYY_ESTM_Ts_dat |
|             | Twall_n, Twall_e,     | a_tt.txt]]            |
|             | Twall_s and Twall_w   | used.                 |
|             | in                    | -  Wall surface       |
|             | [[#SSss_YYYY_ESTM_Ts_ | temperature is        |
|             | data_tt.txt           | different for four    |
|             |                       | directions.           |
+-------------+-----------------------+-----------------------+
| evolveTibld | Source of internal    |                       |
|             | building temperature  |                       |
|             | (Tibld)               |                       |
+-------------+-----------------------+-----------------------+
| 0           | \*Tiair in            | SSss_YYYY_ESTM_Ts_dat |
|             | [[#SSss_YYYY_ESTM_Ts_ | a_tt.txt]]            |
|             | data_tt.txt           | used.                 |
+-------------+-----------------------+-----------------------+
| 1           | \*Tibld calculated    |                       |
|             | considering the       |                       |
|             | effect of             |                       |
|             | anthropogenic heat    |                       |
|             | from HVAC             |                       |
+-------------+-----------------------+-----------------------+
| 2           | \*Tibld calculated    |                       |
|             | without considering   |                       |
|             | the influence of      |                       |
|             | HVAC.                 |                       |
+-------------+-----------------------+-----------------------+
| IbldCHmod   | Method to calculate   |                       |
|             | internal convective   |                       |
|             | heat exchange         |                       |
|             | coefficients (CH) for |                       |
|             | internal building,    |                       |
|             | wall and roof if      |                       |
|             | evolveTibld is 1 or   |                       |
|             | 2.                    |                       |
+-------------+-----------------------+-----------------------+
| 0           | CHs are read from     |                       |
|             | SUEWS_ESTMcoefficient |                       |
|             | s.txt.                |                       |
+-------------+-----------------------+-----------------------+
| 1           | CHs are calculated    |                       |
|             | based on ASHRAE       |                       |
|             | (2001)                |                       |
+-------------+-----------------------+-----------------------+
| 2           | CHs are calculated    |                       |
|             | based on Awbi (1998). |                       |
+-------------+-----------------------+-----------------------+
| LBC_soil    | Soil temperature at   |                       |
|             | lowest boundary       |                       |
|             | condition [˚C]        |                       |
+-------------+-----------------------+-----------------------+
| Theat_on    | Temperature at which  |                       |
|             | heat control is       |                       |
|             | turned on (used when  |                       |
|             | evolveTibld =1) [˚C]  |                       |
+-------------+-----------------------+-----------------------+
| Theat_off   | Temperature at which  |                       |
|             | heat control is       |                       |
|             | turned off (used when |                       |
|             | evolveTibld=1) [˚C]   |                       |
+-------------+-----------------------+-----------------------+
| Theat_fix   | Ideal internal        |                       |
|             | building temperature  |                       |
|             | [˚C]                  |                       |
+-------------+-----------------------+-----------------------+
|             |                       |                       |
+-------------+-----------------------+-----------------------+

SSss_YYYY_ESTM_Ts_data_tt.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

SSss_YYYY_ESTM_Ts_data_tt.txt contains a time-series of input surface
temperature for roof, wall, ground and internal elements.

+-----------------------+-----------------------+-----------------------+
| No.                   | Column name           | Description           |
+=======================+=======================+=======================+
| 1                     | iy                    | Year [YYYY]           |
+-----------------------+-----------------------+-----------------------+
| 2                     | id                    | Day of year [DOY]     |
+-----------------------+-----------------------+-----------------------+
| 3                     | it                    | Hour [H]              |
+-----------------------+-----------------------+-----------------------+
| 4                     | imin                  | Minute [M]            |
+-----------------------+-----------------------+-----------------------+
| 5                     | Tiair                 | Indoor air            |
|                       |                       | temperature [˚C]      |
+-----------------------+-----------------------+-----------------------+
| 6                     | Tsurf                 | Bulk surface          |
|                       |                       | temperature [˚C]      |
|                       |                       | (used when TsurfCoice |
|                       |                       | = 0)                  |
+-----------------------+-----------------------+-----------------------+
| 7                     | Troof                 | Roof surface          |
|                       |                       | temperature [˚C]      |
|                       |                       | (used when            |
|                       |                       | TsurfChoice = 1 or 2) |
+-----------------------+-----------------------+-----------------------+
| 8                     | Troad                 | Ground surface        |
|                       |                       | temperature [˚C]      |
|                       |                       | (used when            |
|                       |                       | TsurfChoice = 1 or 2) |
+-----------------------+-----------------------+-----------------------+
| 9                     | Twall                 | Wall surface          |
|                       |                       | temperature [˚C]      |
|                       |                       | (used when            |
|                       |                       | TsurfChoice = 1)      |
+-----------------------+-----------------------+-----------------------+
| 10                    | Twall_n               | North-facing wall     |
|                       |                       | surface temperature   |
|                       |                       | [˚C] (used when       |
|                       |                       | TsurfChoice = 2)      |
+-----------------------+-----------------------+-----------------------+
| 11                    | Twall_e               | East-facing wall      |
|                       |                       | surface temperature   |
|                       |                       | [˚C] (used when       |
|                       |                       | TsurfChoice = 2)      |
+-----------------------+-----------------------+-----------------------+
| 12                    | Twall_s               | South-facing wall     |
|                       |                       | surface temperature   |
|                       |                       | [˚C] (used when       |
|                       |                       | TsurfChoice = 2)      |
+-----------------------+-----------------------+-----------------------+
| 13                    | Twall_w               | West-facing wall      |
|                       |                       | surface temperature   |
|                       |                       | [˚C] (used when       |
|                       |                       | TsurfChoice = 2)      |
+-----------------------+-----------------------+-----------------------+








