CBL input files
---------------

Main references for this part of the model: Onomura et al. (2015) [Shiho2015]_
and Cleugh and Grimmond (2001) [CG2001]_.

If CBL slab model is used (CBLuse=1 in
`RunControl.nml <#RunControl.nml>`__) the following files are needed:

+----------------------+-----------------------------------+
| Filename             | Purpose                           |
+======================+===================================+
| CBL_initial_data.txt | Gives initial data every morning  |
|                      | when CBL slab model starts        |
|                      | running.                          |
|                      | -  filename must match the        |
|                      | InitialData_FileName in           |
|                      | CBLInput.nml.                     |
|                      | -  fixed format.                  |
+----------------------+-----------------------------------+
| CBLInput.nml         | Specifies run options, parameters |
|                      | and input file names.             |
|                      | -  Can be in any order            |
+----------------------+-----------------------------------+

CBL_initial_data.txt
~~~~~~~~~~~~~~~~~~~~

This file should give initial data every morning when CBL slab model
starts running. The file name should match the InitialData_FileName in
CBLInput.nml.

Definitions and example file of initial values prepared for Sacramento.

+-----------------------+-----------------------+-----------------------+
| No.                   | Column name           | Description           |
+=======================+=======================+=======================+
| 1                     | id                    | Day of year [DOY]     |
+-----------------------+-----------------------+-----------------------+
| 2                     | zi0                   | initial convective    |
|                       |                       | boundary layer height |
|                       |                       | (m)                   |
+-----------------------+-----------------------+-----------------------+
| 3                     | gamt_Km               | vertical gradient of  |
|                       |                       | potential temperature |
|                       |                       | (K m\ :sup:`-1`)      |
|                       |                       | strength of the       |
|                       |                       | inversion             |
+-----------------------+-----------------------+-----------------------+
| 4                     | gamq_gkgm             | vertical gradient of  |
|                       |                       | specific humidity (g  |
|                       |                       | kg\ :sup:`-1`         |
|                       |                       | m\ :sup:`-1`)         |
+-----------------------+-----------------------+-----------------------+
| 5                     | Theta+_K              | potential temperature |
|                       |                       | at the top of CBL (K) |
+-----------------------+-----------------------+-----------------------+
| 6                     | q+_gkg                | specific humidity at  |
|                       |                       | the top of CBL (g     |
|                       |                       | kg\ :sup:`-1`)        |
+-----------------------+-----------------------+-----------------------+
| 7                     | Theta_K               | potential temperature |
|                       |                       | in CBL (K)            |
+-----------------------+-----------------------+-----------------------+
| 8                     | q_gkg                 | specific humidiy in   |
|                       |                       | CBL (g kg\ :sup:`-1`) |
+-----------------------+-----------------------+-----------------------+

-  gamt_Km and gamq_gkgm written to two significant figures are required
   for the model performance in appropriate ranges [Shiho2015]_.

+-----+-----+---------+-----------+----------+--------+---------+-------+
| id  | zi0 | gamt_Km | gamq_gkgm | Theta+_K | q+_gkg | theta_K | q_gkg |
+=====+=====+=========+===========+==========+========+=========+=======+
| 234 | 188 | 0.0032  | 0.00082   | 290.4    | 9.6    | 288.7   | 8.3   |
+-----+-----+---------+-----------+----------+--------+---------+-------+
| 235 | 197 | 0.0089  | 0.089     | 290.2    | 8.4    | 288.3   | 8.7   |
+-----+-----+---------+-----------+----------+--------+---------+-------+
| ⁞   | ⁞   | ⁞       | ⁞         | ⁞        | ⁞      | ⁞       | ⁞     |
+-----+-----+---------+-----------+----------+--------+---------+-------+
| ⁞   | ⁞   | ⁞       | ⁞         | ⁞        | ⁞      | ⁞       | ⁞     |
+-----+-----+---------+-----------+----------+--------+---------+-------+
|     |     |         |           |          |        |         |       |
+-----+-----+---------+-----------+----------+--------+---------+-------+

