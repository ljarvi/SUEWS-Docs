.. _SUEWS_AnthropogenicHeat.txt:

SUEWS_AnthropogenicHeat.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~~

SUEWS_AnthropogenicHeatFlux.txt provides the parameters needed to model
the anthropogenic heat flux using either the method of Järvi et al.
(2011) based on heating and cooling degree days (AnthropHeatMethod = 2
in 4.1 `RunControl.nml`) or the method of Loridan et
al. (2011) based on air temperature (AnthropHeatMethod = 1 in
`RunControl.nml`). The sub-daily variation in
anthropogenic heat flux is modelled according to the daily cycles
specified in SUEWS_Profiles.txt. Alternatively, if available, the
anthropogenic heat flux can be provided in the met forcing file (and set
AnthropHeatMethod = 0 in `RunControl.nml`), in which
case all columns here except Code and BaseTHDD should be set to ’-999’.


.. csv-table::
  :file: SUEWS_AnthropogenicHeat.csv
  :header-rows: 1
  :widths: auto
