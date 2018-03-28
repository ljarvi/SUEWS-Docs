.. _SUEWS_WithinGridWaterDist.txt:

SUEWS_WithinGridWaterDist.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

SUEWS_WithinGridWaterDist.txt specifies the movement of water between
surfaces within a grid/area. It allows impervious connectivity to be
taken into account.

Each row corresponds to a surface type (linked by the Code in column 1
to the `SUEWS_SiteSelect.txt` columns:
WithinGridPavedCode, WithinGridBldgsCode, …, WithinGridWaterCode). Each
column contains the fraction of water flowing from the surface type to
each of the other surface types or to runoff or the sub-surface soil
store.

Note:

-  The sum of each row (excluding the Code) must equal 1.
-  Water cannot flow from one surface to that same surface, so the
   diagonal elements should be zero.
-  The row corresponding to the water surface should be zero, as there
   is currently no flow permitted from the water surface to other
   surfaces by the model.
-  Currently water **cannot** go to both runoff and soil store (i.e. it
   must go to one or the other – runoff for impervious surfaces;
   soilstore for pervious surfaces).

In the table below, for example,

-  all flow from paved surfaces goes to runoff;
-  90% of flow from buildings goes to runoff, with small amounts going
   to other surfaces (mostly paved surfaces as buildings are often
   surrounded by paved areas);
-  all flow from vegetated and bare soil areas goes into the sub-surface
   soil store;
-  the row corresponding to water contains zeros (as it is currently not
   used).


.. csv-table::
  :file: SUEWS_WithinGridWaterDist.csv
  :header-rows: 1
