Output files
============


Error messages: problems.txt
----------------------------

If there are problems running the program serious error messages will be
written to problems.txt.

-  Serious problems will usually cause the program to stop after writing
   the error message. If this is the case, the last line of problems.txt
   will contain a non-zero number (the error code).
-  If the program runs successfully, problems.txt file ends with

| ``Run completed.``
| ``0``

SUEWS has a large number of error messages included to try to capture
common errors to help the user determine what the problem is. If you
encounter an error that does not provide an error message please capture
the details so we can hopefully provide better error messages in future.

See `Troubleshooting <#Troubleshooting>`__ section for help solving
problems. If the file paths are not correct the program will return an
error when run (see `Preparing to run the
model <#Preparing_to_run_the_model>`__).

Error messages: warnings.txt
----------------------------

-  If the program encounters a more minor issue it will not stop but a
   warning may be written to warnings.txt. It is advisable to check the
   warnings to ensure there is not a more serious problem.
-  The warnings.txt file can be large (over several GBs) given warning
   messages are written out during a large scale simulation, you can use
   ``tail``/``head`` to view the ending/starting part without opening
   the whole file on Unix-like systems (Linux/mac OS), which may slow
   down your system.
-  To prevent warnings.txt from being written, set **SuppressWarnings**
   to 1 in `RunControl.nml <#RunControl.nml>`__.
-  Warning messages are usually written with a grid number, timestamp
   and error count. If the problem occurs in the initial stages (i.e.
   before grid numbers and timestamps are assigned, these are printed as
   00000).

Summary of model parameters: SS_FileChoices.txt
-----------------------------------------------

For each run, the model parameters specified in the input files are
written out to the file SS_FileChoices.txt.

Model output files
------------------

SSss_YYYY_TT.txt
~~~~~~~~~~~~~~~~

SUEWS produces the main output file (SSss_YYYY_tt.txt) with time
resolution (TT min) set by **ResolutionFilesOut** in
`RunControl <#RunControl>`__.

Before these main data files are written out, SUEWS provides a summary
of the column names, units and variables included in the file
Ss_YYYY_TT_OutputFormat.txt (one file per run).

The variables included in the main output file are determined according
to **WriteOutOption** set in `RunControl.nml <#RunControl.nml>`__.

