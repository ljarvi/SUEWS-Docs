.. _SUEWS_Snow.txt:

SUEWS_Snow.txt
~~~~~~~~~~~~~~

SUEWS_Snow.txt specifies the characteristics for snow surfaces when
`SnowUse=1 <SnowUse>` in `RunControl.nml`. If the snow part of
the model is not run, fill this table with ‘-999’ except for the first
(Code) column and set `SnowUse=0 <SnowUse>` in `RunControl.nml`.
For a detailed description of the variables, see Järvi et al.
(2014) [Leena2014]_.

.. warning::
  In the current release `SnowUse` should be set to 0.


.. csv-table::
  :file: SUEWS_Snow.csv
  :header-rows: 1
  :widths: 5 25 5 65
