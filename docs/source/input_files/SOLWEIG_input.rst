SOLWEIG input files
-------------------

If the SOLWEIG model option is used (SOLWEIGout=1), spatial data and a
SOLWEIGInput.nml file need to be prepared. The Digital Surface Models
(DSMs) as well as derivatives originating from DSMs, e.g. Sky View
Factors (SVF) must have the same spatial resolution and extent. Since
SOLWEIG is a 2D model it will considerably increase computation time and
should be used with care.

Description of choices in SOLWEIGinput_file.nml file. The file can be in
any order.

+----------------+--------------------------+-----------------------+
| Name           | Units                    | Description           |
+================+==========================+=======================+
|                |                          |                       |
+----------------+--------------------------+-----------------------+
| Posture        | -                        | Determines the        |
|                |                          | posture of a human    |
|                |                          | for which the radiant |
|                |                          | fluxes should be      |
|                |                          | considered            |
+----------------+--------------------------+-----------------------+
| 1              | Standing (default)       |                       |
+----------------+--------------------------+-----------------------+
| 2              | Sitting                  |                       |
+----------------+--------------------------+-----------------------+
| absL           | -                        | Absorption            |
|                |                          | coefficient of        |
|                |                          | longwave radiation of |
|                |                          | a person.             |
|                |                          | -  Recommended value: |
|                |                          | 0.97                  |
+----------------+--------------------------+-----------------------+
| absK           | -                        | Absorption            |
|                |                          | coefficient of        |
|                |                          | shortwave radiation   |
|                |                          | of a person.          |
|                |                          | -  Recommended value: |
|                |                          | 0.70                  |
+----------------+--------------------------+-----------------------+
| heightgravity  | m                        | Centre of gravity for |
|                |                          | a person.             |
|                |                          | -  Recommended value  |
|                |                          | for a standing        |
|                |                          | man: 1.1 m            |
+----------------+--------------------------+-----------------------+
| usevegdem      | -                        | Vegetation scheme     |
+----------------+--------------------------+-----------------------+
| 1              | Vegetation scheme is     |                       |
|                | active (Lindberg and     |                       |
|                | Grimmond 2011 [FL2011]_) |                       |
+----------------+--------------------------+-----------------------+
| 2              | No vegetation scheme     |                       |
|                | used                     |                       |
+----------------+--------------------------+-----------------------+
| DSMPath        | -                        | Path to Digital       |
|                |                          | Surface Models (DSM). |
+----------------+--------------------------+-----------------------+
| DSMname        | -                        | Ground and Building   |
|                |                          | DSM                   |
+----------------+--------------------------+-----------------------+
| CDSMname       | -                        | Vegetation canopy DSM |
+----------------+--------------------------+-----------------------+
| TDSMname       | -                        | Vegetation trunk zone |
|                |                          | DSM                   |
+----------------+--------------------------+-----------------------+
| TransMin       | -                        | Tranmissivity of K    |
|                |                          | through deciduous     |
|                |                          | vegetation (leaf on)  |
|                |                          | -  Recommended value: |
|                |                          | 0.02 (Konarska et     |
|                |                          | al. 2014 [Ko14]_)     |
+----------------+--------------------------+-----------------------+
| TransMax       | -                        | Tranmissivity of K    |
|                |                          | through deciduous     |
|                |                          | vegetation (leaf off) |
|                |                          | -  Recommended value: |
|                |                          | 0.50 (Konarska et     |
|                |                          | al. 2014 [Ko14]_)     |
+----------------+--------------------------+-----------------------+
| SVFPath        | -                        | Path to SVFs matrices |
|                |                          | (See Lindberg and     |
|                |                          | Grimmond              |
|                |                          | (2011) [FL2011]_ for  |
|                |                          | details)              |
+----------------+--------------------------+-----------------------+
| SVFSuffix      | -                        | Suffix used (if any)  |
+----------------+--------------------------+-----------------------+
| BuildingName   | -                        | Boolean matrix for    |
|                |                          | locations of building |
|                |                          | pixels                |
+----------------+--------------------------+-----------------------+
| row            | -                        | X coordinate for      |
|                |                          | point of interest.    |
|                |                          | Here all variables    |
|                |                          | from the model will   |
|                |                          | written to            |
|                |                          | SOLWEIGpoiOUT.txt     |
+----------------+--------------------------+-----------------------+
| col            | -                        | Y coordinate for      |
|                |                          | point of interest.    |
|                |                          | Here all variables    |
|                |                          | from the model will   |
|                |                          | written to            |
|                |                          | SOLWEIGpoiOUT.txt     |
+----------------+--------------------------+-----------------------+
| onlyglobal     | -                        | Global radiation      |
+----------------+--------------------------+-----------------------+
| 0              | Diffuse and direct       |                       |
|                | shortwave radiation      |                       |
|                | taken from met           |                       |
|                | forcing file.            |                       |
+----------------+--------------------------+-----------------------+
| 1              | Diffuse and direct       |                       |
|                | shortwave radiation      |                       |
|                | calculated from          |                       |
|                | Reindl et al.            |                       |
|                | (1990) [Re90]_           |                       |
+----------------+--------------------------+-----------------------+
| SOLWEIGpoi_out | -                        | Write output          |
|                |                          | variables at point of |
|                |                          | interest (see below)  |
+----------------+--------------------------+-----------------------+
| 0              | No POI output            |                       |
+----------------+--------------------------+-----------------------+
| Tmrt_out       | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | No grid output           |                       |
+----------------+--------------------------+-----------------------+
| 1              | Write grid to file       |                       |
|                | (saves as ERSI Ascii     |                       |
|                | grid)                    |                       |
+----------------+--------------------------+-----------------------+
| Lup2d_out      | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | No grid output           |                       |
+----------------+--------------------------+-----------------------+
| 1              | Write grid to file       |                       |
|                | (saves as ERSI Ascii     |                       |
|                | grid)                    |                       |
+----------------+--------------------------+-----------------------+
| Ldown2d_out    | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | No grid output           |                       |
+----------------+--------------------------+-----------------------+
| 1              | Write grid to file       |                       |
|                | (saves as ERSI Ascii     |                       |
|                | grid)                    |                       |
+----------------+--------------------------+-----------------------+
| Kup2d_out      | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | No grid output           |                       |
+----------------+--------------------------+-----------------------+
| 1              | Write grid to file       |                       |
|                | (saves as ERSI Ascii     |                       |
|                | grid)                    |                       |
+----------------+--------------------------+-----------------------+
| Kdown2d_out    | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | No grid output           |                       |
+----------------+--------------------------+-----------------------+
| 1              | Write grid to file       |                       |
|                | (saves as ERSI Ascii     |                       |
|                | grid)                    |                       |
+----------------+--------------------------+-----------------------+
| GVF_out        | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | No grid output           |                       |
+----------------+--------------------------+-----------------------+
| 1              | Write grid to file       |                       |
|                | (saves as ERSI Ascii     |                       |
|                | grid)                    |                       |
+----------------+--------------------------+-----------------------+
| SOLWEIG_ldown  | -                        |                       |
+----------------+--------------------------+-----------------------+
| 0              | Not active (use SUEWS    |                       |
|                | to estimate Ldown        |                       |
|                | above canyon)            |                       |
+----------------+--------------------------+-----------------------+
| 1              | Use SOLWEIG to           |                       |
|                | estimate Ldown above     |                       |
|                | canyon                   |                       |
+----------------+--------------------------+-----------------------+
| OutInterval    | min                      | Output interval. Set  |
|                |                          | to 60 in current      |
|                |                          | version.              |
+----------------+--------------------------+-----------------------+
| RunForGrid     | -                        | Grid for which        |
|                |                          | SOLWEIG should be     |
|                |                          | run.                  |
+----------------+--------------------------+-----------------------+
| -999           | All grids (use with      |                       |
|                | care)                    |                       |
+----------------+--------------------------+-----------------------+
|                |                          |                       |
+----------------+--------------------------+-----------------------+