+-------------+-------------+-------------+-------------+-------------+
| Column      | Name        | WriteOutOpt | Description |
|             |             | ion         |             |
+=============+=============+=============+=============+
| 1           | Year        | 0,1,2       | Year [YYYY] |
+-------------+-------------+-------------+-------------+-------------+
| 2           | DOY         | 0,1,2       | Day of year |
|             |             |             | [DOY]       |
+-------------+-------------+-------------+-------------+-------------+
| 3           | Hour        | 0,1,2       | Hour [H]    |
+-------------+-------------+-------------+-------------+-------------+
| 4           | Min         | 0,1,2       | Minute [M]  |
+-------------+-------------+-------------+-------------+-------------+
| 5           | Dectime     | 0,1,2       | Decimal     |
|             |             |             | time [-]    |
+-------------+-------------+-------------+-------------+-------------+
| 6           | Kdown       | 0,1,2       | Incoming    |
|             |             |             | shortwave   |
|             |             |             | radiation   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 7           | Kup         | 0,1,2       | Outgoing    |
|             |             |             | shortwave   |
|             |             |             | radiation   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 8           | Ldown       | 0,1,2       | Incoming    |
|             |             |             | longwave    |
|             |             |             | radiation   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 9           | Lup         | 0,1,2       | Outgoing    |
|             |             |             | longwave    |
|             |             |             | radiation   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 10          | Tsurf       | 0,1,2       | Bulk        |
|             |             |             | surface     |
|             |             |             | temperature |
|             |             |             | [°C]        |
+-------------+-------------+-------------+-------------+-------------+
| 11          | QN          | 0,1,2       | Net         |
|             |             |             | all-wave    |
|             |             |             | radiation   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 12          | QF          | 0,1,2       | Anthropogen |
|             |             |             | ic          |
|             |             |             | heat flux   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 13          | QS          | 0,1,2       | Storage     |
|             |             |             | heat flux   |
|             |             |             | [W          |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 14          | QH          | 0,1,2       | Sensible    |
|             |             |             | heat flux   |
|             |             |             | (calculated |
|             |             |             | using       |
|             |             |             | SUEWS) [W   |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 15          | QE          | 0,1,2       | Latent heat |
|             |             |             | flux        |
|             |             |             | (calculated |
|             |             |             | using       |
|             |             |             | SUEWS) [W   |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 16          | QHlumps     | 0,1         | Sensible    |
|             |             |             | heat flux   |
|             |             |             | (calculated |
|             |             |             | using       |
|             |             |             | LUMPS) [W   |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 17          | QElumps     | 0,1         | Latent heat |
|             |             |             | flux        |
|             |             |             | (calculated |
|             |             |             | using       |
|             |             |             | LUMPS) [W   |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 18          | QHresis     | 0,1         | Sensible    | '''         |
|             |             |             | heat flux   |             |
|             |             |             | (calculated |             |
|             |             |             | using       |             |
|             |             |             | resistance  |             |
|             |             |             | method) [W  |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 19          | Rain        | 0,1,2       | Rain [mm]   |
+-------------+-------------+-------------+-------------+-------------+
| 20          | Irr         | 0,1,2       | Irrigation  |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 21          | Evap        | 0,1,2       | Evaporation |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 22          | RO          | 0,1,2       | Runoff [mm] |
+-------------+-------------+-------------+-------------+-------------+
| 23          | TotCh       | 0,1,2       | Change in   |
|             |             |             | surface and |
|             |             |             | soil        |
|             |             |             | moisture    |
|             |             |             | stores [mm] |
+-------------+-------------+-------------+-------------+-------------+
| 24          | SurfCh      | 0,1,2       | Change in   |
|             |             |             | surface     |
|             |             |             | moisture    |
|             |             |             | store [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 25          | State       | 0,1,2       | Surface     |
|             |             |             | wetness     |
|             |             |             | state [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 26          | NWtrState   | 0,1,2       | Surface     |
|             |             |             | wetness     |
|             |             |             | state (for  |
|             |             |             | non-water   |
|             |             |             | surfaces)   |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 27          | Drainage    | 0,1,2       | Drainage    |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 28          | SMD         | 0,1,2       | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 29          | FlowCh      | 0,1         | Additional  |
|             |             |             | flow into   |
|             |             |             | water body  |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 30          | AddWater    | 0,1         | Additional  |
|             |             |             | water flow  |
|             |             |             | received    |
|             |             |             | from other  |
|             |             |             | grids [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 31          | ROSoil      | 0,1         | Runoff to   |
|             |             |             | soil        |
|             |             |             | (sub-surfac |
|             |             |             | e)          |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 32          | ROPipe      | 0,1         | Runoff to   |
|             |             |             | pipes [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 33          | ROImp       | 0,1         | Above       |
|             |             |             | ground      |
|             |             |             | runoff over |
|             |             |             | impervious  |
|             |             |             | surfaces    |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 34          | ROVeg       | 0,1         | Above       |
|             |             |             | ground      |
|             |             |             | runoff over |
|             |             |             | vegetated   |
|             |             |             | surfaces    |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 35          | ROWater     | 0,1         | Runoff for  |
|             |             |             | water body  |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 36          | WUInt       | 0,1         | Internal    |
|             |             |             | water use   |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 37          | WUEveTr     | 0,1         | Water use   |
|             |             |             | for         |
|             |             |             | irrigation  |
|             |             |             | of          |
|             |             |             | evergreen   |
|             |             |             | trees [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 38          | WUDecTr     | 0,1         | Water use   |
|             |             |             | for         |
|             |             |             | irrigation  |
|             |             |             | of          |
|             |             |             | deciduous   |
|             |             |             | trees [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 39          | WUGrass     | 0,1         | Water use   |
|             |             |             | for         |
|             |             |             | irrigation  |
|             |             |             | of grass    |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 40          | SMDPaved    | 0,1         | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit for |
|             |             |             | paved       |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 41          | SMDBldgs    | 0,1         | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit for |
|             |             |             | building    |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 42          | SMDEveTr    | 0,1         | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit for |
|             |             |             | evergreen   |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 43          | SMDDecTr    | 0,1         | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit for |
|             |             |             | deciduous   |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 44          | SMDGrass    | 0,1         | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit for |
|             |             |             | grass       |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 45          | SMDBSoil    | 0,1         | Soil        |
|             |             |             | moisture    |
|             |             |             | deficit for |
|             |             |             | bare soil   |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 46          | StPaved     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | paved       |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 47          | StBldgs     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | building    |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 48          | StEveTr     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | evergreen   |
|             |             |             | tree        |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 49          | StDecTr     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | deciduous   |
|             |             |             | tree        |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 50          | StGrass     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | grass       |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 51          | StBSoil     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | bare soil   |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 52          | StWater     | 0,1         | Surface     |
|             |             |             | wetness     |
|             |             |             | state for   |
|             |             |             | water       |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 53          | Zenith      | 0,1,2       | Solar       |
|             |             |             | zenith      |
|             |             |             | angle [°]   |
+-------------+-------------+-------------+-------------+-------------+
| 54          | Azimuth     | 0,1,2       | Solar       |
|             |             |             | azimuth     |
|             |             |             | angle [°]   |
+-------------+-------------+-------------+-------------+-------------+
| 55          | AlbBulk     | 0,1,2       | Bulk albedo |
|             |             |             | [-]         |
+-------------+-------------+-------------+-------------+-------------+
| 56          | Fcld        | 0,1,2       | Cloud       |
|             |             |             | fraction    |
|             |             |             | [-]         |
+-------------+-------------+-------------+-------------+-------------+
| 57          | LAI         | 0,1,2       | Leaf area   |
|             |             |             | index       |
|             |             |             | [m:sup:`2`  |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 58          | z0m         | 0,1         | Roughness   |
|             |             |             | length for  |
|             |             |             | momentum    |
|             |             |             | [m]         |
+-------------+-------------+-------------+-------------+-------------+
| 59          | zdm         | 0,1         | Zero-plane  |
|             |             |             | displacemen |
|             |             |             | t           |
|             |             |             | height [m]  |
+-------------+-------------+-------------+-------------+-------------+
| 60          | ustar       | 0,1,2       | Friction    |
|             |             |             | velocity [m |
|             |             |             | s\ :sup:`-1 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 61          | Lob         | 0,1,2       | Obukhov     |
|             |             |             | length [m]  |
+-------------+-------------+-------------+-------------+-------------+
| 62          | ra          | 0,1         | Aerodynamic |
|             |             |             | resistance  |
|             |             |             | [s          |
|             |             |             | m\ :sup:`-1 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 63          | rs          | 0,1         | Surface     |
|             |             |             | resistance  |
|             |             |             | [s          |
|             |             |             | m\ :sup:`-1 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 64          | Fc          | 0,1,2       | CO2 flux    | '''         |
|             |             |             | [umol       |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `           |             |
|             |             |             | s\ :sup:`-1 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 65          | FcPhoto     | 0,1         | CO2 flux    | '''         |
|             |             |             | from        |             |
|             |             |             | photosynthe |             |
|             |             |             | sis         |             |
|             |             |             | [umol       |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `           |             |
|             |             |             | s\ :sup:`-1 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 66          | FcRespi     | 0,1         | CO2 flux    | '''         |
|             |             |             | from        |             |
|             |             |             | respiration |             |
|             |             |             | [umol       |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `           |             |
|             |             |             | s\ :sup:`-1 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 67          | FcMetab     | 0,1         | CO2 flux    | '''         |
|             |             |             | from        |             |
|             |             |             | metabolism  |             |
|             |             |             | [umol       |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `           |             |
|             |             |             | s\ :sup:`-1 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 68          | FcTraff     | 0,1         | CO2 flux    | '''         |
|             |             |             | from        |             |
|             |             |             | traffic     |             |
|             |             |             | [umol       |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `           |             |
|             |             |             | s\ :sup:`-1 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 69          | FcBuild     | 0,1         | CO2 flux    | '''         |
|             |             |             | from        |             |
|             |             |             | buildings   |             |
|             |             |             | [umol       |             |
|             |             |             | m\ :sup:`-2 |             |
|             |             |             | `           |             |
|             |             |             | s\ :sup:`-1 |             |
|             |             |             | `]          |             |
|             |             |             | '''Do not   |             |
|             |             |             | use in      |             |
|             |             |             | v2017b      |             |
+-------------+-------------+-------------+-------------+-------------+
| 70          | QNSnowFr    | 1           | Net         |
|             |             |             | all-wave    |
|             |             |             | radiation   |
|             |             |             | for         |
|             |             |             | snow-free   |
|             |             |             | area [W     |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 71          | QNSnow      | 1           | Net         |
|             |             |             | all-wave    |
|             |             |             | radiation   |
|             |             |             | for snow    |
|             |             |             | area [W     |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 72          | AlbSnow     | 1           | Snow albedo |
|             |             |             | [-]         |
+-------------+-------------+-------------+-------------+-------------+
| 73          | QM          | 1           | Snow-relate |
|             |             |             | d           |
|             |             |             | heat        |
|             |             |             | exchange [W |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 74          | QMFreeze    | 1           | Internal    |
|             |             |             | energy      |
|             |             |             | change [W   |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 75          | QMRain      | 1           | Heat        |
|             |             |             | released by |
|             |             |             | rain on     |
|             |             |             | snow [W     |
|             |             |             | m\ :sup:`-2 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
| 76          | SWE         | 1           | Snow water  |
|             |             |             | equivalent  |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 77          | MeltWater   | 1           | Meltwater   |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 78          | MeltWStore  | 1           | Meltwater   |
|             |             |             | store [mm]  |
+-------------+-------------+-------------+-------------+-------------+
| 79          | SnowCh      | 1           | Change in   |
|             |             |             | snow pack   |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 80          | SnowRPaved  | 1           | Snow        |
|             |             |             | removed     |
|             |             |             | from paved  |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 81          | SnowRBldgs  | 1           | Snow        |
|             |             |             | removed     |
|             |             |             | from        |
|             |             |             | building    |
|             |             |             | surface     |
|             |             |             | [mm]        |
+-------------+-------------+-------------+-------------+-------------+
| 82          | T2          | 0,1,2       | Air         |
|             |             |             | temperature |
|             |             |             | at 2 m agl  |
|             |             |             | [°C]        |
+-------------+-------------+-------------+-------------+-------------+
| 83          | Q2          | 0,1,2       | Air         |
|             |             |             | specific    |
|             |             |             | humidity at |
|             |             |             | 2 m agl [g  |
|             |             |             | kg\ :sup:`- |
|             |             |             | 1`]         |
+-------------+-------------+-------------+-------------+-------------+
| 84          | U10         | 0,1,2       | Wind speed  |
|             |             |             | at 10 m agl |
|             |             |             | [m          |
|             |             |             | s\ :sup:`-1 |
|             |             |             | `]          |
+-------------+-------------+-------------+-------------+-------------+
|  |
+-------------+-------------+-------------+-------------+-------------+

====SSss_YYYY_nn_TT.nc (when ncMode=1 in RunControl) ==== SUEWS can also
produce the main output file in netCDF format by setting ncMode=1 (set
in `RunControl <#RunControl>`__).

As the date and time information is incorporated in the netCDF output as
separate dimension, the first five variables in the normal text output
file (in .txt) are not included in the netCDF output but other variables
are all kept.

N.B., considering the file size limit by the classic netCDF format, the
output frequency is determined automatically by the internal SUEWS
program setting to avoid the oversize problem in the netCDF files.

SSss_DailyState.txt
~~~~~~~~~~~~~~~~~~~

Contains information about the state of the surface and soil and
vegetation parameters at a time resolution of one day. One file is
written for each grid so it may contain multiple years.

+-----------------------+-----------------------+-----------------------+
| Column                | Name                  | Description           |
+=======================+=======================+=======================+
| 1                     | iy                    | Year [YYYY]           |
+-----------------------+-----------------------+-----------------------+
| 2                     | id                    | Day of year [DOY]     |
+-----------------------+-----------------------+-----------------------+
| 3                     | HDD1_h                | Heating degree days   |
|                       |                       | [°C]                  |
+-----------------------+-----------------------+-----------------------+
| 4                     | HDD2_c                | Cooling degree days   |
|                       |                       | [°C]                  |
+-----------------------+-----------------------+-----------------------+
| 5                     | HDD3_Tmean            | Average daily air     |
|                       |                       | temperature [°C]      |
+-----------------------+-----------------------+-----------------------+
| 6                     | HDT4_T5d              | 5-day running-mean    |
|                       |                       | air temperature [°C]  |
+-----------------------+-----------------------+-----------------------+
| 7                     | P/day                 | Daily total           |
|                       |                       | precipitation [mm]    |
+-----------------------+-----------------------+-----------------------+
| 8                     | DaysSR                | Days since rain       |
|                       |                       | [days]                |
+-----------------------+-----------------------+-----------------------+
| 9                     | GDD1_g                | Growing degree days   |
|                       |                       | for leaf growth [°C]  |
+-----------------------+-----------------------+-----------------------+
| 10                    | GDD2_s                | Growing degree days   |
|                       |                       | for senescence [°C]   |
+-----------------------+-----------------------+-----------------------+
| 11                    | GDD3_Tmin             | Daily minimum         |
|                       |                       | temperature [°C]      |
+-----------------------+-----------------------+-----------------------+
| 12                    | GDD4_Tmax             | Daily maximum         |
|                       |                       | temperature [°C]      |
+-----------------------+-----------------------+-----------------------+
| 13                    | GDD5_DayLHrs          | Day length [h]        |
+-----------------------+-----------------------+-----------------------+
| 14                    | LAI_EveTr             | Leaf area index of    |
|                       |                       | evergreen trees       |
|                       |                       | [m:sup:`-2`           |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 15                    | LAI_DecTr             | Leaf area index of    |
|                       |                       | deciduous trees       |
|                       |                       | [m:sup:`-2`           |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 16                    | LAI_Grass             | Leaf area index of    |
|                       |                       | grass [m:sup:`-2`     |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 17                    | DecidCap              | Moisture storage      |
|                       |                       | capacity of deciduous |
|                       |                       | trees [mm]            |
+-----------------------+-----------------------+-----------------------+
| 18                    | Porosity              | Porosity of deciduous |
|                       |                       | trees [-]             |
+-----------------------+-----------------------+-----------------------+
| 19                    | AlbEveTr              | Albedo of evergreen   |
|                       |                       | trees [-]             |
+-----------------------+-----------------------+-----------------------+
| 20                    | AlbDecTr              | Albedo of deciduous   |
|                       |                       | trees [-]             |
+-----------------------+-----------------------+-----------------------+
| 21                    | AlbGrass              | Albedo of grass [-]   |
+-----------------------+-----------------------+-----------------------+
| 22                    | WU_EveTr(1)           | Total water use for   |
|                       |                       | evergreen trees [mm]  |
+-----------------------+-----------------------+-----------------------+
| 23                    | WU_EveTr(2)           | Automatic water use   |
|                       |                       | for evergreen trees   |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 24                    | WU_EveTr(3)           | Manual water use for  |
|                       |                       | evergreen trees [mm]  |
+-----------------------+-----------------------+-----------------------+
| 25                    | WU_DecTr(1)           | Total water use for   |
|                       |                       | deciduous trees [mm]  |
+-----------------------+-----------------------+-----------------------+
| 26                    | WU_DecTr(2)           | Automatic water use   |
|                       |                       | for deciduous trees   |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 27                    | WU_DecTr(3)           | Manual water use for  |
|                       |                       | deciduous trees [mm]  |
+-----------------------+-----------------------+-----------------------+
| 28                    | WU_Grass(1)           | Total water use for   |
|                       |                       | grass [mm]            |
+-----------------------+-----------------------+-----------------------+
| 29                    | WU_Grass(2)           | Automatic water use   |
|                       |                       | for grass [mm]        |
+-----------------------+-----------------------+-----------------------+
| 30                    | WU_Grass(3)           | Manual water use for  |
|                       |                       | grass [mm]            |
+-----------------------+-----------------------+-----------------------+
| 31                    | deltaLAI              | Change in leaf area   |
|                       |                       | index (normalised     |
|                       |                       | 0-1) [-]              |
+-----------------------+-----------------------+-----------------------+
| 32                    | LAIlumps              | Leaf area index used  |
|                       |                       | in LUMPS (normalised  |
|                       |                       | 0-1) [-]              |
+-----------------------+-----------------------+-----------------------+
| 33                    | AlbSnow               | Snow albedo [-]       |
+-----------------------+-----------------------+-----------------------+
| 34                    | DensSnow_Paved        | Snow density - paved  |
|                       |                       | surface [kg           |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 35                    | DensSnow_Bldgs        | Snow density -        |
|                       |                       | building surface [kg  |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 36                    | DensSnow_EveTr        | Snow density -        |
|                       |                       | evergreen surface [kg |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 37                    | DensSnow_DecTr        | Snow density -        |
|                       |                       | deciduous surface [kg |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 38                    | DensSnow_Grass        | Snow density - grass  |
|                       |                       | surface [kg           |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 39                    | DensSnow_BSoil        | Snow density - bare   |
|                       |                       | soil surface [kg      |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 40                    | DensSnow_Water        | Snow density - water  |
|                       |                       | surface [kg           |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
|  |
+-----------------------+-----------------------+-----------------------+

.. _initialconditionsssss_yyyy.nml-1:

InitialConditionsSSss_YYYY.nml
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

At the end of the model run (or the end of each year in the model run) a
new InitialConditions file is written out (to the input folder) for each
grid, see
`InitialConditionsSSss_YYYY.nml <#InitialConditionsSSss_YYYY.nml>`__

SSss_YYYY_snow_TT.txt
~~~~~~~~~~~~~~~~~~~~~

SUEWS produces a separate output file for snow (when snowUse = 1 in
RunControl.nml) with details for each surface type.

File format of SSss_YYYY_snow_60.txt

+-----------------------+-----------------------+-----------------------+
| Column                | Name                  | Description           |
+=======================+=======================+=======================+
| 1                     | iy                    | Year [YYYY]           |
+-----------------------+-----------------------+-----------------------+
| 2                     | id                    | Day of year [DOY]     |
+-----------------------+-----------------------+-----------------------+
| 3                     | it                    | Hour [H]              |
+-----------------------+-----------------------+-----------------------+
| 4                     | imin                  | Minute [M]            |
+-----------------------+-----------------------+-----------------------+
| 5                     | dectime               | Decimal time [-]      |
+-----------------------+-----------------------+-----------------------+
| 6                     | SWE_Paved             | Snow water equivalent |
|                       |                       | – paved surface [mm]  |
+-----------------------+-----------------------+-----------------------+
| 7                     | SWE_Bldgs             | Snow water equivalent |
|                       |                       | – building surface    |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 8                     | SWE_EveTr             | Snow water equivalent |
|                       |                       | – evergreen surface   |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 9                     | SWE_DecTr             | Snow water equivalent |
|                       |                       | – deciduous surface   |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 10                    | SWE_Grass             | Snow water equivalent |
|                       |                       | – grass surface [mm]  |
+-----------------------+-----------------------+-----------------------+
| 11                    | SWE_BSoil             | Snow water equivalent |
|                       |                       | – bare soil surface   |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 12                    | SWE_Water             | Snow water equivalent |
|                       |                       | – water surface [mm]  |
+-----------------------+-----------------------+-----------------------+
| 13                    | Mw_Paved              | Meltwater – paved     |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`]         |
+-----------------------+-----------------------+-----------------------+
| 14                    | Mw_Bldgs              | Meltwater – building  |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`]         |
+-----------------------+-----------------------+-----------------------+
| 15                    | Mw_EveTr              | Meltwater – evergreen |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`]         |
+-----------------------+-----------------------+-----------------------+
| 16                    | Mw_DecTr              | Meltwater – deciduous |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`]         |
+-----------------------+-----------------------+-----------------------+
| 17                    | Mw_Grass              | Meltwater – grass     |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`\ 1]      |
+-----------------------+-----------------------+-----------------------+
| 18                    | Mw_BSoil              | Meltwater – bare soil |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`]         |
+-----------------------+-----------------------+-----------------------+
| 19                    | Mw_Water              | Meltwater – water     |
|                       |                       | surface [mm           |
|                       |                       | h\ :sup:`-1`]         |
+-----------------------+-----------------------+-----------------------+
| 20                    | Qm_Paved              | Snowmelt-related heat |
|                       |                       | – paved surface [W    |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 21                    | Qm_Bldgs              | Snowmelt-related heat |
|                       |                       | – building surface [W |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 22                    | Qm_EveTr              | Snowmelt-related heat |
|                       |                       | – evergreen surface   |
|                       |                       | [W m\ :sup:`-2`]      |
+-----------------------+-----------------------+-----------------------+
| 23                    | Qm_DecTr              | Snowmelt-related heat |
|                       |                       | – deciduous surface   |
|                       |                       | [W m\ :sup:`-2`]      |
+-----------------------+-----------------------+-----------------------+
| 24                    | Qm_Grass              | Snowmelt-related heat |
|                       |                       | – grass surface [W    |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 25                    | Qm_BSoil              | Snowmelt-related heat |
|                       |                       | – bare soil surface   |
|                       |                       | [W m\ :sup:`-2`]      |
+-----------------------+-----------------------+-----------------------+
| 26                    | Qm_Water              | Snowmelt-related heat |
|                       |                       | – water surface [W    |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 27                    | Qa_Paved              | Advective heat –      |
|                       |                       | paved surface [W      |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 28                    | Qa_Bldgs              | Advective heat –      |
|                       |                       | building surface [W   |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 29                    | Qa_EveTr              | Advective heat –      |
|                       |                       | evergreen surface [W  |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 30                    | Qa_DecTr              | Advective heat –      |
|                       |                       | deciduous surface [W  |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 31                    | Qa_Grass              | Advective heat –      |
|                       |                       | grass surface [W      |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 32                    | Qa_BSoil              | Advective heat – bare |
|                       |                       | soil surface [W       |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 33                    | Qa_Water              | Advective heat –      |
|                       |                       | water surface [W      |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 34                    | QmFr_Paved            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – paved surface |
|                       |                       | [W m\ :sup:`-2`]      |
+-----------------------+-----------------------+-----------------------+
| 35                    | QmFr_Bldgs            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – building      |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 36                    | QmFr_EveTr            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – evergreen     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 37                    | QmFr_DecTr            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – deciduous     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 38                    | QmFr_Grass            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – grass surface |
|                       |                       | [W m\ :sup:`-2`]      |
+-----------------------+-----------------------+-----------------------+
| 39                    | QmFr_BSoil            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – bare soil     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 40                    | QmFr_Water            | Heat related to       |
|                       |                       | freezing of surface   |
|                       |                       | store – water [W      |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 41                    | fr_Paved              | Fraction of snow –    |
|                       |                       | paved surface [-]     |
+-----------------------+-----------------------+-----------------------+
| 42                    | fr_Bldgs              | Fraction of snow –    |
|                       |                       | building surface [-]  |
+-----------------------+-----------------------+-----------------------+
| 43                    | fr_EveTr              | Fraction of snow –    |
|                       |                       | evergreen surface [-] |
+-----------------------+-----------------------+-----------------------+
| 44                    | fr_DecTr              | Fraction of snow –    |
|                       |                       | deciduous surface [-] |
+-----------------------+-----------------------+-----------------------+
| 45                    | fr_Grass              | Fraction of snow –    |
|                       |                       | grass surface [-]     |
+-----------------------+-----------------------+-----------------------+
| 46                    | Fr_BSoil              | Fraction of snow –    |
|                       |                       | bare soil surface [-] |
+-----------------------+-----------------------+-----------------------+
| 47                    | RainSn_Paved          | Rain on snow – paved  |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 48                    | RainSn_Bdgs           | Rain on snow –        |
|                       |                       | building surface [mm] |
+-----------------------+-----------------------+-----------------------+
| 49                    | RainSn_EveTr          | Rain on snow –        |
|                       |                       | evergreen surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 50                    | RainSn_DecTr          | Rain on snow –        |
|                       |                       | deciduous surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 51                    | RainSn_Grass          | Rain on snow – grass  |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 52                    | RainSn_BSoil          | Rain on snow – bare   |
|                       |                       | soil surface [mm]     |
+-----------------------+-----------------------+-----------------------+
| 53                    | RainSn_Water          | Rain on snow – water  |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 54                    | qn_PavedSnow          | Net all-wave          |
|                       |                       | radiation – paved     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 55                    | qn_BldgsSnow          | Net all-wave          |
|                       |                       | radiation – building  |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 56                    | qn_EveTrSnow          | Net all-wave          |
|                       |                       | radiation – evergreen |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 57                    | qn_DecTrSnow          | Net all-wave          |
|                       |                       | radiation – deciduous |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 58                    | qn_GrassSnow          | Net all-wave          |
|                       |                       | radiation – grass     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 59                    | qn_BSoilSnow          | Net all-wave          |
|                       |                       | radiation – bare soil |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 60                    | qn_WaterSnow          | Net all-wave          |
|                       |                       | radiation – water     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 61                    | kup_PavedSnow         | Reflected shortwave   |
|                       |                       | radiation – paved     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 62                    | kup_BldgsSnow         | Reflected shortwave   |
|                       |                       | radiation – building  |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 63                    | kup_EveTrSnow         | Reflected shortwave   |
|                       |                       | radiation – evergreen |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 64                    | kup_DecTrSnow         | Reflected shortwave   |
|                       |                       | radiation – deciduous |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 65                    | kup_GrassSnow         | Reflected shortwave   |
|                       |                       | radiation – grass     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 66                    | kup_BSoilSnow         | Reflected shortwave   |
|                       |                       | radiation – bare soil |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 67                    | kup_WaterSnow         | Reflected shortwave   |
|                       |                       | radiation – water     |
|                       |                       | surface [W            |
|                       |                       | m\ :sup:`-2`]         |
+-----------------------+-----------------------+-----------------------+
| 68                    | frMelt_Paved          | Amount of freezing    |
|                       |                       | melt water – paved    |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 69                    | frMelt_Bldgs          | Amount of freezing    |
|                       |                       | melt water – building |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 70                    | frMelt_EveTr          | Amount of freezing    |
|                       |                       | melt water –          |
|                       |                       | evergreen surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 71                    | frMelt_DecTr          | Amount of freezing    |
|                       |                       | melt water –          |
|                       |                       | deciduous surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 72                    | frMelt_Grass          | Amount of freezing    |
|                       |                       | melt water – grass    |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 73                    | frMelt_BSoil          | Amount of freezing    |
|                       |                       | melt water – bare     |
|                       |                       | soil surface [mm]     |
+-----------------------+-----------------------+-----------------------+
| 74                    | frMelt_Water          | Amount of freezing    |
|                       |                       | melt water – water    |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 75                    | MwStore_Paved         | Melt water store –    |
|                       |                       | paved surface [mm]    |
+-----------------------+-----------------------+-----------------------+
| 76                    | MwStore_Bldgs         | Melt water store –    |
|                       |                       | building surface [mm] |
+-----------------------+-----------------------+-----------------------+
| 77                    | MwStore_EveTt         | Melt water store –    |
|                       |                       | evergreen surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 78                    | MwStore_DecTr         | Melt water store –    |
|                       |                       | deciduous surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 79                    | MwStore_Grass         | Melt water store –    |
|                       |                       | grass surface [mm]    |
+-----------------------+-----------------------+-----------------------+
| 80                    | MwStore_BSoil         | Melt water store –    |
|                       |                       | bare soil surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 81                    | MwStore_Water         | Melt water store –    |
|                       |                       | water surface [mm]    |
+-----------------------+-----------------------+-----------------------+
| 82                    | DensSnow_Paved        | Snow density – paved  |
|                       |                       | surface [kg           |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 83                    | DensSnow_Bldgs        | Snow density –        |
|                       |                       | building surface [kg  |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 84                    | DensSnow_EveTr        | Snow density –        |
|                       |                       | evergreen surface [kg |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 85                    | DensSnow_DecTr        | Snow density –        |
|                       |                       | deciduous surface [kg |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 86                    | DensSnow_Grass        | Snow density – grass  |
|                       |                       | surface [kg           |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 87                    | DensSnow_BSoil        | Snow density – bare   |
|                       |                       | soil surface [kg      |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 88                    | DensSnow_Water        | Snow density – water  |
|                       |                       | surface [kg           |
|                       |                       | m\ :sup:`-3`]         |
+-----------------------+-----------------------+-----------------------+
| 89                    | Sd_Paved              | Snow depth – paved    |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 90                    | Sd_Bldgs              | Snow depth – building |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 91                    | Sd_EveTr              | Snow depth –          |
|                       |                       | evergreen surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 92                    | Sd_DecTr              | Snow depth –          |
|                       |                       | deciduous surface     |
|                       |                       | [mm]                  |
+-----------------------+-----------------------+-----------------------+
| 93                    | Sd_Grass              | Snow depth – grass    |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 94                    | Sd_BSoil              | Snow depth – bare     |
|                       |                       | soil surface [mm]     |
+-----------------------+-----------------------+-----------------------+
| 95                    | Sd_Water              | Snow depth – water    |
|                       |                       | surface [mm]          |
+-----------------------+-----------------------+-----------------------+
| 96                    | Tsnow_Paved           | Snow surface          |
|                       |                       | temperature – paved   |
|                       |                       | surface [°C]          |
+-----------------------+-----------------------+-----------------------+
| 97                    | Tsnow_Bldgs           | Snow surface          |
|                       |                       | temperature –         |
|                       |                       | building surface [°C] |
+-----------------------+-----------------------+-----------------------+
| 98                    | Tsnow_EveTr           | Snow surface          |
|                       |                       | temperature –         |
|                       |                       | evergreen surface     |
|                       |                       | [°C]                  |
+-----------------------+-----------------------+-----------------------+
| 99                    | Tsnow_DecTr           | Snow surface          |
|                       |                       | temperature –         |
|                       |                       | deciduous surface     |
|                       |                       | [°C]                  |
+-----------------------+-----------------------+-----------------------+
| 100                   | Tsnow_Grass           | Snow surface          |
|                       |                       | temperature – grass   |
|                       |                       | surface [°C]          |
+-----------------------+-----------------------+-----------------------+
| 101                   | Tsnow_BSoil           | Snow surface          |
|                       |                       | temperature – bare    |
|                       |                       | soil surface [°C]     |
+-----------------------+-----------------------+-----------------------+
| 102                   | Tsnow_Water           | Snow surface          |
|                       |                       | temperature – water   |
|                       |                       | surface [°C]          |
+-----------------------+-----------------------+-----------------------+

SSss_YYYY_BL.txt
~~~~~~~~~~~~~~~~

Meteorological variables modelled by CBL portion of the model are output
in to this file created for each day with time step (see section CBL
Input).

+-----------------+-----------------+-----------------+-----------------+
| Col             | Header          | Name            | Units           |
+=================+=================+=================+=================+
| 1               | iy              | Year [YYYY]     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 2               | id              | Day of year     |                 |
|                 |                 | [DoY]           |                 |
+-----------------+-----------------+-----------------+-----------------+
| 3               | it              | Hour [H]        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 4               | imin            | Minute [M]      |                 |
+-----------------+-----------------+-----------------+-----------------+
| 5               | dectime         | Decimal time    |                 |
|                 |                 | [-]             |                 |
+-----------------+-----------------+-----------------+-----------------+
| 6               | zi              | Convectibe      | m               |
|                 |                 | boundary layer  |                 |
|                 |                 | height          |                 |
+-----------------+-----------------+-----------------+-----------------+
| 7               | Theta           | Potential       | K               |
|                 |                 | temperature in  |                 |
|                 |                 | the inertial    |                 |
|                 |                 | sublayer        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 8               | Q               | Specific        | g kg\ :sup:`-1` |
|                 |                 | humidity in the |                 |
|                 |                 | inertial        |                 |
|                 |                 | sublayer        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 9               | theta+          | Potential       | K               |
|                 |                 | temperature     |                 |
|                 |                 | just above the  |                 |
|                 |                 | CBL             |                 |
+-----------------+-----------------+-----------------+-----------------+
| 10              | q+              | Specific        | g kg\ :sup:`-1` |
|                 |                 | humidity just   |                 |
|                 |                 | above the CBL   |                 |
+-----------------+-----------------+-----------------+-----------------+
| 11              | Temp_C          | Air temperature | °C              |
+-----------------+-----------------+-----------------+-----------------+
| 12              | RH              | Relative        | %               |
|                 |                 | humidity        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 13              | QH_use          | Sensible heat   | W m\ :sup:`-2`  |
|                 |                 | flux used for   |                 |
|                 |                 | calculation     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 14              | QE_use          | Latent heat     | W m\ :sup:`-2`  |
|                 |                 | flux used for   |                 |
|                 |                 | calculation     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 15              | Press_hPa       | Pressure used   | hPa             |
|                 |                 | for calculation |                 |
+-----------------+-----------------+-----------------+-----------------+
| 16              | avu1            | Wind speed used | m s\ :sup:`-1`  |
|                 |                 | for calculation |                 |
+-----------------+-----------------+-----------------+-----------------+
| 17              | ustar           | Friction        | m s\ :sup:`-1`  |
|                 |                 | velocity used   |                 |
|                 |                 | for calculation |                 |
+-----------------+-----------------+-----------------+-----------------+
| 18              | avdens          | Air density     | kg m\ :sup:`-3` |
|                 |                 | used for        |                 |
|                 |                 | calculation     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 19              | lv_J_kg         | Latent heat of  | J kg\ :sup:`-1` |
|                 |                 | vaporization    |                 |
|                 |                 | used for        |                 |
|                 |                 | calculation     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 20              | avcp            | Specific heat   | J kg\ :sup:`-1` |
|                 |                 | capacity used   | K\ :sup:`-1`    |
|                 |                 | for calculation |                 |
+-----------------+-----------------+-----------------+-----------------+
| 21              | gamt            | Vertical        | K m\ :sup:`-1`  |
|                 |                 | gradient of     |                 |
|                 |                 | potential       |                 |
|                 |                 | temperature     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 22              | gamq            | Vertical        | kg              |
|                 |                 | gradient of     | kg\ :sup:`-1`   |
|                 |                 | specific        | m\ :sup:`-1`    |
|                 |                 | humidity        |                 |
+-----------------+-----------------+-----------------+-----------------+

SOLWEIGpoiOut.txt
~~~~~~~~~~~~~~~~~

Calculated variables from POI, point of interest (row, col) stated in
SOLWEIGinput.nml.

SOLWEIG model output file format: SOLWEIGpoiOUT.txt

+-----------------+-----------------+-----------------+-----------------+
| Col             | Header          | Name            | Units           |
+=================+=================+=================+=================+
| 1               | id              | Day of year     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 2               | dectime         | Decimal time    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 3               | azimuth         | Azimuth angle   | °               |
|                 |                 | of the Sun      |                 |
+-----------------+-----------------+-----------------+-----------------+
| 4               | altitude        | Altitude angle  | °               |
|                 |                 | of the Sun      |                 |
+-----------------+-----------------+-----------------+-----------------+
| 5               | GlobalRad       | Input Kdn       | W m\ :sup:`-2`  |
+-----------------+-----------------+-----------------+-----------------+
| 6               | DiffuseRad      | Diffuse         | W m\ :sup:`-2`  |
|                 |                 | shortwave       |                 |
|                 |                 | radiation       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 7               | DirectRad       | Direct          | W m\ :sup:`-2`  |
|                 |                 | shortwave       |                 |
|                 |                 | radiation       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 8               | Kdown2d         | Incoming        | W m\ :sup:`-2`  |
|                 |                 | shortwave       |                 |
|                 |                 | radiation at    |                 |
|                 |                 | POI             |                 |
+-----------------+-----------------+-----------------+-----------------+
|  |
+-----------------+-----------------+-----------------+-----------------+
| 9               | Kup2d           | Outgoing        | W m\ :sup:`-2`  |
|                 |                 | shortwave       |                 |
|                 |                 | radiation at    |                 |
|                 |                 | POI             |                 |
+-----------------+-----------------+-----------------+-----------------+
|  |
+-----------------+-----------------+-----------------+-----------------+
| 10              | Ksouth          | Shortwave       | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | south at POI    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 11              | Kwest           | Shortwave       | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | west at POI     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 12              | Knorth          | Shortwave       | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | north at POI    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 13              | Keast           | Shortwave       | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | east at POI     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 14              | Ldown2d         | Incoming        | W m\ :sup:`-2`  |
|                 |                 | longwave        |                 |
|                 |                 | radiation at    |                 |
|                 |                 | POI             |                 |
+-----------------+-----------------+-----------------+-----------------+
| 15              | Lup2d           | Outgoing        | W m\ :sup:`-2`  |
|                 |                 | longwave        |                 |
|                 |                 | radiation at    |                 |
|                 |                 | POI             |                 |
+-----------------+-----------------+-----------------+-----------------+
| 16              | Lsouth          | Longwave        | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | south at POI    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 17              | Lwest           | Longwave        | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | west at POI     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 18              | Lnorth          | Longwave        | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | north at POI    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 19              | Least           | Longwave        | W m\ :sup:`-2`  |
|                 |                 | radiation from  |                 |
|                 |                 | east at POI     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 20              | Tmrt            | Mean Radiant    | °C              |
|                 |                 | Temperature     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 21              | I0              | theoretical     | W m\ :sup:`-2`  |
|                 |                 | value of        |                 |
|                 |                 | maximum         |                 |
|                 |                 | incoming solar  |                 |
|                 |                 | radiation       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 22              | CI              | clearness index |                 |
|                 |                 | for Ldown       |                 |
|                 |                 | (Lindberg et    |                 |
|                 |                 | al. 2008)       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 23              | gvf             | Ground view     |                 |
|                 |                 | factor          |                 |
|                 |                 | (Lindberg and   |                 |
|                 |                 | Grimmond 2011)  |                 |
+-----------------+-----------------+-----------------+-----------------+
| 24              | shadow          | Shadow value    |                 |
|                 |                 | (0= shadow, 1 = |                 |
|                 |                 | sun)            |                 |
+-----------------+-----------------+-----------------+-----------------+
| 25              | svf             | Sky View Factor |                 |
|                 |                 | from ground and |                 |
|                 |                 | buildings       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 26              | svfbuveg        | Sky View Factor |                 |
|                 |                 | from ground,    |                 |
|                 |                 | buildings and   |                 |
|                 |                 | vegetation      |                 |
+-----------------+-----------------+-----------------+-----------------+
| 27              | Ta              | Air temperature | °C              |
+-----------------+-----------------+-----------------+-----------------+
| 28              | Tg              | Surface         | °C              |
|                 |                 | temperature     |                 |
+-----------------+-----------------+-----------------+-----------------+

SSss_YYYY_ESTM_TT.txt
~~~~~~~~~~~~~~~~~~~~~

If the ESTM model option is run, the following output file is created.
**Note: First time steps of storage output could give NaN values during
the initial converging phase.**

ESTM output file format

+-----------------+-----------------+-----------------+-----------------+
| Col             | Header          | Name            | Units           |
+=================+=================+=================+=================+
| 1               | iy              | Year            |                 |
+-----------------+-----------------+-----------------+-----------------+
| 2               | id              | Day of year     |                 |
+-----------------+-----------------+-----------------+-----------------+
| 3               | it              | Hour            |                 |
+-----------------+-----------------+-----------------+-----------------+
| 4               | imin            | Minute          |                 |
+-----------------+-----------------+-----------------+-----------------+
| 5               | dectime         | Decimal time    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 6               | QSnet           | Net storage     | W m\ :sup:`-2`  |
|                 |                 | heat flux       |                 |
|                 |                 | (QSwall+QSgroun |                 |
|                 |                 | d+QS)           |                 |
+-----------------+-----------------+-----------------+-----------------+
| 7               | QSair           | Storage heat    | W m\ :sup:`-2`  |
|                 |                 | flux into air   |                 |
+-----------------+-----------------+-----------------+-----------------+
| 8               | QSwall          | Storage heat    | W m\ :sup:`-2`  |
|                 |                 | flux into wall  |                 |
+-----------------+-----------------+-----------------+-----------------+
| 9               | QSroof          | Storage heat    | W m\ :sup:`-2`  |
|                 |                 | flux into roof  |                 |
+-----------------+-----------------+-----------------+-----------------+
| 10              | QSground        | Storage heat    | W m\ :sup:`-2`  |
|                 |                 | flux into       |                 |
|                 |                 | ground          |                 |
+-----------------+-----------------+-----------------+-----------------+
| 11              | QSibld          | Storage heat    | W m\ :sup:`-2`  |
|                 |                 | flux into       |                 |
|                 |                 | internal        |                 |
|                 |                 | elements in     |                 |
|                 |                 | buildling       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 12              | Twall1          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of wall         |                 |
|                 |                 | (outer-most)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 13              | Twall2          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of wall         |                 |
+-----------------+-----------------+-----------------+-----------------+
| 14              | Twall3          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of wall         |                 |
+-----------------+-----------------+-----------------+-----------------+
| 15              | Twall4          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of wall         |                 |
+-----------------+-----------------+-----------------+-----------------+
| 16              | Twall5          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of wall         |                 |
|                 |                 | (inner-most)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 17              | Troof1          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of roof         |                 |
|                 |                 | (outer-most)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 18              | Troof2          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of roof         |                 |
+-----------------+-----------------+-----------------+-----------------+
| 19              | Troof3          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of roof         |                 |
+-----------------+-----------------+-----------------+-----------------+
| 20              | Troof4          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of roof         |                 |
+-----------------+-----------------+-----------------+-----------------+
| 21              | Troof5          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of ground       |                 |
|                 |                 | (inner-most)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 22              | Tground1        | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of ground       |                 |
|                 |                 | (outer-most)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 23              | Tground2        | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of ground       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 24              | Tground3        | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of ground       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 25              | Tground4        | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of ground       |                 |
+-----------------+-----------------+-----------------+-----------------+
| 26              | Tground5        | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of ground       |                 |
|                 |                 | (inner-most)    |                 |
+-----------------+-----------------+-----------------+-----------------+
| 27              | Tibld1          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of internal     |                 |
|                 |                 | elements        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 28              | Tibld2          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of internal     |                 |
|                 |                 | elements        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 29              | Tibld3          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of internal     |                 |
|                 |                 | elements        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 30              | Tibld4          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of internal     |                 |
|                 |                 | elements        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 31              | Tibld5          | Temperature in  | K               |
|                 |                 | the first layer |                 |
|                 |                 | of internal     |                 |
|                 |                 | elements        |                 |
+-----------------+-----------------+-----------------+-----------------+
| 32              | Tabld           | Air temperature | K               |
|                 |                 | in buildings    |                 |
+-----------------+-----------------+-----------------+-----------------+