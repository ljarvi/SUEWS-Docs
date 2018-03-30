.. _SUEWS_Conductance.txt:

SUEWS_Conductance.txt
~~~~~~~~~~~~~~~~~~~~~

SUEWS_Conductance.txt contains the parameters needed for the Jarvis
(1976) surface conductance model used in the modelling of evaporation in
SUEWS. These values should **not** be changed independently of each
other. The suggested values below have been derived using datasets for
Los Angeles and Vancouver (see Järvi et al. (2011) [J11]_) and should be
used with `gsModel=1 <gsModel>`. An alternative formulation
(`gsModel=2 <gsModel>`) uses
slightly different functional forms and different coefficients (with
different units).

.. csv-table::
  :file: SUEWS_Conductance.csv
  :header-rows: 1
  :widths: 5 25 5 65