CBL_Input.nml
~~~~~~~~~~~~~

+---------------------+-------------------------------------+
| Name                | Description                         |
+=====================+=====================================+
|                     |                                     |
+---------------------+-------------------------------------+
| EntrainmentType     | Determines entrainment scheme.      |
|                     | See Cleugh and Grimmond             |
|                     | 2000 [CG2001]_ for details.         |
+---------------------+-------------------------------------+
| Value               | Comments                            |
+---------------------+-------------------------------------+
| 1                   | Tennekes and Driedonks (1981) -     |
|                     | **Recommended**                     |
+---------------------+-------------------------------------+
| 2                   | McNaughton and Springs (1986)       |
+---------------------+-------------------------------------+
| 3                   | Rayner and Watson (1991)            |
+---------------------+-------------------------------------+
| 4                   | Tennekes (1973)                     |
+---------------------+-------------------------------------+
| QH_Choice           | Determines QH used for CBL model.   |
+---------------------+-------------------------------------+
| Value               | Comments                            |
+---------------------+-------------------------------------+
| 1                   | QH modelled by SUEWS                |
+---------------------+-------------------------------------+
| 2                   | QH modelled by LUMPS                |
+---------------------+-------------------------------------+
| 3                   | Observed QH values are used from    |
|                     | the meteorological input file       |
+---------------------+-------------------------------------+
| Wsb                 | Subsidence velocity (m              |
|                     | s\ :sup:`-1`) in eq. 1 and 2 of     |
|                     | Onomura et al. (2015) [Shiho2015]_. |
|                     | (-0.01 m s\ :sup:`-1`               |
|                     | recommended)                        |
+---------------------+-------------------------------------+
| CBLday(id)          | CBL model is used for the days      |
|                     | you choose.                         |
|                     | -  Set CBLday(id) = 1               |
|                     | -  If CBL model is set to run for   |
|                     | DOY 175–177, CBLday(175) = 1,       |
|                     | CBLday(176) = 1, CBLday(177) =      |
|                     | 1                                   |
+---------------------+-------------------------------------+
| CO2_included        | Set to zero in current version      |
+---------------------+-------------------------------------+
| InitialData_use     | Determines initial values (see      |
|                     | CBL_Initial_data.txt)               |
+---------------------+-------------------------------------+
| Value               | Comments                            |
+---------------------+-------------------------------------+
| 0                   | All initial values are              |
|                     | calculated. (Not available in       |
|                     | current release.)                   |
+---------------------+-------------------------------------+
| 1                   | Take zi0, gamt_Km and gamq_gkgm     |
|                     | from input data file. Theta+_K,     |
|                     | q+_gkg, Theta_K and q_gkg are       |
|                     | calculated using Temp_C, avrh and   |
|                     | Pres_kPa in meteorological input    |
|                     | file.                               |
+---------------------+-------------------------------------+
| 2                   | Take all initial values from        |
|                     | input data file (see                |
|                     | CBL_Initial_data.txt).              |
+---------------------+-------------------------------------+
| InitialDataFileName | If InitialData_use ≥ 1, write the   |
|                     | file name including the path from   |
|                     | site directory e.g.                 |
|                     | InitialDataFileName='CBLinputfile   |
|                     | s\CBL_initial_data.txt'             |
+---------------------+-------------------------------------+
| Sondeflag           |                                     |
+---------------------+-------------------------------------+
| Value               | Comments                            |
+---------------------+-------------------------------------+
| 0                   | Does not read radiosonde vertical   |
|                     | profile data -**recommended**       |
+---------------------+-------------------------------------+
| 1                   | Reads radiosonde vertical profile   |
|                     | data                                |
+---------------------+-------------------------------------+
| FileSonde(id)       | If Sondeflag=1, write the file      |
|                     | name including the path from site   |
|                     | directory e.g. FileSonde(id)=       |
|                     | 'CBLinputfiles\XXX.txt', XXX is     |
|                     | an arbitrary name.                  |
+---------------------+-------------------------------------+
|                     |                                     |
+---------------------+-------------------------------------+