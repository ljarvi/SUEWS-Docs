.. _SUEWS_Soil.txt:

SUEWS_Soil.txt
~~~~~~~~~~~~~~

SUEWS_Soil.txt specifies the characteristics of the sub-surface soil
below each of the non-water surface types (Paved, Bldgs, EveTr, DecTr,
Grass, BSoil). The model does not have a soi store below the water
surfaces. Note that these sub-surface soil stores are different to the
bare soil/unmamnaged surface cover type. Each of the non-water surface
types need to link to soil characteristics specified here. If the soil
characteristics are assumed to be the same for all surface types, use a
single code value to link the characteristics here with the SoilTypeCode
columns in `SUEWS_NonVeg.txt` and `SUEWS_Veg.txt`.

Soil moisture can either be provided using observational data in the met
forcing file (smd_choice = 1 or 2 in
`RunControl.nml`) and providing some metadata
information here (OBS columns), or modelled by SUEWS (smd_choice = 0
in `RunControl.nml`). **- Note, the option to use
observational data is not operational in the current release!**


.. csv-table::
  :file: SUEWS_Soil.csv
  :header-rows: 1
  :widths: auto
