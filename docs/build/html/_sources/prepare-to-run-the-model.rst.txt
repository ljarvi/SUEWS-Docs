Preparing to run the model
--------------------------

The following is to help with the model setup. Note that there is a
version of SUEWS in `UMEP <http://urban-climate.net/umep/UMEP_Manual>`__
and there are some starting
`tutorials <http://urban-climate.net/umep/UMEP_Manual#Tutorials>`__ for
that. The version there is the same (i.e. the executable) as the
standalone version so you can swap to that later once you have some
familiarity.

Preparatory reading
~~~~~~~~~~~~~~~~~~~

Read the manual and relevant papers (and references therein):

-  Järvi L, Grimmond CSB & Christen A (2011) The Surface Urban Energy
   and Water Balance Scheme (SUEWS): Evaluation in Los Angeles and
   Vancouver. J. Hydrol. 411, 219-237.
   `doi:10.1016/j.jhydrol.2011.10.00 <http://www.sciencedirect.com/science/article/pii/S0022169411006937>`__
-  Järvi L, Grimmond CSB, Taka M, Nordbo A, Setälä H & Strachan IB
   (2014) Development of the Surface Urban Energy and Water balance
   Scheme (SUEWS) for cold climate cities. Geosci. Model Dev. 7,
   1691-1711.
   `doi:10.5194/gmd-7-1691-2014 <http://www.geosci-model-dev.net/7/1691/2014/>`__
-  Ward HC, Kotthaus S, Järvi L and Grimmond CSB (2016) Surface Urban
   Energy and Water Balance Scheme (SUEWS): development and evaluation
   at two UK sites. Urban Climate 18, 1-32.
   `doi:10.1016/j.uclim.2016.05.001 <http://www.sciencedirect.com/science/article/pii/S2212095516300256/>`__

`See other publications with example
applications <http://urban-climate.net/umep/SUEWS#Recent_publications>`__

Decide what type of model run you are interested in
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+--------------------------------------------+---------------------------+
|                                            | Available in this release |
+============================================+===========================+
| LUMPS                                      | Yes – not standalone      |
+--------------------------------------------+---------------------------+
| SUEWS at a point or for an individual area | Yes                       |
+--------------------------------------------+---------------------------+
| SUEWS for multiple grids or areas          | Yes                       |
+--------------------------------------------+---------------------------+
| SUEWS with Boundary Layer (BL)             | Yes                       |
+--------------------------------------------+---------------------------+
| SUEWS with snow                            | Yes                       |
+--------------------------------------------+---------------------------+
| SUEWS with SOLWEIG                         | No                        |
+--------------------------------------------+---------------------------+
| SUEWS with SOLWEIG and BL                  | No                        |
+--------------------------------------------+---------------------------+

Download the program and example data files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Visit the website to receive a link to download the program and example
data files. Select the appropriate compiled version of the model to
download. For windows there is an installation version which will put
the programs and all the files into the appropriate place. There is also
a version linked to QGIS:
`**UMEP** <http://urban-climate.net/umep/UMEP>`__.

Note, as the definition of long double precision varies between
computers (e.g. Mac vs Windows) slightly different results may occur in
the output files.

Test/example files are given for the London KCL site, 2011 data (denoted
Kc11)

In the following SS is the site code (e.g. Kc), ss the grid ID, YYYY the
year and tt the time interval.

