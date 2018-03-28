Meteorological Input File
-------------------------

SUEWS is designed to run using commonly measured meteorological
variables.

-  Required inputs must be continuous – i.e. **gap fill** any missing
   data.
-  The table below gives the required (R) and optional (O) additional
   input variables.
-  If an optional input variable is not available or will not be used by
   the model, enter ‘-999.0’ for this column.
-  Since v2017a forcing files no longer need to end with two rows
   containing ‘-9’ in the first column.

-  One single meteorological file can be used for all grids
   (**MultipleMetFiles=0** in `RunControl.nml <#RunControl.nml>`__, no
   grid number in file name) if appropriate for the study area, or
-  separate met files can be used for each grid if data are available
   (**MultipleMetFiles=1** in `RunControl.nml <#RunControl.nml>`__,
   filename includes grid number).

-  The meteorological forcing file names should be appended with the
   temporal resolution in minutes (SS_YYYY_data_tt.txt, or
   SSss_YYYY_data_tt.txt for multiple grids).

-  Separate met forcing files should be provided for each year.
-  Files do not need to start/end at the start/end of the year, but they
   must contain a whole number of days.
-  The meteorological input file should match the information given in
   `SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__.
-  If a *partial year* is used that specific year must be given in
   SUEWS_SiteSelect.txt.
-  If *multiple years* are used, all years should be included in
   SUEWS_SiteSelect.txt.
-  If a *whole year* (e.g. 2011) is intended to be modelled using and
   hourly resolution dataset, the number of lines in the met data file
   should be 8760 and begin and end with::

     iy     id  it  imin
     2011   1   1   0 …
     …
     2012   1   0   0 …


.. _SSss_YYYY_data_tt.txt:

SSss_YYYY_data_tt.txt
~~~~~~~~~~~~~~~~~~~~~

Main meteorological data file.

+-----+-----+-------------+------------------+
| No. | Use | Column name | Description      |
+=====+=====+=============+==================+
| 1   | R   | iy          | Year [YYYY]      |
+-----+-----+-------------+------------------+
| 2   | R   | id          | Day of year      |
|     |     |             | [DOY]            |
+-----+-----+-------------+------------------+
| 3   | R   | it          | Hour [H]         |
+-----+-----+-------------+------------------+
| 4   | R   | imin        | Minute [M]       |
+-----+-----+-------------+------------------+
| 5   | O   | qn          | Net              |
|     |     |             | all-wave         |
|     |     |             | radiation        |
|     |     |             | [W               |
|     |     |             | m^-2 ]           |
|     |     |             | -  Required      |
|     |     |             | if               |
|     |     |             | **NetRad         |
|     |     |             | iationMetho      |
|     |     |             | d**              |
|     |     |             | = 1.             |
+-----+-----+-------------+------------------+
| 6   | O   | qh          | Sensible         |
|     |     |             | heat flux        |
|     |     |             | [W               |
|     |     |             | m^-2             |
|     |     |             | ]                |
+-----+-----+-------------+------------------+
| 7   | O   | qe          | Latent heat      |
|     |     |             | flux [W          |
|     |     |             | m^-2             |
|     |     |             | ]                |
+-----+-----+-------------+------------------+
| 8   | O   | qs          | Storage          |
|     |     |             | heat flux        |
|     |     |             | [W               |
|     |     |             | m^-2             |
|     |     |             | ]                |
+-----+-----+-------------+------------------+
| 9   | O   | qf          | Anthropogen      |
|     |     |             | ic               |
|     |     |             | heat flux        |
|     |     |             | [W               |
|     |     |             | m^-2             |
|     |     |             | ]                |
+-----+-----+-------------+------------------+
| 10  | R   | U           | Wind speed       |
|     |     |             | [m               |
|     |     |             | s^-1             |
|     |     |             | ]                |
|     |     |             | \*Height of      |
|     |     |             | the wind         |
|     |     |             | speed            |
|     |     |             | measurement      |
|     |     |             | (z) is           |
|     |     |             | needed in        |
|     |     |             | [[#SUEWS_Si      |
|     |     |             | teSelect.tx      |
|     |     |             | t]               |
+-----+-----+-------------+------------------+
| 11  | R   | RH          | Relative         |
|     |     |             | Humidity         |
|     |     |             | [%]              |
+-----+-----+-------------+------------------+
| 12  | R   | Tair        | Air              |
|     |     |             | temperature      |
|     |     |             | [°C]             |
+-----+-----+-------------+------------------+
| 13  | R   | pres        | Barometric       |
|     |     |             | pressure         |
|     |     |             | [kPa]            |
+-----+-----+-------------+------------------+
| 14  | R   | rain        | Rainfall         |
|     |     |             | [mm]             |
+-----+-----+-------------+------------------+
| 15  | R   | kdown       | Incoming         |
|     |     |             | shortwave        |
|     |     |             | radiation        |
|     |     |             | [W               |
|     |     |             | m^-2             |
|     |     |             | ]                |
|     |     |             | -  Must be > 0 W |
|     |     |             | m^-2.            |
+-----+-----+-------------+------------------+
| 16  | O   | snow        | Snow [mm]        |
|     |     |             | -  Required      |
|     |     |             | if               |
|     |     |             | **SnowUs         |
|     |     |             | e**              |
|     |     |             | = 1              |
+-----+-----+-------------+------------------+
| 17  | O   | ldown       | Incoming         |
|     |     |             | longwave         |
|     |     |             | radiation        |
|     |     |             | [W               |
|     |     |             | m^-2\ ]          |
+-----+-----+-------------+------------------+
| 18  | O   | fcld        | Cloud            |
|     |     |             | fraction         |
|     |     |             | [tenths]         |
+-----+-----+-------------+------------------+
| 19  | O   | Wuh         | External         |
|     |     |             | water use        |
|     |     |             | [m^-3 ]          |
+-----+-----+-------------+------------------+
| 20  | O   | xsmd        | Observed         |
|     |     |             | soil             |
|     |     |             | moisture         |
|     |     |             | [m^-3 m^-3       |
|     |     |             | ]                |
|     |     |             | or [kg           |
|     |     |             | kg^-1            |
|     |     |             | ]                |
+-----+-----+-------------+------------------+
| 21  | O   | lai         | Observed         |
|     |     |             | leaf area        |
|     |     |             | index            |
|     |     |             | [m^-2            |
|     |     |             | m^-2 ]           |
+-----+-----+-------------+------------------+
| 22  | O   | kdiff       | Diffuse          |
|     |     |             | radiation        |
|     |     |             | [W               |
|     |     |             | m^-2]            |
|     |     |             | -  Recommended   |
|     |     |             | if               |
|     |     |             | **SOLWEIGUse**   |
|     |     |             | = 1              |
+-----+-----+-------------+------------------+
| 23  | O   | kdir        | Direct           |
|     |     |             | radiation        |
|     |     |             | [W               |
|     |     |             | m^-2             |
|     |     |             | ]                |
|     |     |             | -  Recommended   |
|     |     |             | if               |
|     |     |             | **SOLWEIGUse**   |
|     |     |             | = 1              |
+-----+-----+-------------+------------------+
| 24  | O   | wdir        | Wind             |
|     |     |             | direction        |
|     |     |             | [°]              |
|     |     |             | -  Currently     |
|     |     |             | not              |
|     |     |             | implemented      |
+-----+-----+-------------+------------------+
