.. _version_history:

Version History
===============

.. _new_latest:

.. _new_2018a:

New in SUEWS Version 2018a
--------------------------

#. Many under-the-hood improvements
#. New Manual

.. _new_2017b:

New in SUEWS Version 2017b (released 2 August 2017)
---------------------------------------------------

:download:`PDF Manual for v2017b <assets/doc/SUEWS_V2017b_Manual.pdf>`

#. Surface-level diagnostics: T2 (air temperature at 2 m agl), Q2 (air
   specific humidity at 2 m agl) and U10 (wind speed at 10 m agl) added
   as default output.
#. Output in netCDF format. Please note this feature is **NOT** enabled
   in the public release due to the dependency of netCDF library.
   Assistance in enabling this feature may be requested to the
   development team via `SUEWS mail
   list <https://www.lists.reading.ac.uk/mailman/listinfo/met-suews>`__.
#. Edits to the manual.
#. New capabilities being developed, including two new options for
   calculating storage heat flux (AnOHM, ESTM) and modelling of carbon
   dioxide fluxes. These are currently under development and **should
   not be used** in v2017b.
#. Known issues

   #. BLUEWS parameters need to be checked
   #. Observed soil moisture can not be used as an input
   #. Wind direction is not currently downscaled so non -999 values will
      cause an error.

New in SUEWS Version 2017a (Feb 2017)
-------------------------------------

#. Changes to input file formats (including RunControl.nml and
   InitialConditions files) to facilitate setting up and running the
   model. Met forcing files no longer need two rows of -9 at the end to
   indicate the end of the file.
#. Changes to output file formats (now option to write out only a subset
   of variables, rather than all variables).
#. SUEWS can now disaggregate forcing files to the model time-step and
   aggregate output at the model time-step to lower resolution. This
   removes the need for the python wrapper used with previous versions.
#. InitialConditions format and requirements changed. A single file can
   now be provided for multiple grids. SUEWS will approximate most (but
   not all) of the required initial conditions if values are unknown.
   (However, if detailed information about the initial conditions is
   known, this can still be provided to and used by SUEWS.)
#. Leaf area index calculations now use parameters provided for each
   vegetated surface (previously only the deciduous tree LAI development
   parameters were applied to all vegetated surfaces).
#. For compatibility with GIS, **the sign convention for longitude has
   been changed**. Now negative values are to the west, positive values
   are to the east. Note this appears to have been incorrectly coded in
   previous versions (but may not necessarily have been problematic).
#. Storage heat flux calculation adapted for shorter (sub-hourly) model
   time-step: hysteresis calculation now based on running means over the
   previous hour.
#. Improved error handling, including separate files for serious errors
   (problems.txt) and less critical issues (warnings.txt).
#. Edits to the manual.
#. New capabilities being developed, including two new options for
   calculating storage heat flux (AnOHM, ESTM) and modelling of carbon
   dioxide fluxes. These are currently under development and **should
   not be used** in v2017a.

New in SUEWS Version 2016a (released 21 June 2016)
--------------------------------------------------

:download:`PDF Manual for v2016a <assets/doc/SUEWS_V2016a_Manual.pdf>`

#. Major changes to the input file formats to facilitate the running of
   multiple grids and multiple years. Surface characteristics are
   provided in SiteSelect.txt and other input files are cross-referenced
   via codes or profile types.
#. The surface types have been altered:

   -  Previously, grass surfaces were entered separately as irrigated
      grass and unirrigated grass surfaces, whilst the ‘unmanaged’ land
      cover fraction was assumed by the model to behave as unirrigated
      grass. There is now a single surface type for grass (total for
      irrigated plus unirrigated) and a new bare soil surface type.
   -  The proportion of irrigated vegetation must now be specified for
      grass, evergreen trees and deciduous trees individually.

#. The entire model now runs at a time step specified by the user. Note
   that 5 min is strongly recommended. (Previously only the water
   balance calculations were done at 5 min with the energy balance
   calculations at 60 min).
#. Surface conductance now depends on the soil moisture under the
   vegetated surfaces only (rather than the total soil moisture for the
   whole study area as previously).
#. Albedo of evergreen trees and grass surfaces can now change with leaf
   area index as was previously possible for deciduous trees only.
#. New suggestions in Troubleshooting section.
#. Edits to the manual.
#. CBL model included.
#. SUEWS has been incorporated into `UMEP <http://umep-docs.readthedocs.io/>`_

New in SUEWS Version 2014b (released 8 October 2014)
----------------------------------------------------

:download:`PDF Manual for v2014b <assets/doc/SUEWS_V2014b_Manual.pdf>`

These affect the run configuration if previously run with older versions
of the model:

#. New input of three additional columns in the Meteorological input
   file (diffusive and direct solar radiation, and wind direction)
#. Change of input variables in InitialConditions.nml file. Note we now
   refer to CT as ET (ie. Evergreen trees rather than coniferous trees)
#. In GridConnectionsYYYY.txt, the site names should now be without the
   underscore (e.g ``Sm`` and not ``Sm_``)

Other issues:

#. Number of grid areas that can be modelled (for one grid, one year
   120; for one grid two years 80)
#. Comment about Time interval of input data
#. Bug fix: Column headers corrected in 5 min file
#. Bug fix: Surface state 60 min file - corrected to give the last 5 min
   of the hour (rather than cumulating through the hour)
#. Bug fix: units in the Horizontal soil water transfer
#. ErrorHints: More have been added to the problems.txt file.
#. Manual: new section on running the model appropriately
#. Manual: notation table updated
#. Possibility to add snow accumulation and melt: new paper

