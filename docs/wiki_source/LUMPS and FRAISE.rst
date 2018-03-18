LUMPS and FRAISE
===========================================


The largest difference between LUMPS and SUEWS is that the latter
simulates the urban water balance in detail while LUMPS takes a simpler
approach for the sensible and latent heat fluxes and the water balance
(“water bucket”). The calculation of evaporation/latent heat in SUEWS is
more biophysically based. Due to its simplicity, LUMPS requires less
parameters in order to run. SUEWS gives turbulent heat fluxes calculated
with both models as an output. **The model can run LUMPS alone without
running SUEWS (Table 4.1 – SuewsStatus).**

Similarities and differences between LUMPS and SUEWS.

+-----------------------+-----------------------+-----------------------+
|                       | LUMPS                 | SUEWS                 |
+=======================+=======================+=======================+
| Net all-wave          | Input or NARP         | Input or NARP         |
| radiation (Q*)        |                       |                       |
+-----------------------+-----------------------+-----------------------+
| Storage heat flux     | Input or from OHM     | Input or from OHM     |
| (ΔQS)                 |                       |                       |
+-----------------------+-----------------------+-----------------------+
| Anthropogenic heat    | Input or calculated   | Input or calculated   |
| flux (QF)             |                       |                       |
+-----------------------+-----------------------+-----------------------+
| Latent heat (QE)      | DeBruin and Holtslag  | Penman-Monteith       |
|                       | (1982)                | equation2             |
+-----------------------+-----------------------+-----------------------+
| Sensible heat flux    | DeBruin and Holtslag  | Residual from         |
| (QH)                  | (1982)                | available energy      |
|                       |                       | minus QE              |
+-----------------------+-----------------------+-----------------------+
| Water balance         | No water balance      | Running water balance |
|                       | included              | of canopy and water   |
|                       |                       | balance of soil       |
+-----------------------+-----------------------+-----------------------+
| Soil moisture         | Not considered        | Modelled              |
+-----------------------+-----------------------+-----------------------+
| Surface wetness       | Simple water bucket   | Running water balance |
|                       | model                 |                       |
+-----------------------+-----------------------+-----------------------+
| Irrigation            | Only fraction of      | Input or calculated   |
|                       | surface area that is  | with a simple model   |
|                       | irrigated             |                       |
+-----------------------+-----------------------+-----------------------+
| Surface cover         | buildings, paved,     | buildings, paved,     |
|                       | vegetation            | coniferous and        |
|                       |                       | deciduous             |
|                       |                       | trees/shrubs,         |
|                       |                       | irrigated and         |
|                       |                       | unirrigated grass     |
+-----------------------+-----------------------+-----------------------+
|  |
+-----------------------+-----------------------+-----------------------+

FRAISE Flux Ratio – Active Index Surface Exchange
-------------------------------------------------

FRAISE provides an estimate of mean midday (±3 h around solar noon)
energy partitioning from information on the surface characteristics and
estimates of the mean midday incoming radiative energy and anthropogenic
heat release. Please refer to Loridan and Grimmond (2012) [LG2012]_ for
further details.

+-----------------+-----------------+-----------------+-----------------+
| Topic           | FRAISE          | LUMPS           | SUEWS           |
+=================+=================+=================+=================+
| **Complexity**  | Simplest:       |                 | More complex:   |
|                 | FRAISE          |                 | SUEWS           |
+-----------------+-----------------+-----------------+-----------------+
| **Software      | R code          | Windows exe     | Windows exe     |
| provided:**     |                 | (written in     | (written in     |
|                 |                 | Fortran)        | Fortran) -      |
|                 |                 |                 | other versions  |
|                 |                 |                 | available       |
+-----------------+-----------------+-----------------+-----------------+
| Applicable      | Midday (within  | hourly          | 5               |
| period:         | 3 h of solar    |                 | min-hourly-annu |
|                 | noon)           |                 | al              |
+-----------------+-----------------+-----------------+-----------------+
| Unique          | calculates      | radiation and   | radiation,      |
| features:       | active surface  | energy balances | energy and      |
|                 | – and fluxes    |                 | water balance   |
|                 |                 |                 | (includes       |
|                 |                 |                 | LUMPS)          |
+-----------------+-----------------+-----------------+-----------------+
|  |
+-----------------+-----------------+-----------------+-----------------+