+-----------------------+-----------------------+-----------------------+
| Filename              | Description           | Input/output          |
+=======================+=======================+=======================+
| SSss_data.txt         | Meteorological input  | Input                 |
|                       | file (60-min)         |                       |
+-----------------------+-----------------------+-----------------------+
| SSss_YYYY_data_5.txt  | Meteorological input  | Input                 |
|                       | file (5-min)          |                       |
+-----------------------+-----------------------+-----------------------+
| InitialConditionsSSss | Initial conditions    | Input                 |
| _YYYY.nml(+)          | file                  |                       |
+-----------------------+-----------------------+-----------------------+
| SUEWS_SiteInfo_SSss.x | Spreadsheet           | Input                 |
| lsm                   | containing all other  |                       |
|                       | input information     |                       |
+-----------------------+-----------------------+-----------------------+
| RunControl.nml        | Sets model run        | Input (located in     |
|                       | options               | main directory)       |
+-----------------------+-----------------------+-----------------------+
| SS_Filechoices.txt    | Summary of model run  | Output                |
|                       | options               |                       |
+-----------------------+-----------------------+-----------------------+
| SSss_YYYY_5.txt       | (Optional) 5-min      | Output                |
|                       | resolution output     |                       |
|                       | file                  |                       |
+-----------------------+-----------------------+-----------------------+
| SSss_YYYY_60.txt      | 60-min resolution     | Output                |
|                       | output file           |                       |
+-----------------------+-----------------------+-----------------------+
| SSss_DailyState.txt   | Daily state variables | Output                |
|                       | (all years in one     |                       |
|                       | file)                 |                       |
+-----------------------+-----------------------+-----------------------+
|  |
+-----------------------+-----------------------+-----------------------+

(+) There is a second file InitialConditionsSSss_YYYY_EndOfRun.nml or
InitialConditionsSSss_YYYY+1.nml in the input directory. At the end of
the run, and at the end of each year of the run, these files are written
out so that this information could be used to initialize further model
runs.

Run the model for example data
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Before running the model for your own data it is good to make certain
that you can run the test data and get the same results as in the
example files provided. It is recommended that you make a copy of the
example output files and put them somewhere else so you can compare the
results. When you run the program it will write over the supplied files.

To run the model you can use **Command Prompt** (in the directory where
the programme is located type the model name) or just double click the
executable file.

Please see `Troubleshooting <#Troubleshooting>`__ if you have problems
running the model.

Preparation of data
~~~~~~~~~~~~~~~~~~~

This section describes the information required to run SUEWS for your
site. The input data can be summarised as follows:

#. Continuous *meteorological forcing data* for the entire period to be
   modelled. Note you can not have gaps in the meteorological data. If
   you need help with preparing the data you may want to use some of the
   tools in
   `UMEP <http://urban-climate.net/umep/UMEP_Manual#Meteorological_Data:_MetPreprocessor>`__.
#. Knowledge of the *surface and soil conditions immediately before the
   start of the run* (if these initial conditions are not known, it is
   usually possible to determine suitable values by running the model
   and using the output at the end of the run to infer the conditions at
   the start of the run).
#. The *location of the site* (latitude, longitude, altitude).
#. Information about the *characteristics of the surface*, including
   land cover, heights of buildings and trees, radiative characteristics
   (e.g. albedo, emissivity), drainage characteristics, soil
   characteristics, snow characteristics, phenological characteristics
   (e.g. seasonal cycle of LAI).
#. Information about *human behaviour*, including energy use and water
   use (e.g. for irrigation or street cleaning) and snow clearing (if
   applicable). The anthropogenic energy use and water use may be
   provided as a time series in the meteorological forcing file if these
   data are available or modelled based on parameters provided to the
   model, including population density, hourly and weekly profiles of
   energy and water use, information about the proportion of properties
   using irrigation and the type of irrigation (automatic or manual).

It is particularly important to ensure the following input information
is appropriate and representative of the site:

-  Fractions of different land cover types and (less so) heights of
   buildings [28]_
-  Accurate meteorological forcing data, particularly precipitation and
   incoming shortwave radiation [29]_
-  Initial soil moisture conditions [30]_
-  Anthropogenic heat flux parameters, particularly if there are
   considerable energy emissions from transport, buildings, metabolism,
   etc [31]_
-  External water use (if irrigation or street cleaning occurs)
-  Snow clearing (if running the snow option)
-  Surface conductance parameterisation [32]_ [33]_

SUEWS can be run either for an individual area or for multiple areas.
There is no requirement for the areas to be of any particular shape but
here we refer to them as model 'grids'.