Järvi L, Grimmond CSB, Taka M, Nordbo A, Setälä H, and Strachan IB 2014:
Development of the Surface Urban Energy and Water balance Scheme (SUEWS)
for cold climate cities, Geosci. Model Dev. 7, 1691-1711,
doi:10.5194/gmd-7-1691-2014.

New in SUEWS Version 2014a.1 (released 26 February 2014)
--------------------------------------------------------

#. Please see the large number of changes made in the 2014a release.
#. This is a minor change to address installing the software.
#. Minor updates to the manual

New in SUEWS Version 2014a (released 21 February 2014)
------------------------------------------------------

#. Bug fix: External irrigation is calculated as combined from automatic
   and manual irrigation and during precipitation events the manual
   irrigation is reduced to 60% of the calculated values. In previous
   version of the model, the irrigation was in all cases taken 60% of
   the calculated value, but now this has been fixed.
#. In previous versions of the model, irrigation was only allowed on the
   irrigated grass surface type. Now, irrigation is also allowed on
   evergreen and deciduous trees/shrubs surfaces. These are not however
   treated as separate surfaces, but the amount of irrigation is evenly
   distributed to the whole surface type in the modelled area. The
   amount of water is calculated using same equation as for grass
   surface (equation 5 in Järvi et al. 2011), and the fraction of
   irrigated trees/shrubs (relative to the area of tree/shrubs surface)
   is set in the gis file (See Table 4.11: SSss_YYYY.gis)
#. In the current version of the model, the user is able to adjust the
   leaf-on and leaf-off lengths in the FunctionalTypes. nml file. In
   addition, user can choose whether to use temperature dependent
   functions or combination of temperature and day length (advised to be
   used at high-latitudes)
#. In the gis-file, there is a new variable Alt that is the area
   altitude above sea level. If not known exactly use an approximate
   value.
#. Snow removal profile has been added to the
   HourlyProfileSSss_YYYY.txt. Not yet used!
#. Model time interval has been changed from minutes to seconds.
   Preferred interval is 3600 seconds (1 hour)
#. Manual correction: input variable Soil moisture said soil moisture
   deficit in the manual – word removed
#. Multiple compiled versions of SUEWS released. There are now users in
   Apple, Linux and Windows environments. So we will now release
   compiled versions for more operating systems (section 3).
#. There are some changes in the output file columns so please, check
   the respective table of each used output file.
#. Bug fix: with very small amount of vegetation in an area – impacted
   Phenology for LUMPS

New in SUEWS Version 2013a
--------------------------

#. Radiation selection bug fixed
#. Aerodynamic resistance – when very low - no longer reverts to neutral
   (which caused a large jump) – but stays low
#. Irrigation day of week fixed
#. New error messages
#. min file – now includes a decimal time column – see Section 5.4 –
   Table 5.3

New in SUEWS Version 2012b
--------------------------

#. Error message generated if all the data are not available for the
   surface resistance calculations
#. Error message generated if wind data are below zero plane
   displacement height.
#. All error messages now written to ‘Problem.txt’ rather than embedded
   in an ErrorFile. Note some errors will be written and the program
   will continue others will stop the program.
#. Default variables removed (see below). Model will stop if any data
   are problematic. File should be checked to ensure that reasonable
   data are being used. If an error occurs when there should not be one
   let us know as it may mean we have made the limits too restrictive.

Contents no longer used File defaultFcld=0.1 defaultPres=1013
defaultRH=50 defaultT=10 defaultU=3 RunControl.nml

-  Just delete lines from file
-  Values you had were likely different from these example value shown
   here

New in SUEWS Version 2012a
--------------------------

#. Improved error messages when an error is encountered. Error message
   will generally be written to the screen and to the file
   ‘problems.txt’
#. Format of all input files have changed.
#. New excel spreadsheet and R programme to help prepare required data
   files. (Not required)
#. Format of coef flux (OHM) input files have changed.

   -  This allows for clearer identification for users of the
      coefficients that are actually to be used
   -  This requires an additional file with coefficients. These do not
      need to be adjusted but new coefficients can be added. We would
      appreciate receiving additional coefficients so they can be
      included in future releases – Please email Sue.

#. Storage heat flux (OHM) coefficients can be changed by

   -  time of year (summer, winter)
   -  surface wetness state

#. New files are written: DailyState.txt

   -  Provides the status of variables that are updated on a daily or
      basis or a snapshot at the end of each day.

#. Surface Types

   -  Clarification of surface types has been made. See GIS and OHM
      related files

New in SUEWS Version2011b
-------------------------

#. Storage heat flux (ΔQs) and anthropogenic heat flux (QF) can be set
   to be 0 W |m^-2|
#. Calculation of hydraulic conductivity in soil has been improved and
   HydraulicConduct in SUEWSInput.nml is replaced with name
   SatHydraulicConduct
#. Following removed from HeaderInput.nml

   -  HydraulicConduct
   -  GrassFractionIrrigated
   -  PavedFractionIrrigated
   -  TreeFractionIrrigated

The lower three are now determined from the water use behaviour used in
SUEWS

#. Following added to HeaderInput.nml

   -  SatHydraulicConduct
   -  defaultQf
   -  defaultQs

#. If ΔQs and QF are not calculated in the model but are given as an
   input, the missing data is replaced with the default values.
#. Added to SAHP input file

   -  AHDIUPRF – diurnal profile used if AnthropHeatChoice = 1

V2012a this became obsolete OHM file (SSss_YYYY.ohm)
