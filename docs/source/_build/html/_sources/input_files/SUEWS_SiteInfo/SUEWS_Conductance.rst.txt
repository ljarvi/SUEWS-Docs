SUEWS_Conductance.txt
~~~~~~~~~~~~~~~~~~~~~

SUEWS_Conductance.txt contains the parameters needed for the Jarvis
(1976) surface conductance model used in the modelling of evaporation in
SUEWS. These values should **not** be changed independently of each
other. The suggested values below have been derived using datasets for
Los Angeles and Vancouver (see Järvi et al. (2011) [J11]_) and should be
used with **gsModel=1**. An alternative formulation (gsModel=2) uses
slightly different functional forms and different coefficients (with
different units).

+-----+-----+---------+----------+-----------+-----------+
| No. | Use | Column  | Example  | Descripti |           |
|     |     | name    |          | on        |           |
+=====+=====+=========+==========+===========+===========+
| 1   | L   | Code    |          | Code      | SUEWS_Sit |
|     |     |         |          | linking   | eSelect.t |
|     |     |         |          | to the    | xt]].     |
|     |     |         |          | CondCode  | Value of  |
|     |     |         |          | column in | integer   |
|     |     |         |          | [[#SUEWS_ | is        |
|     |     |         |          | SiteSelec | arbitrary |
|     |     |         |          | t.txt     | but must  |
|     |     |         |          |           | match     |
|     |     |         |          |           | code      |
|     |     |         |          |           | specified |
|     |     |         |          |           | in        |
|     |     |         |          |           | SUEWS_Sit |
|     |     |         |          |           | eSelect.t |
|     |     |         |          |           | xt.       |
+-----+-----+---------+----------+-----------+-----------+
| 2   | MD  | G1      | 16.4764  | Related   |           |
|     |     |         |          | to        |           |
|     |     |         |          | maximum   |           |
|     |     |         |          | surface   |           |
|     |     |         |          | conductan |           |
|     |     |         |          | ce        |           |
|     |     |         |          | [mm       |           |
|     |     |         |          | s\ :sup:` |           |
|     |     |         |          | -1`]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 3   | MD  | G2      | 566.0923 | Related   |           |
|     |     |         |          | to Kdown  |           |
|     |     |         |          | dependenc |           |
|     |     |         |          | e         |           |
|     |     |         |          | [W        |           |
|     |     |         |          | m\ :sup:` |           |
|     |     |         |          | -2`]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 4   | MD  | G3      | 0.2163   | Related   | RunContro |
|     |     |         |          | to VPD    | l.nml]]   |
|     |     |         |          | dependenc | ]         |
|     |     |         |          | e         |           |
|     |     |         |          | [units    |           |
|     |     |         |          | depend on |           |
|     |     |         |          | gsChoice  |           |
|     |     |         |          | in        |           |
|     |     |         |          | [[#RunCon |           |
|     |     |         |          | trol.nml  |           |
+-----+-----+---------+----------+-----------+-----------+
| 5   | MD  | G4      | 3.3649   | Related   | RunContro |
|     |     |         |          | to VPD    | l.nml]]   |
|     |     |         |          | dependenc | ]         |
|     |     |         |          | e         |           |
|     |     |         |          | [units    |           |
|     |     |         |          | depend on |           |
|     |     |         |          | gsChoice  |           |
|     |     |         |          | in        |           |
|     |     |         |          | [[#RunCon |           |
|     |     |         |          | trol.nml  |           |
+-----+-----+---------+----------+-----------+-----------+
| 6   | MD  | G5      | 11.0764  | Related   |           |
|     |     |         |          | to        |           |
|     |     |         |          | temperatu |           |
|     |     |         |          | re        |           |
|     |     |         |          | dependenc |           |
|     |     |         |          | e         |           |
|     |     |         |          | [°C]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 7   | MD  | G6      | 0.0176   | Related   |           |
|     |     |         |          | to soil   |           |
|     |     |         |          | moisture  |           |
|     |     |         |          | dependenc |           |
|     |     |         |          | e         |           |
|     |     |         |          | [mm:sup:` |           |
|     |     |         |          | -1`]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 8   | MD  | TH      | 40       | Upper air |           |
|     |     |         |          | temperatu |           |
|     |     |         |          | re        |           |
|     |     |         |          | limit     |           |
|     |     |         |          | [°C]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 9   | MD  | TL      | 0        | Lower air |           |
|     |     |         |          | temperatu |           |
|     |     |         |          | re        |           |
|     |     |         |          | limit     |           |
|     |     |         |          | [°C]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 10  | MD  | S1      | 0.45     | Related   |           |
|     |     |         |          | to soil   |           |
|     |     |         |          | moisture  |           |
|     |     |         |          | dependenc |           |
|     |     |         |          | e         |           |
|     |     |         |          | [-]       |           |
|     |     |         |          | *These    |           |
|     |     |         |          | will      |           |
|     |     |         |          | change in |           |
|     |     |         |          | the       |           |
|     |     |         |          | future to |           |
|     |     |         |          | ensure    |           |
|     |     |         |          | consisten |           |
|     |     |         |          | cy        |           |
|     |     |         |          | with soil |           |
|     |     |         |          | behaviour |           |
|     |     |         |          | *         |           |
+-----+-----+---------+----------+-----------+-----------+
| 11  | MD  | S2      | 15       | Related   |           |
|     |     |         |          | to soil   |           |
|     |     |         |          | moisture  |           |
|     |     |         |          | dependenc |           |
|     |     |         |          | e         |           |
|     |     |         |          | [mm]      |           |
|     |     |         |          | *These    |           |
|     |     |         |          | will      |           |
|     |     |         |          | change in |           |
|     |     |         |          | the       |           |
|     |     |         |          | future to |           |
|     |     |         |          | ensure    |           |
|     |     |         |          | consisten |           |
|     |     |         |          | cy        |           |
|     |     |         |          | with soil |           |
|     |     |         |          | behaviour |           |
|     |     |         |          | *         |           |
+-----+-----+---------+----------+-----------+-----------+
| 12  | MD  | Kmax    | 1200     | Maximum   |           |
|     |     |         |          | incoming  |           |
|     |     |         |          | shortwave |           |
|     |     |         |          | radiation |           |
|     |     |         |          | [W        |           |
|     |     |         |          | m\ :sup:` |           |
|     |     |         |          | -2`]      |           |
+-----+-----+---------+----------+-----------+-----------+
| 13  | MD  | gsModel | 1        | Determine |           |
|     |     |         |          | s         |           |
|     |     |         |          | which     |           |
|     |     |         |          | surface   |           |
|     |     |         |          | conductan |           |
|     |     |         |          | ce        |           |
|     |     |         |          | parameter |           |
|     |     |         |          | isation   |           |
|     |     |         |          | to use    |           |
|     |     |         |          | -  1 =    |           |
|     |     |         |          | Järvi     |           |
|     |     |         |          | et al.    |           |
|     |     |         |          | (2011)    |           |
|     |     |         |          | [J11]_    |           |
|     |     |         |          | -  2 =    |           |
|     |     |         |          | Ward      |           |
|     |     |         |          | et al.    |           |
|     |     |         |          | (2016)    |           |
|     |     |         |          | [W16]_    |           |
|     |     |         |          | **Reco    |           |
|     |     |         |          | mmended.* |           |
|     |     |         |          | *         |           |
|     |     |         |          | **The     |           |
|     |     |         |          | parameter |           |
|     |     |         |          | isation   |           |
|     |     |         |          | specified |           |
|     |     |         |          | here must |           |
|     |     |         |          | match the |           |
|     |     |         |          | coefficie |           |
|     |     |         |          | nts       |           |
|     |     |         |          | specified |           |
|     |     |         |          | in the    |           |
|     |     |         |          | other     |           |
|     |     |         |          | columns   |           |
|     |     |         |          | of        |           |
|     |     |         |          | SUEWS_Con |           |
|     |     |         |          | ductance. |           |
|     |     |         |          | txt.**    |           |
+-----+-----+---------+----------+-----------+-----------+