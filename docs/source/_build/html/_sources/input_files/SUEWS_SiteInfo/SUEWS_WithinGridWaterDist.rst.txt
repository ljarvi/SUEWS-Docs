SUEWS_WithinGridWaterDist.txt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

SUEWS_WithinGridWaterDist.txt specifies the movement of water between
surfaces within a grid/area. It allows impervious connectivity to be
taken into account.

Each row corresponds to a surface type (linked by the Code in column 1
to the `SiteSelect.txt <#SiteSelect.txt>`__ columns:
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

+----+----+----+----+----+----+----+----+----+----+----+
| 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9  | 10 |    |
+====+====+====+====+====+====+====+====+====+====+====+
| Co | To | To | To | To | To | To | To | To | To |    |
| de | Pa | Bu | Ev | De | Gr | BS | Wa | Ru | So |    |
|    | ve | il | eT | cT | as | oi | te | no | il |    |
|    | d  | t  | r  | r  | s  | l  | r  | ff | St |    |
|    |    |    |    |    |    |    |    |    | or |    |
|    |    |    |    |    |    |    |    |    | e  |    |
+----+----+----+----+----+----+----+----+----+----+----+
| 10 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | Pa |
|    |    |    |    |    |    |    |    |    |    | ve |
|    |    |    |    |    |    |    |    |    |    | d  |
+----+----+----+----+----+----+----+----+----+----+----+
| 20 | 0. | 0  | 0. | 0. | 0. | 0. | 0  | 0. | 0  | Bl |
|    | 06 |    | 01 | 01 | 01 | 01 |    | 9  |    | dg |
|    |    |    |    |    |    |    |    |    |    | s  |
+----+----+----+----+----+----+----+----+----+----+----+
| 30 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | Ev |
|    |    |    |    |    |    |    |    |    |    | eT |
|    |    |    |    |    |    |    |    |    |    | r  |
+----+----+----+----+----+----+----+----+----+----+----+
| 40 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | De |
|    |    |    |    |    |    |    |    |    |    | cT |
|    |    |    |    |    |    |    |    |    |    | r  |
+----+----+----+----+----+----+----+----+----+----+----+
| 50 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | Gr |
|    |    |    |    |    |    |    |    |    |    | as |
|    |    |    |    |    |    |    |    |    |    | s  |
+----+----+----+----+----+----+----+----+----+----+----+
| 60 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | BS |
|    |    |    |    |    |    |    |    |    |    | oi |
|    |    |    |    |    |    |    |    |    |    | l  |
+----+----+----+----+----+----+----+----+----+----+----+
| 70 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Wa |
|    |    |    |    |    |    |    |    |    |    | te |
|    |    |    |    |    |    |    |    |    |    | r  |
+----+----+----+----+----+----+----+----+----+----+----+