Preparation of site characteristics and model parameters
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The area to be modelled is described by a set of characteristics that
are specified in the `SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__
file. Each row corresponds to one model grid for one year (i.e. running
a single grid over three years would require three rows; running two
grids over two years would require four rows). Characteristics are often
selected by a code for a particular set of conditions. For example, a
specific soil type (links to `SUEWS_Soil.txt <#SUEWS_Soil.txt>`__) or
characteristics of deciduous trees in a particular region (links to
`SUEWS_Veg.txt <#SUEWS_Veg.txt>`__). The intent is to build a library of
characteristics for different types of urban areas. The codes are
specified by the user, must be integer values and must be unique within
the first column of each input file, otherwise the model will return an
error. (Note in `SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__ the
first column is labelled 'Grid' and can contain repeat values for
different years.) See `Input files <#Input_files>`__ for details. Note
`UMEP <http://urban-climate.net/umep/UMEP>`__ maybe helpful for
components of this.

Land cover
''''''''''

For each grid, the land cover must be classified using the following
surface types:

+-----------------+-----------------+-----------------+-----------------+
| Classification  | Surface type    | File where      |
|                 |                 | characteristics |
|                 |                 | are specified   |
+=================+=================+=================+
| Non-vegetated   | Paved surfaces  | [[#SUEWS_NonVeg | SUEWS_NonVeg.tx |
|                 |                 | .txt            | t]]             |
+-----------------+-----------------+-----------------+-----------------+
|                 | Building        | [[#SUEWS_NonVeg | SUEWS_NonVeg.tx |
|                 | surfaces        | .txt            | t]]             |
+-----------------+-----------------+-----------------+-----------------+
|                 | Bare soil       | [[#SUEWS_NonVeg | SUEWS_NonVeg.tx |
|                 | surfaces        | .txt            | t]]             |
+-----------------+-----------------+-----------------+-----------------+
| Vegetation      | Evergreen trees | [[#SUEWS_Veg.tx | SUEWS_Veg.txt]] |
|                 | and shrubs      | t               |                 |
+-----------------+-----------------+-----------------+-----------------+
|                 | Deciduous trees | [[#SUEWS_Veg.tx | SUEWS_Veg.txt]] |
|                 | and shrubs      | t               |                 |
+-----------------+-----------------+-----------------+-----------------+
|                 | Grass           | [[#SUEWS_Veg.tx | SUEWS_Veg.txt]] |
|                 |                 | t               |                 |
+-----------------+-----------------+-----------------+-----------------+
| Water           | Water           | [[#SUEWS_Water. | SUEWS_Water.txt |
|                 |                 | txt             | ]]              |
+-----------------+-----------------+-----------------+-----------------+
| Snow            | Snow            | [[#SUEWS_Snow.t | SUEWS_Snow.txt] |
|                 |                 | xt              | ]               |
+-----------------+-----------------+-----------------+-----------------+
|  |
+-----------------+-----------------+-----------------+-----------------+

The surface cover fractions (i.e. proportion of the grid taken up by
each surface) must be specified in
`SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__. The surface cover
fractions are **critical**, so make certain that the different surface
cover fractions are appropriate for your site.

For some locations, land cover information may be already available
(e.g. from various remote sensing resources). If not, websites like Bing
Maps and Google Maps allow you to see aerial images of your site and can
be used to estimate the relative proportion of each land cover type. If
detailed spatial datasets are available,
`UMEP <http://urban-climate.net/umep/UMEP>`__ allows for a direct link
to a GIS environment using QGIS.

.. _anthropogenic-heat-flux-qf-1:

Anthropogenic heat flux (Q:sub:`F`)
'''''''''''''''''''''''''''''''''''

You can either model Q\ :sub:`F` within SUEWS or provide it as an input.

-  To model it population density is needed as an input for LUMPS and
   SUEWS to calculate Q\ :sub:`F`.
-  If you have no information about the population of the site we
   recommend that you use the LUCY model [34]_  [35]_ to estimate the
   anthropogenic heat flux which can then be provided as input SUEWS
   along with the meteorological forcing data. The LUCY model can be
   downloaded from `here <http://micromet.reading.ac.uk/>`__.

Alternatively, you can use the updated version of LUCY called
`LQF <http://urban-climate.net/umep/LQF_Manual>`__, which is included in
`UMEP <http://urban-climate.net/umep/UMEP>`__.

Other information
'''''''''''''''''

The surface cover fractions and population density can have a major
impact on the model output. However, it is important to consider the
suitability of all parameters for your site. Using inappropriate
parameters may result in the model returning an error or, worse,
generating output that is simply not representative of your site. Please
read the section on `Input files <#Input_files>`__. Recommended or
reasonable ranges of values are suggested for some parameters, along
with important considerations for how to select appropriate values for
your site.

Data Entry
''''''''''

To create the series of input text files describing the characteristics
of your site, there are three options:

#. Data can be entered directly into the input text files. The example
   (.txt) files provide a template to create your own files which can be
   edited with a `text editor <#A_text_editor>`__ directly.
#. Data can be entered into the spreadsheet **SUEWS_SiteInfo.xlsm** and
   the input text files generated by running the macro.
#. Use [http://urban-climate.net/umep/UMEP\ \| UMEP].

**To run the xlsm macro:** Enter the data for your site into the xlsm
spreadsheet **SUEWS_SiteInfo.xlsm** and then use the macro to create the
text files which will appear the same directory.

If there is a problem

-  Make sure none of the text files to be generated are open.
-  It is recommended to close the spreadsheet before running the actual
   model code.

Note that in all txt files:

-  The first two rows are headers. The first row is the column number;
   the second row is the column name.
-  The names and order of the columns should not be altered from the
   templates, as these are checked by the model and errors will be
   returned if particular columns cannot be found.
-  Since v2017a it is no longer necessary for the meteorological forcing
   data to have two rows with -9 in column 1 as their last two rows.
-  “!” indicates a comment, so any text following "!" on the same line
   will not be read by the model.
-  If data are unavailable or not required, enter the value -999 in the
   correct place in the input file.
-  Ensure the units are correct for all input information. See `Input
   files <#Input_files>`__ for a description of parameters.

In addition to these text files, the following files are also needed to
run the model.

Preparation of the RunControl file
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In the RunControl.nml file the site name (SS_) and directories for the
model input and output are given. This means **before running** the
model (even the with the example datasets) you must either

#. open the RunControl.nml file and edit the input and output file paths
   and the site name (with a `text editor <#A_text_editor>`__) so that
   they are correct for your setup, or
#. create the directories specified in the RunControl.nml file

From the given site identification the model identifies the input files
and generates the output files. For example if you specify

| **``FileOutputPath``\ ````\ ``=``\ ````\ ``“C:\FolderName\SUEWSOutput\”``**\ `` and use site code SS the model creates an output file``
| **``C:\FolderName\SUEWSOutput\SSss_YYYY_TT.txt``**\ `` (remember to add the last backslash in windows and slash in Linux/Mac).``

If the file paths are not correct the program will return an error when
run (see `error messages <#Error_messages:_problems.txt>`__) and write
the error to the problems.txt file.

Preparation of the Meteorological forcing data
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The model time-step is specified in `RunControl.nml <#RunControl.nml>`__
(5 min is highly recommended). If meteorological forcing data are not
available at this resolution, SUEWS has the option to downscale (e.g.
hourly) data to the time-step required. See details about the
`meteorological forcing data <#SSss_YYYY_data_tt.txt>`__ to learn more
about choices of data input. Each grid can have its own meteorological
forcing file, or a single file can be used for all grids. The forcing
data should be representative of the local-scale, i.e. collected (or
derived) above the height of the roughness elements (buildings and
trees).

Preparation of the InitialConditions file
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Information about the surface state and meteorological conditions just
before the start of the run are provided in the Initial Conditions file.
At the very start of the run, each grid can have its own Initial
Conditions file, or a single file can be used for all grids. For details
see `InitialConditions <#InitialConditions>`__.

Run the model for your site
~~~~~~~~~~~~~~~~~~~~~~~~~~~

To run the model you can use **Command Prompt** (in the directory where
the programme is located type the model name) or just double click the
executable file.

Please see `Troubleshooting <#Troubleshooting>`__ if you have problems
running the model.

Analyse the output
~~~~~~~~~~~~~~~~~~

It is a good idea to perform initial checks that the model output looks
reasonable.

+-----------------------+-----------------------+-----------------------+
| Characteristic        | Things to check       |
+=======================+=======================+
| Leaf area index       | Does the phenology    |
|                       | look appropriate      |
|                       | (i.e. what does the   |
|                       | seasonal cycle of     |
|                       | `leaf area index      |
|                       | (LAI) <http://glossar |
|                       | y.ametsoc.org/wiki/Le |
|                       | af_area_index>`__     |
|                       | look like?)           |
|                       |                       |
|                       | -  Are the leaves on  |
|                       |    the trees at       |
|                       |    approximately the  |
|                       |    right time of the  |
|                       |    year?              |
+-----------------------+-----------------------+-----------------------+
| Kdown                 | Is the timing of the  | SUEWS_SiteSelect.txt] |
|                       | diurnal cycle correct | ].                    |
|                       | for the incoming      |                       |
|                       | solar radiation?      | -  Checking solar     |
|                       |                       |    angles (zenith and |
|                       | \*Although Kdown is a |    azimuth) can also  |
|                       | required input, it is |    be a useful check  |
|                       | also included in the  |    that the timing is |
|                       | output file. It is a  |    correct.           |
|                       | good idea to check    |                       |
|                       | that the timing of    |                       |
|                       | Kdown in the output   |                       |
|                       | file is appropriate,  |                       |
|                       | as problems can       |                       |
|                       | indicate errors with  |                       |
|                       | the timestamp,        |                       |
|                       | incorrect time        |                       |
|                       | settings or problems  |                       |
|                       | with the              |                       |
|                       | disaggregation. In    |                       |
|                       | particular, make sure |                       |
|                       | the sign of the       |                       |
|                       | longitude is          |                       |
|                       | specified correctly   |                       |
|                       | in                    |                       |
|                       | [[#SUEWS_SiteSelect.t |                       |
|                       | xt                    |                       |
+-----------------------+-----------------------+-----------------------+
| Albedo                | Is the bulk albedo    |
|                       | correct?              |
|                       |                       |
|                       | -  This is critical   |
|                       |    because a small    |
|                       |    error has an       |
|                       |    impact on all the  |
|                       |    fluxes (energy and |
|                       |    hydrology).        |
|                       | -  If you have        |
|                       |    measurements of    |
|                       |    outgoing shortwave |
|                       |    radiation compare  |
|                       |    these with the     |
|                       |    modelled values.   |
|                       | -  How do the values  |
|                       |    compare to         |
|                       |    literature values  |
|                       |    for your area?     |
+-----------------------+-----------------------+-----------------------+
|  |
+-----------------------+-----------------------+-----------------------+

Summary of files
~~~~~~~~~~~~~~~~

The table below lists the files required to run SUEWS and the output
files produced. SS is the two-letter code (specified in RunControl)
representing the site name, ss is the grid identification (integer
values between 0 and 2,147,483,647 (largest 4-byte integer)) and YYYY is
the year. TT is the resolution of the input/output file and tt is the
model time-step.

The last column indicates whether the files are needed/produced once per
run (1/run), or once per day (1/day), for each year (1/year) or for each
grid (1/grid).

| ``[B] indicates files used with the CBL part of SUEWS (BLUEWS) and therefore are only needed/produced if this option is selected``
| ``[E] indicates files associated with ESTM storage heat flux models and therefore are only needed/produced if this option is selected``

+-------------+-------------+-------------+-------------+-------------+
| Filename    | Description | Location    | Option      |
+=============+=============+=============+=============+
| **Program** |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_V2017 | SUEWS       | Directory   |             |
| b.exe       | executable  | where the   |             |
|             |             | program     |             |
|             |             | will run    |             |
+-------------+-------------+-------------+-------------+-------------+
| [[#Input    | **Input     |             |             |             |
| files       | files**]]   |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
| RunControl. | Specifies   | Same        | 1/run       |
| nml         | options for | directory   |             |
|             | the model   | as          |             |
|             | run         | executable  |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_SiteS | Main input  | Input       | 1/run       |
| elect.txt   | file for    | directory   |             |
|             | this site   |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_NonVe | Inputs for  | Input       | 1/run       |
| g.txt       | non-vegetat | directory   |             |
|             | ed          |             |             |
|             | surfaces    |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Veg.t | Inputs for  | Input       | 1/run       |
| xt          | vegetated   | directory   |             |
|             | surfaces    |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Water | Inputs for  | Input       | 1/run       |
| .txt        | water       | directory   |             |
|             | surfaces    |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Snow. | Inputs for  | Input       | 1/run       |
| txt         | snow        | directory   |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Soil. | Inputs for  | Input       | 1/run       |
| txt         | sub-surface | directory   |             |
|             | soil        |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Anthr | Inputs for  | Input       | 1/run       |
| opogenicHea | anthropogen | directory   |             |
| t.txt       | ic          |             |             |
|             | heat flux   |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Irrig | Inputs for  | Input       | 1/run       |
| ation.txt   | irrigation  | directory   |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Profi | Inputs for  | Input       | 1/run       |
| les.txt     | hourly      | directory   |             |
|             | profiles    |             |             |
|             | (energy     |             |             |
|             | use, water  |             |             |
|             | use,        |             |             |
|             | snow-cleari |             |             |
|             | ng)         |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Withi | Inputs      | Input       | 1/run       |
| nGridWaterD | describing  | directory   |             |
| ist.txt     | within-grid |             |             |
|             | water       |             |             |
|             | distributio |             |             |
|             | n           |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_OHMCo | Inputs for  | Input       | 1/run       |
| efficients. | OHM         | directory   |             |
| txt         | coefficient |             |             |
|             | s           |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_Condu | Inputs for  | Input       | 1/run       |
| ctance.txt  | surface     | directory   |             |
|             | conductance |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_SiteI | (Optional)  | Anywhere,   | -           |
| nfo.xlsm    | spreadsheet | but the     |             |
|             | for         | input files |             |
|             | creating    | created     |             |
|             | input files | must be in  |             |
|             |             | the input   |             |
|             |             | directory   |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_YYYY_d | Meteorologi | Input       | 1/grid/year |
| ata_tt.txt  | cal         | directory   | or 1/year   |
| /           | input file  |             |             |
| SSss_YYYY_d | at model    |             |             |
| ata_TT.txt  | time-step   |             |             |
|             | (tt) /      |             |             |
|             | lower       |             |             |
|             | resolution  |             |             |
|             | (TT)        |             |             |
+-------------+-------------+-------------+-------------+-------------+
| InitialCond | Initial     | Input       | 1/grid/run  |
| itionsSSss_ | conditions  | directory   | or 1/run    |
| YYYY.nml    | file        |             |             |
+-------------+-------------+-------------+-------------+-------------+
| ESTMinput.n | Specifies   | Input       | 1/run [E]   |
| ml          | options and | directory   |             |
|             | inputs for  |             |             |
|             | ESTM model  |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SUEWS_ESTMC | Inputs for  | Input       | 1/run [E]   |
| oefficients | ESTM        | directory   |             |
| .txt        | coefficient |             |             |
|             | s           |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_YYYY_E | Surface     | Input       | 1/grid/year |
| STM_Ts_data | temperature | directory   | or 1/year   |
| _tt.txt     | data input  |             | [E]         |
|             | file at     |             |             |
|             | model       |             |             |
|             | time-step   |             |             |
|             | (tt) /      |             |             |
|             | lower       |             |             |
|             | resolution  |             |             |
|             | (TT)        |             |             |
+-------------+-------------+-------------+-------------+-------------+
| CBLinput.nm | Specifies   | Input       | 1/run [B]   |
| l           | options and | directory   |             |
|             | inputs for  |             |             |
|             | CBL model   |             |             |
+-------------+-------------+-------------+-------------+-------------+
| CBL_initial | Initial     | Input       | 1/day [B]   |
| _data.txt   | data for    | directory   |             |
|             | CBL model   |             |             |
+-------------+-------------+-------------+-------------+-------------+
| [[#Output   | **Output    |             |             |             |
| files       | files**]]   |             |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_YYYY_t | Model       | Output      | 1/grid/year |
| t.txt       | output at   | directory   |             |
|             | model       |             |             |
|             | time-step   |             |             |
|             | (optional)  |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_YYYY_T | Model       | Output      | 1/grid/year |
| T.txt       | output at   | directory   |             |
|             | resolution  |             |             |
|             | specified   |             |             |
|             | by          |             |             |
|             | ResolutionF |             |             |
|             | ilesOut     |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_DailyS | Status at a | Output      | 1/grid      |
| tate.txt    | daily time  | directory   |             |
|             | step        |             |             |
+-------------+-------------+-------------+-------------+-------------+
| InitialCond | New         | Input       | 1/grid/year |
| itionsSSss_ | InitialCond | directory   |             |
| YYYY+1.nml  | itions      |             |             |
|             | file        |             |             |
|             | written for |             |             |
|             | each grid   |             |             |
|             | at the end  |             |             |
|             | of each     |             |             |
|             | year for    |             |             |
|             | multi-year  |             |             |
|             | runs. If    |             |             |
|             | the run     |             |             |
|             | finishes    |             |             |
|             | before the  |             |             |
|             | end of the  |             |             |
|             | year the    |             |             |
|             | InitialCond |             |             |
|             | itions      |             |             |
|             | file is     |             |             |
|             | still       |             |             |
|             | written and |             |             |
|             | the file    |             |             |
|             | name is     |             |             |
|             | appended    |             |             |
|             | with        |             |             |
|             | '_EndofRun' |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SS_FileChoi | Summary of  | Output      | 1/run       |
| ces.txt     | model run   | directory   |             |
|             | options     |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SS_YYYY_TT_ | Describes   | Output      | 1/run       |
| OutputForma | header,     | directory   |             |
| t.txt       | units and   |             |             |
|             | formatting  |             |             |
|             | of the main |             |             |
|             | output file |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_YYYY_E | Model       | Output      | 1/grid/year |
| STM_tt.txt  | output at   | directory   | [E]         |
|             | model       |             |             |
|             | time-step   |             |             |
|             | (optional)  |             |             |
+-------------+-------------+-------------+-------------+-------------+
| SSss_YYYY_E | Model       | Output      | 1/grid/year |
| STM_TT.txt  | output at   | directory   | [E]         |
|             | resolution  |             |             |
|             | specified   |             |             |
|             | by          |             |             |
|             | ResoltuionF |             |             |
|             | ilesOut     |             |             |
+-------------+-------------+-------------+-------------+-------------+
| problems.tx | Contains    | Same        | 1/run       |
| t           | details of  | directory   |             |
|             | serious     | as          |             |
|             | errors      | executable  |             |
|             | encountered |             |             |
|             | in the      |             |             |
|             | model run   |             |             |
+-------------+-------------+-------------+-------------+-------------+
| warnings.tx | List of     | Same        | 1/run       |
| t           | potential   | directory   |             |
|             | issues      | as          |             |
|             | encountered | executable  |             |
|             | in the      |             |             |
|             | model run   |             |             |
+-------------+-------------+-------------+-------------+-------------+
|  |
+-------------+-------------+-------------+-------------+-------------+
| CBL_id.txt  | CBL model   | Output      | 1/day [B]   |
|             | output file | directory   |             |
|             | for day of  |             |             |
|             | year id     |             |             |
+-------------+-------------+-------------+-------------+-------------+
