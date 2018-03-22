Initial Conditions file
-----------------------

To start the model, information about the conditions at the start of the
run is required. This information is provided in initial conditions
file. One file can be specified for each grid (MultipleInitFiles=1 in
`RunControl.nml <#RunControl.nml>`__, filename includes grid number) or,
alternatively, a single file can be specified for all grids
(MultipleInitFiles=0 in `RunControl.nml <#RunControl.nml>`__, no grid
number in the filename). After that, a new
InitialConditionsSSss_YYYY.nml file will be written for each grid for
the following years. It is recommended that you look at these files
(written to the input directory) to check the status of various surfaces
at the end or the run. This may help you get more realistic starting
values if you are uncertain what they should be. Note this file will be
created for each year for multiyear runs for each grid. If the run
finishes before the end of the year the InitialConditions file is still
written and the file name is appended with '_EndofRun'.

The two most important pieces of information in the initial conditions
file is the soil moisture and state of vegetation at the start of the
run. This is the minimal information required; other information can be
provided if known, otherwise SUEWS will make an estimate of initial
conditions.

InitialConditionsSSss_YYYY.nml
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Variables can be in any order

+-----------+-----------+-----------+-----------+-----------+-----------+
| Parameter | Required/ | Unit      | Comments  |           |           |
| s         | Optional  |           |           |           |           |
+===========+===========+===========+===========+===========+===========+
| **Soil    |           |           |           |           |           |
| moisture  |           |           |           |           |           |
| states**  |           |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Soilstore | R         | mm        | Initial   | SUEWS_Soi |           |
| PavedStat |           |           | state of  | l.txt]]   |           |
| e         |           |           | the soil  |           |           |
|           |           |           | water     |           |           |
|           |           |           | storage   |           |           |
|           |           |           | under     |           |           |
|           |           |           | paved     |           |           |
|           |           |           | surfaces. |           |           |
|           |           |           | \*For     |           |           |
|           |           |           | maximum   |           |           |
|           |           |           | values,   |           |           |
|           |           |           | see the   |           |           |
|           |           |           | used soil |           |           |
|           |           |           | code in   |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Soil.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Soilstore | R         | mm        | Initial   | SUEWS_Soi |           |
| BldgsStat |           |           | state of  | l.txt]]   |           |
| e         |           |           | the soil  |           |           |
|           |           |           | water     |           |           |
|           |           |           | storage   |           |           |
|           |           |           | under     |           |           |
|           |           |           | buildings |           |           |
|           |           |           | \*For     |           |           |
|           |           |           | maximum   |           |           |
|           |           |           | values,   |           |           |
|           |           |           | see the   |           |           |
|           |           |           | used soil |           |           |
|           |           |           | code in   |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Soil.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Soilstore | R         | mm        | Initial   | SUEWS_Soi |           |
| EveTrStat |           |           | state of  | l.txt]]   |           |
| e         |           |           | the soil  |           |           |
|           |           |           | water     |           |           |
|           |           |           | storage   |           |           |
|           |           |           | under     |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | trees     |           |           |
|           |           |           | \*For     |           |           |
|           |           |           | maximum   |           |           |
|           |           |           | values,   |           |           |
|           |           |           | see the   |           |           |
|           |           |           | used soil |           |           |
|           |           |           | code in   |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Soil.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Soilstore | R         | mm        | Initial   | SUEWS_Soi |           |
| DecTrStat |           |           | state of  | l.txt]]   |           |
| e         |           |           | the soil  |           |           |
|           |           |           | water     |           |           |
|           |           |           | storage   |           |           |
|           |           |           | under     |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | trees     |           |           |
|           |           |           | \*For     |           |           |
|           |           |           | maximum   |           |           |
|           |           |           | values,   |           |           |
|           |           |           | see the   |           |           |
|           |           |           | used soil |           |           |
|           |           |           | code in   |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Soil.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Soilstore | R         | mm        | Initial   | SUEWS_Soi |           |
| GrassStat |           |           | state of  | l.txt]]   |           |
| e         |           |           | the soil  |           |           |
|           |           |           | water     |           |           |
|           |           |           | storage   |           |           |
|           |           |           | under     |           |           |
|           |           |           | grass     |           |           |
|           |           |           | \*For     |           |           |
|           |           |           | maximum   |           |           |
|           |           |           | values,   |           |           |
|           |           |           | see the   |           |           |
|           |           |           | used soil |           |           |
|           |           |           | code in   |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Soil.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Soilstore | R         | mm        | Initial   | SUEWS_Soi |           |
| BSoilStat |           |           | state of  | l.txt]]   |           |
| e         |           |           | the soil  |           |           |
|           |           |           | water     |           |           |
|           |           |           | storage   |           |           |
|           |           |           | under     |           |           |
|           |           |           | bare soil |           |           |
|           |           |           | surfaces  |           |           |
|           |           |           | \*For     |           |           |
|           |           |           | maximum   |           |           |
|           |           |           | values,   |           |           |
|           |           |           | see the   |           |           |
|           |           |           | used soil |           |           |
|           |           |           | code in   |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Soil.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
|           |           |           | (Note: no |           |           |
|           |           |           | soil      |           |           |
|           |           |           | store     |           |           |
|           |           |           | below     |           |           |
|           |           |           | water     |           |           |
|           |           |           | surface)  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| **Vegetat |           |           | Can be    |           |           |
| ion       |           |           | set       |           |           |
| parameter |           |           | individua |           |           |
| s**       |           |           | lly       |           |           |
|           |           |           | or using  |           |           |
|           |           |           | a single  |           |           |
|           |           |           | vegetatio |           |           |
|           |           |           | n         |           |           |
|           |           |           | parameter |           |           |
|           |           |           | (LeavesOu |           |           |
|           |           |           | tInitiall |           |           |
|           |           |           | y)        |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| LeavesOut | (O)       | -         | Sets all  | SUEWS_Veg |           |
| Intially  |           |           | required  | .txt]]    |           |
|           |           |           | vegetatio | and the   |           |
|           |           |           | n         | time of   |           |
|           |           |           | parameter | year.     |           |
|           |           |           | s         | -  If     |           |
|           |           |           | according | values    |           |
|           |           |           | ly        | are       |           |
|           |           |           | using     | provid    |           |
|           |           |           | informati | ed        |           |
|           |           |           | on        | indivi    |           |
|           |           |           | for full  | dually,   |           |
|           |           |           | leaf-out  | values    |           |
|           |           |           | (1)/compl | for       |           |
|           |           |           | ete       | all       |           |
|           |           |           | leaf-off  | requir    |           |
|           |           |           | (0)       | ed        |           |
|           |           |           | -  If the | surfac    |           |
|           |           |           | model     | es        |           |
|           |           |           | run       | must      |           |
|           |           |           | starts    | be        |           |
|           |           |           | in        | provid    |           |
|           |           |           | winter    | ed        |           |
|           |           |           | when      | (i.e.     |           |
|           |           |           | trees     | specif    |           |
|           |           |           | are       | ying      |           |
|           |           |           | bare,     | only      |           |
|           |           |           | set       | albGra    |           |
|           |           |           | Leaves    | ss0       |           |
|           |           |           | OutIntial | but       |           |
|           |           |           | ly        | not       |           |
|           |           |           | = 0       | albDec    |           |
|           |           |           | and       | Tr0       |           |
|           |           |           | the       | nor       |           |
|           |           |           | vegeta    | albEve    |           |
|           |           |           | tion      | Tr0       |           |
|           |           |           | parame    | is not    |           |
|           |           |           | ters      | permit    |           |
|           |           |           | will      | ted).     |           |
|           |           |           | be set    |           |           |
|           |           |           | accord    |           |           |
|           |           |           | ingly     |           |           |
|           |           |           | based     |           |           |
|           |           |           | on the    |           |           |
|           |           |           | values    |           |           |
|           |           |           | set in    |           |           |
|           |           |           | SUEWS_    |           |           |
|           |           |           | SiteInfo. |           |           |
|           |           |           | xlsm.     |           |           |
|           |           |           | -  If the |           |           |
|           |           |           | model     |           |           |
|           |           |           | run       |           |           |
|           |           |           | starts    |           |           |
|           |           |           | in        |           |           |
|           |           |           | summer    |           |           |
|           |           |           | when      |           |           |
|           |           |           | leaves    |           |           |
|           |           |           | are       |           |           |
|           |           |           | fully     |           |           |
|           |           |           | out,      |           |           |
|           |           |           | set       |           |           |
|           |           |           | Leaves    |           |           |
|           |           |           | OutIntial |           |           |
|           |           |           | ly        |           |           |
|           |           |           | = 1       |           |           |
|           |           |           | and       |           |           |
|           |           |           | the       |           |           |
|           |           |           | vegeta    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | parame    |           |           |
|           |           |           | ters      |           |           |
|           |           |           | will      |           |           |
|           |           |           | be set    |           |           |
|           |           |           | accord    |           |           |
|           |           |           | ingly     |           |           |
|           |           |           | based     |           |           |
|           |           |           | on the    |           |           |
|           |           |           | values    |           |           |
|           |           |           | set in    |           |           |
|           |           |           | SUEWS_    |           |           |
|           |           |           | SiteInfo. |           |           |
|           |           |           | xlsm.     |           |           |
|           |           |           | -  Not    |           |           |
|           |           |           | Leaves    |           |           |
|           |           |           | OutInitia |           |           |
|           |           |           | lly       |           |           |
|           |           |           | can       |           |           |
|           |           |           | only      |           |           |
|           |           |           | be set    |           |           |
|           |           |           | to 0,     |           |           |
|           |           |           | 1 or      |           |           |
|           |           |           | -999      |           |           |
|           |           |           | (fract    |           |           |
|           |           |           | ional     |           |           |
|           |           |           | values    |           |           |
|           |           |           | cannot    |           |           |
|           |           |           | be        |           |           |
|           |           |           | used      |           |           |
|           |           |           | to        |           |           |
|           |           |           | indica    |           |           |
|           |           |           | te        |           |           |
|           |           |           | partia    |           |           |
|           |           |           | l         |           |           |
|           |           |           | leaf-o    |           |           |
|           |           |           | ut).      |           |           |
|           |           |           | -  The    |           |           |
|           |           |           | value     |           |           |
|           |           |           | of        |           |           |
|           |           |           | Leaves    |           |           |
|           |           |           | OutInitia |           |           |
|           |           |           | lly       |           |           |
|           |           |           | overri    |           |           |
|           |           |           | des       |           |           |
|           |           |           | any       |           |           |
|           |           |           | values    |           |           |
|           |           |           | provid    |           |           |
|           |           |           | ed        |           |           |
|           |           |           | for       |           |           |
|           |           |           | the       |           |           |
|           |           |           | indivi    |           |           |
|           |           |           | dual      |           |           |
|           |           |           | vegeta    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | parame    |           |           |
|           |           |           | ters.     |           |           |
|           |           |           | -  To     |           |           |
|           |           |           | preven    |           |           |
|           |           |           | t         |           |           |
|           |           |           | Leaves    |           |           |
|           |           |           | OutInitia |           |           |
|           |           |           | lly       |           |           |
|           |           |           | from      |           |           |
|           |           |           | settin    |           |           |
|           |           |           | g         |           |           |
|           |           |           | the       |           |           |
|           |           |           | initia    |           |           |
|           |           |           | l         |           |           |
|           |           |           | condit    |           |           |
|           |           |           | ions,     |           |           |
|           |           |           | either    |           |           |
|           |           |           | omit      |           |           |
|           |           |           | it        |           |           |
|           |           |           | from      |           |           |
|           |           |           | the       |           |           |
|           |           |           | nameli    |           |           |
|           |           |           | st        |           |           |
|           |           |           | or set    |           |           |
|           |           |           | to        |           |           |
|           |           |           | -999.     |           |           |
|           |           |           | \*If      |           |           |
|           |           |           | values    |           |           |
|           |           |           | are       |           |           |
|           |           |           | provided  |           |           |
|           |           |           | individua |           |           |
|           |           |           | lly,      |           |           |
|           |           |           | they      |           |           |
|           |           |           | should be |           |           |
|           |           |           | consisten |           |           |
|           |           |           | t         |           |           |
|           |           |           | the       |           |           |
|           |           |           | informati |           |           |
|           |           |           | on        |           |           |
|           |           |           | provided  |           |           |
|           |           |           | in        |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Veg.txt   |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| GDD_1_0   | O         | °C        | Growing   |           |           |
|           |           |           | degree    |           |           |
|           |           |           | days for  |           |           |
|           |           |           | leaf      |           |           |
|           |           |           | growth.   |           |           |
|           |           |           | -  Cannot |           |           |
|           |           |           | be        |           |           |
|           |           |           | negati    |           |           |
|           |           |           | ve.       |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | leaves    |           |           |
|           |           |           | are       |           |           |
|           |           |           | alread    |           |           |
|           |           |           | y         |           |           |
|           |           |           | full,     |           |           |
|           |           |           | then      |           |           |
|           |           |           | this      |           |           |
|           |           |           | should    |           |           |
|           |           |           | be the    |           |           |
|           |           |           | same      |           |           |
|           |           |           | as        |           |           |
|           |           |           | GDDFul    |           |           |
|           |           |           | l         |           |           |
|           |           |           | in        |           |           |
|           |           |           | SUEWS_    |           |           |
|           |           |           | Veg.txt.  |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | *winte    |           |           |
|           |           |           | r*,       |           |           |
|           |           |           | set to    |           |           |
|           |           |           | 0.        |           |           |
|           |           |           | -  It is  |           |           |
|           |           |           | import    |           |           |
|           |           |           | ant       |           |           |
|           |           |           | that      |           |           |
|           |           |           | the       |           |           |
|           |           |           | vegeta    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | charac    |           |           |
|           |           |           | teristics |           |           |
|           |           |           | are       |           |           |
|           |           |           | set       |           |           |
|           |           |           | correc    |           |           |
|           |           |           | tly       |           |           |
|           |           |           | (i.e.     |           |           |
|           |           |           | for       |           |           |
|           |           |           | the       |           |           |
|           |           |           | start     |           |           |
|           |           |           | of the    |           |           |
|           |           |           | run in    |           |           |
|           |           |           | summer    |           |           |
|           |           |           | /winter). |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| GDD_2_0   | O         | °C        | Growing   |           |           |
|           |           |           | degree    |           |           |
|           |           |           | days for  |           |           |
|           |           |           | senescenc |           |           |
|           |           |           | e         |           |           |
|           |           |           | growth.   |           |           |
|           |           |           | -  Cannot |           |           |
|           |           |           | be        |           |           |
|           |           |           | positi    |           |           |
|           |           |           | ve        |           |           |
|           |           |           | -  If the |           |           |
|           |           |           | leaves    |           |           |
|           |           |           | are       |           |           |
|           |           |           | full      |           |           |
|           |           |           | but in    |           |           |
|           |           |           | early/    |           |           |
|           |           |           | mid       |           |           |
|           |           |           | summer    |           |           |
|           |           |           | then      |           |           |
|           |           |           | set to    |           |           |
|           |           |           | 0.        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | *late     |           |           |
|           |           |           | summer    |           |           |
|           |           |           | or        |           |           |
|           |           |           | autumn    |           |           |
|           |           |           | *,        |           |           |
|           |           |           | this      |           |           |
|           |           |           | should    |           |           |
|           |           |           | be a      |           |           |
|           |           |           | negati    |           |           |
|           |           |           | ve        |           |           |
|           |           |           | value.    |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | *leave    |           |           |
|           |           |           | s         |           |           |
|           |           |           | are       |           |           |
|           |           |           | off*,     |           |           |
|           |           |           | then      |           |           |
|           |           |           | use       |           |           |
|           |           |           | the       |           |           |
|           |           |           | values    |           |           |
|           |           |           | of        |           |           |
|           |           |           | SDDFul    |           |           |
|           |           |           | l         |           |           |
|           |           |           | in        |           |           |
|           |           |           | SUEWS_    |           |           |
|           |           |           | Veg.txt   |           |           |
|           |           |           | to        |           |           |
|           |           |           | guide     |           |           |
|           |           |           | your      |           |           |
|           |           |           | minimu    |           |           |
|           |           |           | m         |           |           |
|           |           |           | value.    |           |           |
|           |           |           | -  It is  |           |           |
|           |           |           | import    |           |           |
|           |           |           | ant       |           |           |
|           |           |           | that      |           |           |
|           |           |           | the       |           |           |
|           |           |           | vegeta    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | charac    |           |           |
|           |           |           | teristics |           |           |
|           |           |           | are       |           |           |
|           |           |           | set       |           |           |
|           |           |           | correc    |           |           |
|           |           |           | tly       |           |           |
|           |           |           | (i.e.     |           |           |
|           |           |           | for       |           |           |
|           |           |           | the       |           |           |
|           |           |           | start     |           |           |
|           |           |           | of the    |           |           |
|           |           |           | run in    |           |           |
|           |           |           | summer    |           |           |
|           |           |           | /winter). |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| LAIinitia | O         | m\ :sup:` | Initial   | SUEWS_Veg |           |
| lEveTr    |           | -2`       | LAI for   | .txt]]    |           |
|           |           | m\ :sup:` | evergreen |           |           |
|           |           | -2`       | trees.    |           |           |
|           |           |           | The       |           |           |
|           |           |           | recommend |           |           |
|           |           |           | ed        |           |           |
|           |           |           | values    |           |           |
|           |           |           | can be    |           |           |
|           |           |           | found     |           |           |
|           |           |           | from      |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Veg.txt   |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| LAIinitia | O         | m\ :sup:` | Initial   | SUEWS_Veg |           |
| lDecTr    |           | -2`       | LAI for   | .txt]]    |           |
|           |           | m\ :sup:` | deciduous |           |           |
|           |           | -2`       | trees.    |           |           |
|           |           |           | The       |           |           |
|           |           |           | recommend |           |           |
|           |           |           | ed        |           |           |
|           |           |           | values    |           |           |
|           |           |           | can be    |           |           |
|           |           |           | found     |           |           |
|           |           |           | from      |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Veg.txt   |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| LAIinitia | O         | m\ :sup:` | Initial   | SUEWS_Veg |           |
| lGrass    |           | -2`       | LAI for   | .txt]]    |           |
|           |           | m\ :sup:` | irrigated |           |           |
|           |           | -2`       | grass.    |           |           |
|           |           |           | The       |           |           |
|           |           |           | recommend |           |           |
|           |           |           | ed        |           |           |
|           |           |           | values    |           |           |
|           |           |           | can be    |           |           |
|           |           |           | found     |           |           |
|           |           |           | from      |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Veg.txt   |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| albEveTr0 | O         | -         | Albedo of |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | surface   |           |           |
|           |           |           | on day 0  |           |           |
|           |           |           | of run    |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| albDecTr0 | O         | -         | Albedo of |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | surface   |           |           |
|           |           |           | on day 0  |           |           |
|           |           |           | of run    |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| albGrass0 | O         | -         | Albedo of |           |           |
|           |           |           | grass     |           |           |
|           |           |           | surface   |           |           |
|           |           |           | on day 0  |           |           |
|           |           |           | of run    |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| decidCap0 | O         | mm        | Deciduous |           |           |
|           |           |           | storage   |           |           |
|           |           |           | capacity  |           |           |
|           |           |           | on day 0  |           |           |
|           |           |           | of run.   |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| porosity0 | O         | -         | Porosity  |           |           |
|           |           |           | of        |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | vegetatio |           |           |
|           |           |           | n         |           |           |
|           |           |           | on day 0  |           |           |
|           |           |           | of run.   |           |           |
|           |           |           | This      |           |           |
|           |           |           | varies    |           |           |
|           |           |           | between   |           |           |
|           |           |           | 0.2       |           |           |
|           |           |           | (leaf-on) |           |           |
|           |           |           | and 0.6   |           |           |
|           |           |           | (leaf-off |           |           |
|           |           |           | ).        |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| **Recent  |           |           |           |           |           |
| meteorolo |           |           |           |           |           |
| gy**      |           |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| DaysSince | O         | days      | Number of |           |           |
| Rain      |           |           | days      |           |           |
|           |           |           | since     |           |           |
|           |           |           | rainfall  |           |           |
|           |           |           | occurred. |           |           |
|           |           |           | -  **Impo |           |           |
|           |           |           | rtant**   |           |           |
|           |           |           | to use    |           |           |
|           |           |           | correc    |           |           |
|           |           |           | t         |           |           |
|           |           |           | value     |           |           |
|           |           |           | if        |           |           |
|           |           |           | starti    |           |           |
|           |           |           | ng        |           |           |
|           |           |           | in        |           |           |
|           |           |           | summer    |           |           |
|           |           |           | season    |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | starti    |           |           |
|           |           |           | ng        |           |           |
|           |           |           | when      |           |           |
|           |           |           | extern    |           |           |
|           |           |           | al        |           |           |
|           |           |           | water     |           |           |
|           |           |           | use is    |           |           |
|           |           |           | not       |           |           |
|           |           |           | occurr    |           |           |
|           |           |           | ing       |           |           |
|           |           |           | it        |           |           |
|           |           |           | will      |           |           |
|           |           |           | be        |           |           |
|           |           |           | reset     |           |           |
|           |           |           | with      |           |           |
|           |           |           | the       |           |           |
|           |           |           | first     |           |           |
|           |           |           | rain      |           |           |
|           |           |           | so can    |           |           |
|           |           |           | just      |           |           |
|           |           |           | be set    |           |           |
|           |           |           | to 0.     |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | SUEWS     |           |           |
|           |           |           | sets      |           |           |
|           |           |           | to        |           |           |
|           |           |           | zero      |           |           |
|           |           |           | by        |           |           |
|           |           |           | defaul    |           |           |
|           |           |           | t.        |           |           |
|           |           |           | -  Used   |           |           |
|           |           |           | to        |           |           |
|           |           |           | model     |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion.     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| Temp_C0   | O         | °C        | Daily     |           |           |
|           |           |           | mean      |           |           |
|           |           |           | temperatu |           |           |
|           |           |           | re        |           |           |
|           |           |           | [°C] for  |           |           |
|           |           |           | the day   |           |           |
|           |           |           | before    |           |           |
|           |           |           | the run   |           |           |
|           |           |           | starts    |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | SUEWS     |           |           |
|           |           |           | uses      |           |           |
|           |           |           | the       |           |           |
|           |           |           | mean      |           |           |
|           |           |           | temper    |           |           |
|           |           |           | ature     |           |           |
|           |           |           | for       |           |           |
|           |           |           | the       |           |           |
|           |           |           | first     |           |           |
|           |           |           | day of    |           |           |
|           |           |           | the       |           |           |
|           |           |           | run.      |           |           |
|           |           |           | -  Used   |           |           |
|           |           |           | to        |           |           |
|           |           |           | model     |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | and       |           |           |
|           |           |           | anthro    |           |           |
|           |           |           | pogenic   |           |           |
|           |           |           | heat      |           |           |
|           |           |           | flux.     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| **Above   |           |           |           |           |           |
| Ground    |           |           |           |           |           |
| State**   |           |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| PavedStat | O         |           | Initial   |           |           |
| e         |           |           | wetness   |           |           |
|           |           |           | state of  |           |           |
|           |           |           | paved     |           |           |
|           |           |           | surface   |           |           |
|           |           |           | (0        |           |           |
|           |           |           | indicates |           |           |
|           |           |           | dry, wet  |           |           |
|           |           |           | otherwise |           |           |
|           |           |           | ).        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | model     |           |           |
|           |           |           | assume    |           |           |
|           |           |           | s         |           |           |
|           |           |           | dry       |           |           |
|           |           |           | surfac    |           |           |
|           |           |           | es        |           |           |
|           |           |           | (accep    |           |           |
|           |           |           | table     |           |           |
|           |           |           | as        |           |           |
|           |           |           | rainfa    |           |           |
|           |           |           | ll        |           |           |
|           |           |           | or        |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | will      |           |           |
|           |           |           | update    |           |           |
|           |           |           | these     |           |           |
|           |           |           | states    |           |           |
|           |           |           | quickl    |           |           |
|           |           |           | y).       |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| BldgsStat | O         | mm        | Initial   |           |           |
| e         |           |           | wetness   |           |           |
|           |           |           | state for |           |           |
|           |           |           | buildings |           |           |
|           |           |           | (0        |           |           |
|           |           |           | indicates |           |           |
|           |           |           | dry, wet  |           |           |
|           |           |           | otherwise |           |           |
|           |           |           | ).        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | model     |           |           |
|           |           |           | assume    |           |           |
|           |           |           | s         |           |           |
|           |           |           | dry       |           |           |
|           |           |           | surfac    |           |           |
|           |           |           | es        |           |           |
|           |           |           | (accep    |           |           |
|           |           |           | table     |           |           |
|           |           |           | as        |           |           |
|           |           |           | rainfa    |           |           |
|           |           |           | ll        |           |           |
|           |           |           | or        |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | will      |           |           |
|           |           |           | update    |           |           |
|           |           |           | these     |           |           |
|           |           |           | states    |           |           |
|           |           |           | quickl    |           |           |
|           |           |           | y).       |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| EveTrStat | O         | mm        | Initial   |           |           |
| e         |           |           | wetness   |           |           |
|           |           |           | state of  |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | trees (0  |           |           |
|           |           |           | indicates |           |           |
|           |           |           | dry, wet  |           |           |
|           |           |           | otherwise |           |           |
|           |           |           | ).        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | model     |           |           |
|           |           |           | assume    |           |           |
|           |           |           | s         |           |           |
|           |           |           | dry       |           |           |
|           |           |           | surfac    |           |           |
|           |           |           | es        |           |           |
|           |           |           | (accep    |           |           |
|           |           |           | table     |           |           |
|           |           |           | as        |           |           |
|           |           |           | rainfa    |           |           |
|           |           |           | ll        |           |           |
|           |           |           | or        |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | will      |           |           |
|           |           |           | update    |           |           |
|           |           |           | these     |           |           |
|           |           |           | states    |           |           |
|           |           |           | quickl    |           |           |
|           |           |           | y).       |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| DecTrStat | O         | mm        | Initial   |           |           |
| e         |           |           | wetness   |           |           |
|           |           |           | state of  |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | trees (0  |           |           |
|           |           |           | indicates |           |           |
|           |           |           | dry, wet  |           |           |
|           |           |           | otherwise |           |           |
|           |           |           | ).        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | model     |           |           |
|           |           |           | assume    |           |           |
|           |           |           | s         |           |           |
|           |           |           | dry       |           |           |
|           |           |           | surfac    |           |           |
|           |           |           | es        |           |           |
|           |           |           | (accep    |           |           |
|           |           |           | table     |           |           |
|           |           |           | as        |           |           |
|           |           |           | rainfa    |           |           |
|           |           |           | ll        |           |           |
|           |           |           | or        |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | will      |           |           |
|           |           |           | update    |           |           |
|           |           |           | these     |           |           |
|           |           |           | states    |           |           |
|           |           |           | quickl    |           |           |
|           |           |           | y).       |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| GrassStat | O         | mm        | Initial   |           |           |
| e         |           |           | wetness   |           |           |
|           |           |           | state of  |           |           |
|           |           |           | grass (0  |           |           |
|           |           |           | indicates |           |           |
|           |           |           | dry, wet  |           |           |
|           |           |           | otherwise |           |           |
|           |           |           | ).        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | model     |           |           |
|           |           |           | assume    |           |           |
|           |           |           | s         |           |           |
|           |           |           | dry       |           |           |
|           |           |           | surfac    |           |           |
|           |           |           | es        |           |           |
|           |           |           | (accep    |           |           |
|           |           |           | table     |           |           |
|           |           |           | as        |           |           |
|           |           |           | rainfa    |           |           |
|           |           |           | ll        |           |           |
|           |           |           | or        |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | will      |           |           |
|           |           |           | update    |           |           |
|           |           |           | these     |           |           |
|           |           |           | states    |           |           |
|           |           |           | quickl    |           |           |
|           |           |           | y).       |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| BSoilStat | O         | mm        | Initial   |           |           |
| e         |           |           | wetness   |           |           |
|           |           |           | state of  |           |           |
|           |           |           | bare soil |           |           |
|           |           |           | surface   |           |           |
|           |           |           | (0        |           |           |
|           |           |           | indicates |           |           |
|           |           |           | dry, wet  |           |           |
|           |           |           | otherwise |           |           |
|           |           |           | ).        |           |           |
|           |           |           | -  If     |           |           |
|           |           |           | unknow    |           |           |
|           |           |           | n,        |           |           |
|           |           |           | model     |           |           |
|           |           |           | assume    |           |           |
|           |           |           | s         |           |           |
|           |           |           | dry       |           |           |
|           |           |           | surfac    |           |           |
|           |           |           | es        |           |           |
|           |           |           | (accep    |           |           |
|           |           |           | table     |           |           |
|           |           |           | as        |           |           |
|           |           |           | rainfa    |           |           |
|           |           |           | ll        |           |           |
|           |           |           | or        |           |           |
|           |           |           | irriga    |           |           |
|           |           |           | tion      |           |           |
|           |           |           | will      |           |           |
|           |           |           | update    |           |           |
|           |           |           | these     |           |           |
|           |           |           | states    |           |           |
|           |           |           | quickl    |           |           |
|           |           |           | y).       |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| WaterStat | O         | mm        | Initial   | SUEWS_Wat | SUEWS_Wat |
| e         |           |           | state of  | er.txt]]. | er.txt]]. |
|           |           |           | water     | \*If      |           |
|           |           |           | surface   | unknown,  |           |
|           |           |           | (must be  | model     |           |
|           |           |           | set > 0,  | uses      |           |
|           |           |           | as 0      | value of  |           |
|           |           |           | indicates | **WaterDe |           |
|           |           |           | dry       | pth**     |           |
|           |           |           | surface). | specified |           |
|           |           |           | -  For a  | in        |           |
|           |           |           | large     | [[#SUEWS_ |           |
|           |           |           | water     | Water.txt |           |
|           |           |           | body      |           |           |
|           |           |           | (e.g.     |           |           |
|           |           |           | river,    |           |           |
|           |           |           | sea,      |           |           |
|           |           |           | lake)     |           |           |
|           |           |           | set       |           |           |
|           |           |           | WaterS    |           |           |
|           |           |           | tate      |           |           |
|           |           |           | to a      |           |           |
|           |           |           | large     |           |           |
|           |           |           | value,    |           |           |
|           |           |           | e.g.      |           |           |
|           |           |           | 20000     |           |           |
|           |           |           | mm;       |           |           |
|           |           |           | for       |           |           |
|           |           |           | small     |           |           |
|           |           |           | water     |           |           |
|           |           |           | bodies    |           |           |
|           |           |           | (e.g.     |           |           |
|           |           |           | ponds,    |           |           |
|           |           |           | founta    |           |           |
|           |           |           | ins)      |           |           |
|           |           |           | set       |           |           |
|           |           |           | WaterS    |           |           |
|           |           |           | tate      |           |           |
|           |           |           | to        |           |           |
|           |           |           | smalle    |           |           |
|           |           |           | r         |           |           |
|           |           |           | value,    |           |           |
|           |           |           | e.g.      |           |           |
|           |           |           | 1000      |           |           |
|           |           |           | mm.       |           |           |
|           |           |           | \*This    |           |           |
|           |           |           | value     |           |           |
|           |           |           | must not  |           |           |
|           |           |           | exceed    |           |           |
|           |           |           | **StateLi |           |           |
|           |           |           | mit**     |           |           |
|           |           |           | specified |           |           |
|           |           |           | in        |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Water.txt |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| **Snow-re |           |           | Can be    |           |           |
| lated     |           |           | set       |           |           |
| parameter |           |           | individua |           |           |
| s**       |           |           | lly       |           |           |
|           |           |           | or using  |           |           |
|           |           |           | a single  |           |           |
|           |           |           | snow      |           |           |
|           |           |           | parameter |           |           |
|           |           |           | (SnowInit |           |           |
|           |           |           | ially)    |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowIntia | (O)       | -         | Sets all  | SUEWS_Sno |           |
| lly       |           |           | required  | w.txt]].  |           |
|           |           |           | snow-rela |           |           |
|           |           |           | ted       |           |           |
|           |           |           | parameter |           |           |
|           |           |           | s         |           |           |
|           |           |           | according |           |           |
|           |           |           | ly        |           |           |
|           |           |           | if there  |           |           |
|           |           |           | is        |           |           |
|           |           |           | initially |           |           |
|           |           |           | no snow   |           |           |
|           |           |           | -  If the |           |           |
|           |           |           | model     |           |           |
|           |           |           | run       |           |           |
|           |           |           | starts    |           |           |
|           |           |           | when      |           |           |
|           |           |           | there     |           |           |
|           |           |           | is no     |           |           |
|           |           |           | snow      |           |           |
|           |           |           | on the    |           |           |
|           |           |           | ground    |           |           |
|           |           |           | ,         |           |           |
|           |           |           | set       |           |           |
|           |           |           | SnowIn    |           |           |
|           |           |           | tially    |           |           |
|           |           |           | = 0       |           |           |
|           |           |           | and       |           |           |
|           |           |           | the       |           |           |
|           |           |           | snow-r    |           |           |
|           |           |           | elated    |           |           |
|           |           |           | parame    |           |           |
|           |           |           | ters      |           |           |
|           |           |           | will      |           |           |
|           |           |           | be set    |           |           |
|           |           |           | accord    |           |           |
|           |           |           | ingly.    |           |           |
|           |           |           | -  If the |           |           |
|           |           |           | model     |           |           |
|           |           |           | run       |           |           |
|           |           |           | starts    |           |           |
|           |           |           | when      |           |           |
|           |           |           | there     |           |           |
|           |           |           | is        |           |           |
|           |           |           | snow      |           |           |
|           |           |           | on the    |           |           |
|           |           |           | ground    |           |           |
|           |           |           | ,         |           |           |
|           |           |           | the       |           |           |
|           |           |           | follow    |           |           |
|           |           |           | ing       |           |           |
|           |           |           | snow-r    |           |           |
|           |           |           | elated    |           |           |
|           |           |           | parame    |           |           |
|           |           |           | ters      |           |           |
|           |           |           | must      |           |           |
|           |           |           | be set    |           |           |
|           |           |           | approp    |           |           |
|           |           |           | riately.  |           |           |
|           |           |           | -  The    |           |           |
|           |           |           | value     |           |           |
|           |           |           | of        |           |           |
|           |           |           | SnowIn    |           |           |
|           |           |           | itially   |           |           |
|           |           |           | overri    |           |           |
|           |           |           | des       |           |           |
|           |           |           | any       |           |           |
|           |           |           | values    |           |           |
|           |           |           | provid    |           |           |
|           |           |           | ed        |           |           |
|           |           |           | for       |           |           |
|           |           |           | the       |           |           |
|           |           |           | indivi    |           |           |
|           |           |           | dual      |           |           |
|           |           |           | snow-r    |           |           |
|           |           |           | elated    |           |           |
|           |           |           | parame    |           |           |
|           |           |           | ters.     |           |           |
|           |           |           | -  To     |           |           |
|           |           |           | preven    |           |           |
|           |           |           | t         |           |           |
|           |           |           | SnowIn    |           |           |
|           |           |           | itially   |           |           |
|           |           |           | from      |           |           |
|           |           |           | settin    |           |           |
|           |           |           | g         |           |           |
|           |           |           | the       |           |           |
|           |           |           | initia    |           |           |
|           |           |           | l         |           |           |
|           |           |           | condit    |           |           |
|           |           |           | ions,     |           |           |
|           |           |           | either    |           |           |
|           |           |           | omit      |           |           |
|           |           |           | it        |           |           |
|           |           |           | from      |           |           |
|           |           |           | the       |           |           |
|           |           |           | nameli    |           |           |
|           |           |           | st        |           |           |
|           |           |           | or set    |           |           |
|           |           |           | to        |           |           |
|           |           |           | -999.     |           |           |
|           |           |           | \*If      |           |           |
|           |           |           | values    |           |           |
|           |           |           | are       |           |           |
|           |           |           | provided  |           |           |
|           |           |           | individua |           |           |
|           |           |           | lly,      |           |           |
|           |           |           | they      |           |           |
|           |           |           | should be |           |           |
|           |           |           | consisten |           |           |
|           |           |           | t         |           |           |
|           |           |           | the       |           |           |
|           |           |           | informati |           |           |
|           |           |           | on        |           |           |
|           |           |           | provided  |           |           |
|           |           |           | in        |           |           |
|           |           |           | [[#SUEWS_ |           |           |
|           |           |           | Snow.txt  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| PavedStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | on paved  |           |           |
|           |           |           | surfaces. |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| BldgsStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | on        |           |           |
|           |           |           | buildings |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| EveTrStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | on        |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| DecTrStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | on        |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| GrassStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | on grass  |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| BSoilStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | on bare   |           |           |
|           |           |           | soil      |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowWater | O         | mm        | Initial   |           |           |
| WaterStat |           |           | amount of |           |           |
| e         |           |           | liquid    |           |           |
|           |           |           | water in  |           |           |
|           |           |           | the snow  |           |           |
|           |           |           | in water  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackP | O         | mm        | Initial   |           |           |
| aved      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | paved     |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackB | O         | mm        | Initial   |           |           |
| ldgs      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | buildings |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackE | O         | mm        | Initial   |           |           |
| veTr      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackD | O         | mm        | Initial   |           |           |
| ecTr      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackG | O         | mm        | Initial   |           |           |
| rass      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | grass     |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackB | O         | mm        | Initial   |           |           |
| Soil      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | bare soil |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowPackW | O         | mm        | Initial   |           |           |
| ater      |           |           | snow      |           |           |
|           |           |           | water     |           |           |
|           |           |           | equivalen |           |           |
|           |           |           | t         |           |           |
|           |           |           | if the    |           |           |
|           |           |           | snow on   |           |           |
|           |           |           | water     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracP | O         | -         | Initial   |           |           |
| aved      |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on paved  |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracB | O         | -         | Initial   |           |           |
| ldgs      |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on        |           |           |
|           |           |           | buildings |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracE | O         | -         | Initial   |           |           |
| veTr      |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on        |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracD | O         | -         | Initial   |           |           |
| ecTr      |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on        |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracG | O         | -         | Initial   |           |           |
| ras       |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on grass  |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracB | O         | -         | Initial   |           |           |
| Soil      |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on bare   |           |           |
|           |           |           | soil      |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowFracW | O         | -         | Initial   |           |           |
| ater      |           |           | plan area |           |           |
|           |           |           | fraction  |           |           |
|           |           |           | of snow   |           |           |
|           |           |           | on water  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensP | O         | kg        | Initial   |           |           |
| aved      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on paved  |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensB | O         | kg        | Initial   |           |           |
| ldgs      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on        |           |           |
|           |           |           | buildings |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensE | O         | kg        | Initial   |           |           |
| veTr      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on        |           |           |
|           |           |           | evergreen |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensD | O         | kg        | Initial   |           |           |
| ecTr      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on        |           |           |
|           |           |           | deciduous |           |           |
|           |           |           | trees     |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensG | O         | kg        | Initial   |           |           |
| rass      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on grass  |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensB | O         | kg        | Initial   |           |           |
| Soil      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on bare   |           |           |
|           |           |           | soil      |           |           |
|           |           |           | surfaces  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+
| SnowDensW | O         | kg        | Initial   |           |           |
| ater      |           | m\ :sup:` | snow      |           |           |
|           |           | -3`       | density   |           |           |
|           |           |           | on water  |           |           |
+-----------+-----------+-----------+-----------+-----------+-----------+