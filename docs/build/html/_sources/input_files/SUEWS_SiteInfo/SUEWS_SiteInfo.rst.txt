
SUEWS_SiteInfo.xlsm
-------------------

The following text files provide SUEWS with information about the study
area.

.. toctree::
   :maxdepth: 1
   :glob:

   SUEWS*

.. toctree::
   :maxdepth: 1
   :hidden:
   Input_Options


These text files are stored as worksheets in
**SUEWS_SiteInfo.xlsm** and can be either edited using Excel and then
generated using the macro, or edited directly (see `Data
Entry <#Data_Entry>`__). Please note this file is subject to possible
changes from version to version due to new features, modifications, etc.
Please be aware of using the correct copy of this worksheet that are
always shipped with the SUEWS public release.

+-----+-----------------------------------+
| Use | Column                            |
+=====+===================================+
| MU  | Parameters which must be supplied |
|     | and must be specific for the      |
|     | site/grid being run.              |
+-----+-----------------------------------+
| MD  | Parameters which must be supplied |
|     | and must be specific for the      |
|     | site/grid being run (but default  |
|     | values may be ok if these values  |
|     | are not known specifically for    |
|     | the site).                        |
+-----+-----------------------------------+
| O   | Parameters that are optional,     |
|     | depending on the model settings   |
|     | in RunControl. Set any parameters |
|     | that are not used/not known to    |
|     | ‘-999’.                           |
+-----+-----------------------------------+
| L   | Codes that are used to link       |
|     | between the input files. These    |
|     | codes are required but their      |
|     | values are completely arbitrary,  |
|     | providing that they link the      |
|     | input files in the correct way.   |
|     | The user should choose these      |
|     | codes, bearing in mind that the   |
|     | codes they match up with in       |
|     | column 1 of the corresponding     |
|     | input file must be unique within  |
|     | that file. Codes must be          |
|     | integers. Note that the codes     |
|     | must match up with column 1 of    |
|     | the corresponding input file,     |
|     | even if those parameters are not  |
|     | used (in which case set all       |
|     | columns except column 1 to ‘-999’ |
|     | in the corresponding input file), |
|     | otherwise the model run will      |
|     | fail.                             |
+-----+-----------------------------------+
