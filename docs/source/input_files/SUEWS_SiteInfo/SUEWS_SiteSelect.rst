.. _SUEWS_SiteSelect.txt:

SUEWS_SiteSelect.txt
~~~~~~~~~~~~~~~~~~~~

For each year and each grid, site specific surface cover information and
other input parameters is provided to SUEWS by `SUEWS_SiteSelect.txt`.
The model currently requires a new row for each year of the model run.
All rows in this file will be read by the model and run.

.. csv-table::
  :file: SUEWS_SiteSelect.csv
  :header-rows: 1
  :widths: 5 25 5 65

.. attention::
  - Two rows of `-9` should be placed at end of this file.
  - In this file the **column order is important**.
  - In this file the **row order is important** for simulaitons of **multiple grids and multiple years**.
    Rows of grids of one year should be placed prior to other years, see below for an example::
      Grid  Year ...
      1     2001 ...
      2     2001 ...
      1     2002 ...
      2     2002 ...

.. tip::
  `\!` can be used to indicate comments in the file. Comments are not read by the
  programme so they can be used by the user to provide notes for their
  interpretation of the contents. This is strongly recommended.

Day Light Savings (DLS)
^^^^^^^^^^^^^^^^^^^^^^^

The dates for DLS normally vary each year and country as they are often
associated with a specific set of Sunday mornings at the beginning of
summer and autumn. Note it is important to remember leap years. You can
check http://www.timeanddate.com/time/dst/ for your city.


.. tip::
    If DLS does not occur give a start and end day immediately after it.
    Make certain the dummy dates are correct for the hemisphere
     - for northern hemisphere, use: 180 181
     - for southern hemisphere, use:  365 1

Example when running  multiple years (in this case 2008 and 2009 in Canada):
    .. list-table::
      :widths: auto
      :header-rows: 1

      * - Year
        - start of daylight savings
        - end of daylight savings
      * - 2008
        - 170
        - 240
      * - 2009
        - 172
        - 242



Grid Connections (water flow between grids)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. caution::
    - not currently implemented
    - columns 64-79 of `SUEWS_SiteSelect.txt` can be set to zero.

This section gives an example of water flow between grids, calculated
based on the relative elevation of the grids and length of the
connecting surface between adjacent grids. For the square grids in the
figure, water flow is assumed to be zero between diagonally adjacent
grids, as the length of connecting surface linking the grids is very
small. Model grids need not be square or the same size.

The table gives example values for the grid connections part of
`SUEWS_SiteSelect.txt` for the grids shown in
the figure. For each row, only water flowing out of the current grid is
entered (e.g. water flows from 234 to 236 and 237, with a larger
proportion of water flowing to 237 because of the greater length of
connecting surface between 234 and 237 than between 234 and 236. No
water is assumed to flow between 234 and 233 or 235 because there is no
elevation difference between these grids. Grids 234 and 238 are at the
same elevation and only connect at a point, so no water flows between
them. Water enters grid 234 from grids 230, 231 and 232 as these are
more elevated.


.. figure:: GridConnections_1.jpg
    :alt: Example grid connections showing water flow between grids. Arrows indicate the water flow in to and out of grid 234, but note that only only water flowing out of each grid is entered in `SUEWS_SiteSelect.txt`

    Example grid connections showing water flow between grids. 

.. note::
  Arrows indicate the water flow in to and out of grid 234, 
  but note that only only water flowing out of each grid is entered in `SUEWS_SiteSelect.txt`



.. figure:: GridConnections_2_v2.jpg
   :alt:  Example values for the grid connections part of `SUEWS_SiteSelect.txt` for the grids.

   Example values for the grid connections part of `SUEWS_SiteSelect.txt` for the grids.
