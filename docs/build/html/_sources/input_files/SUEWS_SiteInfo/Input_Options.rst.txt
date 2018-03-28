Input_Options
~~~~~~~~~~~~~

.. option:: a1

	:Description:
		Coefficient for Q* term [-]

	:Configuration:
		.. csv-table::
			:file: a1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: a2

	:Description:
		Coefficient for dQ*/dt term [h]

	:Configuration:
		.. csv-table::
			:file: a2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: a3

	:Description:
		Constant term [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: a3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ActivityProfWD

	:Description:
		Code for human activity profile (weekdays) Provides the link to column 1 of SUEWS_Profiles.txt. Look the codes Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. Used for CO2 flux calculation - not used in v2017a 

	:Configuration:
		.. csv-table::
			:file: ActivityProfWD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ActivityProfWE

	:Description:
		Code for human activity profile (weekends) Provides the link to column 1 of SUEWS_Profiles.txt. Look the codes Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. Used for CO2 flux calculation - not used in v2017a 

	:Configuration:
		.. csv-table::
			:file: ActivityProfWE.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AHMin

	:Description:
		Use with AnthropHeatMethod = 1

	:Configuration:
		.. csv-table::
			:file: AHMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AHSlope

	:Description:
		Use with AnthropHeatMethod = 1

	:Configuration:
		.. csv-table::
			:file: AHSlope.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AlbedoMax

	:Description:
		Effective surface albedo (middle of the day value) for summertime. View factors should be taken into account. Effective surface albedo (middle of the day value) for summertime, full leaf-on. View factors should be taken into account. Example values [-] 0.1 EveTr Oke (1987) [35]  0.18 DecTr Oke (1987) [35]  0.21 Grass Oke (1987) [35]  Effective albedo of the water surface. View factors should be taken into account. Example values [-] 0.1 Water Oke (1987) [35]  Example values [-] 0.85 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: AlbedoMax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AlbedoMin

	:Description:
		Effective surface albedo (middle of the day value) for wintertime (not including snow). View factors should be taken into account. Not currently used for non-vegetated surfaces – set the same as AlbedoMax. Effective surface albedo (middle of the day value) for wintertime (not including snow), leaf-off. View factors should be taken into account. Example values [-] 0.1 EveTr Oke (1987) [35]  0.18 DecTr Oke (1987) [35]  0.21 Grass Oke (1987) [35]  View factors should be taken into account. Not currently used for water surface - set same as AlbedoMax. Example values [-] 0.18 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: AlbedoMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Alt

	:Description:
		Used for both the radiation and water flow between grids. ( N.B. water flow between grids not currently implemented. )

	:Configuration:
		.. csv-table::
			:file: Alt.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AnOHM_Ch

	:Description:
		Bulk transfer coefficient for this surface to use in AnOHM [-] Bulk transfer coefficient for this surface to use in AnOHM [-] Bulk transfer coefficient for this surface to use in AnOHM [-] Bulk transfer coefficient for this surface to use in AnOHM [-]

	:Configuration:
		.. csv-table::
			:file: AnOHM_Ch.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AnOHM_Cp

	:Description:
		Volumetric heat capacity for this surface to use in AnOHM [J m -3 ] Volumetric heat capacity for this surface to use in AnOHM [J m -3 ] Volumetric heat capacity for this surface to use in AnOHM [J m -3 ] Volumetric heat capacity for this surface to use in AnOHM [J m -3 ]

	:Configuration:
		.. csv-table::
			:file: AnOHM_Cp.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AnOHM_Kk

	:Description:
		Thermal conductivity for this surface to use in AnOHM [W m K -1 ] Thermal conductivity for this surface to use in AnOHM [W m K -1 ] Thermal conductivity for this surface to use in AnOHM [W m K -1 ] Thermal conductivity for this surface to use in AnOHM [W m K -1 ]

	:Configuration:
		.. csv-table::
			:file: AnOHM_Kk.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AnthropogenicCode

	:Description:
		Code for modelling anthropogenic heat flux Provides the link to column 1 of SUEWS_AnthropogenicHeat.txt, which contains the model coefficients for estimation of the anthropogenic heat flux (used if AnthropHeatChoice = 1, 2 in RunControl.nml ). Value of integer is arbitrary but must match code specified in column 1 of SUEWS_AnthropogenicHeat.txt. 

	:Configuration:
		.. csv-table::
			:file: AnthropogenicCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: AreaWall

	:Description:
		Area of wall within grid (needed for ESTM calculation).

	:Configuration:
		.. csv-table::
			:file: AreaWall.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: BaseT

	:Description:
		See section 2.2 Järvi et al. (2011); Appendix A Järvi et al. (2014). Example values [°C] 5 EveTr Järvi et al. (2011) [1]  5 DecTr Järvi et al. (2011) [1]  5 Grass Järvi et al. (2011) [1] 

	:Configuration:
		.. csv-table::
			:file: BaseT.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: BaseTe

	:Description:
		See section 2.2 Järvi et al. (2011) [1] ; Appendix A Järvi et al. (2014) [15] . Example values [°C] 10 EveTr Järvi et al. (2011) [1]  10 DecTr Järvi et al. (2011) [1]  10 Grass Järvi et al. (2011) [1] 

	:Configuration:
		.. csv-table::
			:file: BaseTe.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: BaseTHDD

	:Description:
		Base temperature for heating degree days [°C] e.g. Sailor and Vasireddy (2006) [39] 

	:Configuration:
		.. csv-table::
			:file: BaseTHDD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: BuildEnergyUse

	:Description:
		Building energy use [W m-2] Can be used for CO2 flux calculation. Do not use in v2017a - set to -999 

	:Configuration:
		.. csv-table::
			:file: BuildEnergyUse.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code

	:Description:
		Code linking to SUEWS_SiteSelect.txt for paved surfaces (Code_Paved), buildings (Code_Bldgs) and bare soil surfaces (Code_BSoil). Value of integer is arbitrary but must match codes specified in SUEWS_SiteSelect.txt.  Code linking to SUEWS_SiteSelect.txt for evergreen trees and shrubs (Code_EveTr), deciduous trees and shrubs (Code_DecTr) and grass surfaces (Code_Grass). Value of integer is arbitrary but must match codes specified in SUEWS_SiteSelect.txt.  Code linking to SUEWS_SiteSelect.txt for water surfaces (Code_Water). Value of integer is arbitrary but must match code specified in SUEWS_SiteSelect.txt.  Code linking to SUEWS_SiteSelect.txt for snow surfaces (SnowCode). Value of integer is arbitrary but must match code specified in SUEWS_SiteSelect.txt.  Code linking to the SoilTypeCode column in SUEWS_NonVeg.txt (for Paved, Bldgs and BSoil surfaces) and SUEWS_Veg.txt (for EveTr, DecTr and Grass surfaces). Value of integer is arbitrary but must match code specified in SUEWS_SiteSelect.txt.  Code linking to the CondCode column in SUEWS_SiteSelect.txt . Value of integer is arbitrary but must match code specified in SUEWS_SiteSelect.txt.  Code linking to the AnthropogenicCode column in SUEWS_SiteSelect.txt . Value of integer is arbitrary but must match code specified in SUEWS_SiteSelect.txt.  Code linking to [[#SUEWS_SiteSelect.txt|SUEWS_SiteSelect.txt] for irrigation modelling (IrrigationCode). Value of integer is arbitrary but must match codes specified in SUEWS_SiteSelect.txt.  Code linking to the OHMCode_SummerWet, OHMCode_SummerDry, OHMCode_WinterWet and OHMCode_WinterDry columns in SUEWS_NonVeg.txt, SUEWS_Veg,txt, SUEWS_Water.txt and SUEWS_Snow.txt files. Value of integer is arbitrary but must match code specified in SUEWS_SiteSelect.txt.  For buildings and paved surfaces, set to zero if there is more than one ESTM class per grid and the codes and surface fractions specified in SUEWS_SiteSelect.txt will be used instead.

	:Configuration:
		.. csv-table::
			:file: Code.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_Bldgs

	:Description:
		Code for Bldgs surface characteristics Provides the link to column 1 of SUEWS_NonVeg.txt, which contains the attributes describing buildings in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_NonVeg.txt. 

	:Configuration:
		.. csv-table::
			:file: Code_Bldgs.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_Bsoil

	:Description:
		Code for BSoil surface characteristics Provides the link to column 1 of SUEWS_NonVeg.txt, which contains the attributes describing bare soil in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_NonVeg.txt. 

	:Configuration:
		.. csv-table::
			:file: Code_Bsoil.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_DecTr

	:Description:
		Code for DecTr surface characteristics Provides the link to column 1 of SUEWS_Veg.txt, which contains the attributes describing deciduous trees and shrubs in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Veg.txt. 

	:Configuration:
		.. csv-table::
			:file: Code_DecTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Bldgs1

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Bldgs1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Bldgs2

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Bldgs2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Bldgs3

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Bldgs3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Bldgs4

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Bldgs4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Bldgs5

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Bldgs5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Paved1

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Paved1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Paved2

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Paved2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_ESTMClass_Paved3

	:Description:
		Code linking to SUEWS_ESTMCoefficients.txt 

	:Configuration:
		.. csv-table::
			:file: Code_ESTMClass_Paved3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_EveTr

	:Description:
		Code for EveTr surface characteristics Provides the link to column 1 of SUEWS_Veg.txt, which contains the attributes describing evergreen trees and shrubs in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Veg.txt. 

	:Configuration:
		.. csv-table::
			:file: Code_EveTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_Grass

	:Description:
		Code for Grass surface characteristics Provides the link to column 1 of SUEWS_Veg.txt, which contains the attributes describing grass surfaces in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Veg.txt. 

	:Configuration:
		.. csv-table::
			:file: Code_Grass.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_Paved

	:Description:
		Code for Paved surface characteristics Provides the link to column 1 of SUEWS_NonVeg.txt, which contains the attributes describing paved areas in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_NonVeg.txt. e.g. 331 means use the characteristics specified in the row of input file SUEWS_NonVeg.txt which has 331 in column 1 (Code). 

	:Configuration:
		.. csv-table::
			:file: Code_Paved.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Code_Water

	:Description:
		Code for Water surface characteristics Provides the link to column 1 of SUEWS_Water.txt, which contains the attributes describing open water in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Water.txt. 

	:Configuration:
		.. csv-table::
			:file: Code_Water.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: CondCode

	:Description:
		Code for surface conductance parameters Provides the link to column 1 of SUEWS_Conductance.txt, which contains the parameters for the Jarvis (1976) parameterisation of surface conductance. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Conductance.txt. e.g. 33 means use the characteristics specified in the row of input file SUEWS_Conductance.txt which has 33 in column 1 (Code). 

	:Configuration:
		.. csv-table::
			:file: CondCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: CRWMax

	:Description:
		Maximum water holding capacity of snow [mm]

	:Configuration:
		.. csv-table::
			:file: CRWMax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: CRWMin

	:Description:
		Minimum water holding capacity of snow [mm]

	:Configuration:
		.. csv-table::
			:file: CRWMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(1)

	:Description:
		Irrigation allowed on Sundays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(1).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(2)

	:Description:
		Irrigation allowed on Mondays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(2).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(3)

	:Description:
		Irrigation allowed on Tuesdays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(3).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(4)

	:Description:
		Irrigation allowed on Wednesdays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(4).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(5)

	:Description:
		Irrigation allowed on Thursdays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(5).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(6)

	:Description:
		Irrigation allowed on Fridays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(6).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWat(7)

	:Description:
		Irrigation allowed on Saturdays [1], if not [0]

	:Configuration:
		.. csv-table::
			:file: DayWat(7).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(1)

	:Description:
		Fraction of properties using irrigation on Sundays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(1).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(2)

	:Description:
		Fraction of properties using irrigation on Mondays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(2).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(3)

	:Description:
		Fraction of properties using irrigation on Tuesdays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(3).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(4)

	:Description:
		Fraction of properties using irrigation on Wednesdays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(4).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(5)

	:Description:
		Fraction of properties using irrigation on Thursdays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(5).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(6)

	:Description:
		Fraction of properties using irrigation on Fridays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(6).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DayWatPer(7)

	:Description:
		Fraction of properties using irrigation on Saturdays [0-1]

	:Configuration:
		.. csv-table::
			:file: DayWatPer(7).csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DrainageCoef1

	:Description:
		Example values DrainageEq 10 Coefficient D0 [mm h -1 ] 3 Recommended [3] for Paved and Bldgs 0.013 Coefficient D0 [mm h -1 ] 2 Recommended [3] for BSoil Example values DrainageEq 10 Coefficient D0 [mm h -1 ] 3 Recommended [3] for Grass (irrigated) 0.013 Coefficient D0 [mm h -1 ] 2 Recommended [3] for EveTr, DecTr, Grass (unirrigated) Not currently used for water surface

	:Configuration:
		.. csv-table::
			:file: DrainageCoef1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DrainageCoef2

	:Description:
		Example values DrainageEq 3 Coefficient b [-] 3 Recommended [3] for Paved and Bldgs 1.71 Coefficient b [mm -1 ] 2 Recommended [3] for BSoil Example values DrainageEq 3 Coefficient b [-] 3 Recommended [3] for Grass (irrigated) 1.71 Coefficient b [mm -1 ] 2 Recommended [3] for EveTr, DecTr, Grass (unirrigated) Not currently used for water surface

	:Configuration:
		.. csv-table::
			:file: DrainageCoef2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: DrainageEq

	:Description:
		Options 1 Falk and Niemczynowicz (1978) [32] 2 Halldin et al. (1979) [33] (Rutter eqn corrected for c=0, see Calder & Wright (1986) [34] ) Recommended [3] for BSoil 3 Falk and Niemczynowicz (1978) [32] Recommended [3] for Paved and Bldgs Coefficients are specified in the following two columns. Options 1 Falk and Niemczynowicz (1978) [32] 2 Halldin et al. (1979) [33] (Rutter eqn corrected for c=0, see Calder & Wright (1986) [34] ) Recommended [3] for EveTr, DecTr, Grass (unirrigated) 3 Falk and Niemczynowicz (1978) [32] Recommended [3] for Grass (irrigated) Coefficients are specified in the following two columns. Not currently used for water surface.

	:Configuration:
		.. csv-table::
			:file: DrainageEq.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Emissivity

	:Description:
		Effective surface emissivity. View factors should be taken into account. Effective surface emissivity. View factors should be taken into account. Example values [-] 0.98 EveTr Oke (1987) [35]  0.98 DecTr Oke (1987) [35]  0.93 Grass Oke (1987) [35]  Effective surface emissivity. View factors should be taken into account Example values [-] 0.95 Water Oke (1987) [35]  Effective surface emissivity. View factors should be taken into account Example values [-] 0.99 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: Emissivity.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: EndDLS

	:Description:
		End of the day light savings [DOY] See section on Day Light Savings . 

	:Configuration:
		.. csv-table::
			:file: EndDLS.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: EnergyUseProfWD

	:Description:
		Code for energy use profile (weekdays) Provides the link to column 1 of SUEWS_Profiles.txt. Look the codes Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. 

	:Configuration:
		.. csv-table::
			:file: EnergyUseProfWD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: EnergyUseProfWE

	:Description:
		Code for energy use profile (weekends) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. 

	:Configuration:
		.. csv-table::
			:file: EnergyUseProfWE.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ESTMCode

	:Description:
		For paved and building surfaces, it is possible to specify multiple codes per grid (3 for paved, 5 for buildings) using SUEWS_SiteSelect.txt . In this case, set ESTMCode here to zero. Code for ESTM coefficients to use for this surface. Links to SUEWS_ESTMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_ESTMCoefficients.txt.  Code for ESTM coefficients to use for this surface. Links to SUEWS_ESTMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_ESTMCoefficients.txt.  For paved and building surfaces, it is possible to specify multiple codes per grid (3 for paved, 5 for buildings) using SUEWS_SiteSelect.txt . In this case, set ESTM code here to zero.

	:Configuration:
		.. csv-table::
			:file: ESTMCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: FAI_Bldgs

	:Description:
		Frontal area index for buildings [-] Required if RoughLenMomMethod = 3 in RunControl.nml . 

	:Configuration:
		.. csv-table::
			:file: FAI_Bldgs.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: FAI_DecTr

	:Description:
		Frontal area index for deciduous trees [-] Required if RoughLenMomMethod = 3 in RunControl.nml . 

	:Configuration:
		.. csv-table::
			:file: FAI_DecTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: FAI_EveTr

	:Description:
		Frontal area index for evergreen trees [-] Required if RoughLenMomMethod = 3 in RunControl.nml . 

	:Configuration:
		.. csv-table::
			:file: FAI_EveTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Faut

	:Description:
		Fraction of irrigated area that is irrigated using automated systems (e.g. sprinklers).

	:Configuration:
		.. csv-table::
			:file: Faut.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: fcld

	:Description:
		Cloud fraction [tenths]

	:Configuration:
		.. csv-table::
			:file: fcld.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: FlowChange

	:Description:
		Difference in input and output flows for water surface [mm h -1 ] Used to indicate river or stream flow through the grid. Currently not fully tested! 

	:Configuration:
		.. csv-table::
			:file: FlowChange.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction1of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction1of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction2of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction2of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction3of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction3of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction4of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction4of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction5of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction5of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction6of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction6of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction7of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction7of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fraction8of8

	:Description:
		Fraction of water that can flow to the grid specified in previous column [-]

	:Configuration:
		.. csv-table::
			:file: Fraction8of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_Bldgs

	:Description:
		Surface cover fraction of buildings [-]

	:Configuration:
		.. csv-table::
			:file: Fr_Bldgs.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_Bsoil

	:Description:
		Surface cover fraction of bare soil or unmanaged land [-]

	:Configuration:
		.. csv-table::
			:file: Fr_Bsoil.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_DecTr

	:Description:
		Surface cover fraction of deciduous trees and shrubs [-]

	:Configuration:
		.. csv-table::
			:file: Fr_DecTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Bldgs1

	:Description:
		Columns 94-98 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Bldgs1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Bldgs2

	:Description:
		Columns 94-98 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Bldgs2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Bldgs3

	:Description:
		Columns 94-98 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Bldgs3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Bldgs4

	:Description:
		Columns 94-98 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Bldgs4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Bldgs5

	:Description:
		Columns 94-98 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Bldgs5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Paved1

	:Description:
		Columns 88-90 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Paved1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Paved2

	:Description:
		Columns 88-90 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Paved2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_ESTMClass_Paved3

	:Description:
		Columns 88-90 must add up to 1

	:Configuration:
		.. csv-table::
			:file: Fr_ESTMClass_Paved3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_EveTr

	:Description:
		Surface cover fraction of evergreen trees and shrubs [-]

	:Configuration:
		.. csv-table::
			:file: Fr_EveTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_Grass

	:Description:
		Surface cover fraction of grass [-]

	:Configuration:
		.. csv-table::
			:file: Fr_Grass.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_Paved

	:Description:
		Columns 14 to 20 must sum to 1 .

	:Configuration:
		.. csv-table::
			:file: Fr_Paved.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Fr_Water

	:Description:
		Surface cover fraction of open water [-] (e.g. river, lakes, ponds, swimming pools) 

	:Configuration:
		.. csv-table::
			:file: Fr_Water.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: G1

	:Description:
		Related to maximum surface conductance [mm s -1 ]

	:Configuration:
		.. csv-table::
			:file: G1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: G2

	:Description:
		Related to Kdown dependence [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: G2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: G3

	:Description:
		Related to VPD dependence [units depend on gsChoice in RunControl.nml ]

	:Configuration:
		.. csv-table::
			:file: G3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: G4

	:Description:
		Related to VPD dependence [units depend on gsChoice in RunControl.nml ]

	:Configuration:
		.. csv-table::
			:file: G4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: G5

	:Description:
		Related to temperature dependence [°C]

	:Configuration:
		.. csv-table::
			:file: G5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: G6

	:Description:
		Related to soil moisture dependence [mm -1 ]

	:Configuration:
		.. csv-table::
			:file: G6.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: gamq_gkgm

	:Description:
		vertical gradient of specific humidity (g kg -1 m -1 )

	:Configuration:
		.. csv-table::
			:file: gamq_gkgm.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: gamt_Km

	:Description:
		vertical gradient of potential temperature (K m -1 ) strength of the inversion

	:Configuration:
		.. csv-table::
			:file: gamt_Km.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GDDFull

	:Description:
		This should be checked carefully for your study area using modelled LAI from the DailyState output file compared to known behaviour in the study area. See section 2.2 Järvi et al. (2011) [1] ; Appendix A Järvi et al. (2014) [15] for more details. Example values [°C] 300 EveTr Järvi et al. (2011) [1]  300 DecTr Järvi et al. (2011) [1]  300 Grass Järvi et al. (2011) [1] 

	:Configuration:
		.. csv-table::
			:file: GDDFull.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Grid

	:Description:
		Grid numbers do not need to be consecutive and do not need to start at a particular value. Each grid must have a unique grid number. All grids must be present for all years. These grid numbers are referred to in GridConnections (columns 64-79) ( N.B. GridConnections not currently implemented! )

	:Configuration:
		.. csv-table::
			:file: Grid.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection1of8

	:Description:
		The next 8 pairs of columns specify the water flow between grids. The first column of each pair specifies the grid that the water flows to (from the current grid, column 1); the second column of each pair specifies the fraction of water that flow to that grid. The fraction (i.e. amount) of water transferred may be estimated based on elevation, the length of connecting surface between grids, presence of walls, etc. Water cannot flow from the current grid to the same grid, so the grid number here must be different to the grid number in column 1. Water can flow to a maximum of 8 other grids. If there is no water flow between grids, or a single grid is run, set to 0. See section on Grid Connections

	:Configuration:
		.. csv-table::
			:file: GridConnection1of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection2of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection2of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection3of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection3of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection4of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection4of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection5of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection5of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection6of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection6of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection7of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection7of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: GridConnection8of8

	:Description:
		Number of the grid where water can flow to

	:Configuration:
		.. csv-table::
			:file: GridConnection8of8.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: gsModel

	:Description:
		1 = Järvi et al. (2011) [1] 2 = Ward et al. (2016) [2] Recommended.

	:Configuration:
		.. csv-table::
			:file: gsModel.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: H_Bldgs

	:Description:
		Mean building height [m]

	:Configuration:
		.. csv-table::
			:file: H_Bldgs.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: H_DecTr

	:Description:
		Mean height of deciduous trees [m]

	:Configuration:
		.. csv-table::
			:file: H_DecTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: H_EveTr

	:Description:
		Mean height of evergreen trees [m]

	:Configuration:
		.. csv-table::
			:file: H_EveTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: id

	:Description:
		Day [DOY] Not used: set to 1 in this version.  Day of year [DOY] Day of year [DOY] Day of year [DOY]

	:Configuration:
		.. csv-table::
			:file: id.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_a1

	:Description:
		Coefficient for automatic irrigation model [mm d -1 ]

	:Configuration:
		.. csv-table::
			:file: Ie_a1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_a2

	:Description:
		Coefficient for automatic irrigation model [mm d -1 °C -1 ]

	:Configuration:
		.. csv-table::
			:file: Ie_a2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_a3

	:Description:
		Coefficient for automatic irrigation model [mm d -2 ]

	:Configuration:
		.. csv-table::
			:file: Ie_a3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_end

	:Description:
		Day when irrigation ends [DOY]

	:Configuration:
		.. csv-table::
			:file: Ie_end.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_m1

	:Description:
		Coefficient for manual irrigation model [mm d -1 ]

	:Configuration:
		.. csv-table::
			:file: Ie_m1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_m2

	:Description:
		Coefficient for manual irrigation model [mm d -1 °C -1 ]

	:Configuration:
		.. csv-table::
			:file: Ie_m2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_m3

	:Description:
		Coefficient for manual irrigation model [mm d -2 ]

	:Configuration:
		.. csv-table::
			:file: Ie_m3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Ie_start

	:Description:
		Day when irrigation starts [DOY]

	:Configuration:
		.. csv-table::
			:file: Ie_start.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ih

	:Description:
		Hour [H] Not used: set to 0 in this version. 

	:Configuration:
		.. csv-table::
			:file: ih.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: imin

	:Description:
		Minute [M] Not used: set to 0 in this version.  Minute [M] Minute [M]

	:Configuration:
		.. csv-table::
			:file: imin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: InfiltrationRate

	:Description:
		Not currently used

	:Configuration:
		.. csv-table::
			:file: InfiltrationRate.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_albedo

	:Description:
		Albedo of all internal elements for building surfaces only

	:Configuration:
		.. csv-table::
			:file: Internal_albedo.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_CHbld

	:Description:
		Bulk transfer coefficient of internal building elements [W m -2 K -1 ] (for building surfaces only and if IbldCHmod == 0 in ESTMinput.nml 

	:Configuration:
		.. csv-table::
			:file: Internal_CHbld.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_CHroof

	:Description:
		Bulk transfer coefficient of internal roof [W m -2 K -1 ] (for building surfaces only and if IbldCHmod == 0 in ESTMinput.nml 

	:Configuration:
		.. csv-table::
			:file: Internal_CHroof.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_CHwall

	:Description:
		Bulk transfer coefficient of internal wall [W m -2 K -1 ] (for building surfaces only and if IbldCHmod == 0 in ESTMinput.nml 

	:Configuration:
		.. csv-table::
			:file: Internal_CHwall.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_emissivity

	:Description:
		Emissivity of all internal elements for building surfaces only

	:Configuration:
		.. csv-table::
			:file: Internal_emissivity.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_k1

	:Description:
		Thermal conductivity of the first layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_k1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_k2

	:Description:
		Thermal conductivity of the second layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_k2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_k3

	:Description:
		Thermal conductivity of the third layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_k3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_k4

	:Description:
		Thermal conductivity of the fourth layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_k4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_k5

	:Description:
		Thermal conductivity of the fifth layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_k5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_rhoCp1

	:Description:
		Volumetric heat capacity of the first layer[J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_rhoCp1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_rhoCp2

	:Description:
		Volumetric heat capacity of the second layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_rhoCp2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_rhoCp3

	:Description:
		Volumetric heat capacity of the third layer[J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_rhoCp3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_rhoCp4

	:Description:
		Volumetric heat capacity of the fourth layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_rhoCp4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_rhoCp5

	:Description:
		Volumetric heat capacity of the fifth layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Internal_rhoCp5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_thick1

	:Description:
		Thickness of the first layer [m] for building surfaces only; set to -999 for all other surfaces

	:Configuration:
		.. csv-table::
			:file: Internal_thick1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_thick2

	:Description:
		Thickness of the second layer [m] (if no second layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Internal_thick2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_thick3

	:Description:
		Thickness of the third layer [m] (if no third layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Internal_thick3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_thick4

	:Description:
		Thickness of the fourth layer [m] (if no fourth layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Internal_thick4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Internal_thick5

	:Description:
		Thickness of the fifth layer [m] (if no fifth layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Internal_thick5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: InternalWaterUse

	:Description:
		Internal water use [mm h -1 ]

	:Configuration:
		.. csv-table::
			:file: InternalWaterUse.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: IrrFr_DecTr

	:Description:
		Fraction of deciduous trees that are irrigated [-]

	:Configuration:
		.. csv-table::
			:file: IrrFr_DecTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: IrrFr_EveTr

	:Description:
		Fraction of evergreen trees that are irrigated [-] e.g. 50% of the evergreen trees/shrubs are irrigated 

	:Configuration:
		.. csv-table::
			:file: IrrFr_EveTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: IrrFr_Grass

	:Description:
		Fraction of grass that is irrigated [-]

	:Configuration:
		.. csv-table::
			:file: IrrFr_Grass.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: IrrigationCode

	:Description:
		Code for modelling irrigation Provides the link to column 1 of SUEWS_Irrigation.txt, which contains the model coefficients for estimation of the water use (used if WU_Choice = 0 in RunControl.nml ). Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Irrigation.txt. 

	:Configuration:
		.. csv-table::
			:file: IrrigationCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: it

	:Description:
		Hour [H] Hour [H]

	:Configuration:
		.. csv-table::
			:file: it.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: iy

	:Description:
		Year [YYYY] Year [YYYY]

	:Configuration:
		.. csv-table::
			:file: iy.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: kdiff

	:Description:
		Recommended if SOLWEIGUse = 1

	:Configuration:
		.. csv-table::
			:file: kdiff.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: kdir

	:Description:
		Recommended if SOLWEIGUse = 1

	:Configuration:
		.. csv-table::
			:file: kdir.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: kdown

	:Description:
		Must be > 0 W m -2 .

	:Configuration:
		.. csv-table::
			:file: kdown.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Kmax

	:Description:
		Maximum incoming shortwave radiation [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: Kmax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: lai

	:Description:
		Observed leaf area index [m -2 m -2 ]

	:Configuration:
		.. csv-table::
			:file: lai.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LAIEq

	:Description:
		Options 0 Järvi et al. (2011) [1]  1 Järvi et al. (2014) [15]  Coefficients are specified in the following four columns. N.B. North and South hemispheres are treated slightly differently.

	:Configuration:
		.. csv-table::
			:file: LAIEq.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LAIMax

	:Description:
		full leaf-on summertime value Example values [m -2 m -2 ] 5.1 EveTr Breuer et al. (2003) [36]  5.5 DecTr Breuer et al. (2003) [36]  5.9 Grass Breuer et al. (2003) [36] 

	:Configuration:
		.. csv-table::
			:file: LAIMax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LAIMin

	:Description:
		leaf-off wintertime value Example values [m -2 m -2 ] 4. EveTr Järvi et al. (2011) [1]  1. DecTr Järvi et al. (2011) [1]  1.6 Grass Grimmond and Oke (1991) [3] and references therein

	:Configuration:
		.. csv-table::
			:file: LAIMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: lat

	:Description:
		Use coordinate system WGS84. Positive values are northern hemisphere (negative southern hemisphere). Used in radiation calculations. Note, if the total modelled area is small the latitude and longitude could be the same for each grid but small differences in radiation will not be determined. If you are defining the latitude and longitude differently between grids make certain that you provide enough decimal places.

	:Configuration:
		.. csv-table::
			:file: lat.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ldown

	:Description:
		Incoming longwave radiation [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: ldown.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LeafGrowthPower1

	:Description:
		Example values LAIEq 0.03 Järvi et al. (2011) [1] 0 0.04 Järvi et al. (2014) [15] 1

	:Configuration:
		.. csv-table::
			:file: LeafGrowthPower1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LeafGrowthPower2

	:Description:
		Example values [°C -1 ] LAIEq 0.0005 Järvi et al. (2011) [1] 0 0.001 Järvi et al. (2014) [15] 1

	:Configuration:
		.. csv-table::
			:file: LeafGrowthPower2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LeafOffPower1

	:Description:
		Example values LAIEq 0.03 Järvi et al. (2011) [1] 0 -1.5 Järvi et al. (2014) [15] 1

	:Configuration:
		.. csv-table::
			:file: LeafOffPower1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LeafOffPower2

	:Description:
		Example values [°C -1 ] LAIEq 0.0005 Järvi et al. (2011) [1] 0 0.0015 Järvi et al. (2014) [15] 1

	:Configuration:
		.. csv-table::
			:file: LeafOffPower2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: lng

	:Description:
		Use coordinate system WGS84. For compatibility with GIS, negative values are to the west, positive values are to the east (e.g. Vancouver = -123.12; Shanghai = 121.47) Note this is a change of sign convention between v2016a and v2017a See latitude for more details.

	:Configuration:
		.. csv-table::
			:file: lng.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LUMPS_Cover

	:Description:
		Limit when surface totally covered with water [mm] Used for LUMPS surface wetness control. Default recommended value of 1 mm from Loridan et al. (2011) [5] . 

	:Configuration:
		.. csv-table::
			:file: LUMPS_Cover.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LUMPS_DrRate

	:Description:
		Drainage rate of bucket for LUMPS [mm h -1 ] Used for LUMPS surface wetness control. Default recommended value of 0.25 mm h -1 from Loridan et al. (2011) [5] . 

	:Configuration:
		.. csv-table::
			:file: LUMPS_DrRate.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: LUMPS_MaxRes

	:Description:
		Maximum water bucket reservoir [mm] Used for LUMPS surface wetness control. Default recommended value of 10 mm from Loridan et al. (2011) [5] . 

	:Configuration:
		.. csv-table::
			:file: LUMPS_MaxRes.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: MaxConductance

	:Description:
		Example values [mm s -1 ] 7.4 EveTr Järvi et al. (2011) [1]  11.7 DecTr Järvi et al. (2011) [1]  33.1 Grass (unirrigated) Järvi et al. (2011) [1]  40. Grass (irrigated) Järvi et al. (2011) [1] 

	:Configuration:
		.. csv-table::
			:file: MaxConductance.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: NARP_Trans

	:Description:
		Atmospheric transmissivity for NARP [-] Value must in the range 0-1. Default recommended value of 1. 

	:Configuration:
		.. csv-table::
			:file: NARP_Trans.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: nroom

	:Description:
		Number of rooms per floor for building surfaces only

	:Configuration:
		.. csv-table::
			:file: nroom.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OBS_SMCap

	:Description:
		Use only if soil moisture is observed and provided in the met forcing file and smd_choice = 1 or 2. Use of observed soil moisture not currently tested

	:Configuration:
		.. csv-table::
			:file: OBS_SMCap.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OBS_SMDepth

	:Description:
		Use only if soil moisture is observed and provided in the met forcing file and smd_choice = 1 or 2. Use of observed soil moisture not currently tested

	:Configuration:
		.. csv-table::
			:file: OBS_SMDepth.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OBS_SoilNotRocks

	:Description:
		Use only if soil moisture is observed and provided in the met forcing file and smd_choice = 1 or 2. Use of observed soil moisture not currently tested

	:Configuration:
		.. csv-table::
			:file: OBS_SoilNotRocks.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OHMCode_SummerDry

	:Description:
		Code for OHM coefficients to use for this surface during dry conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during dry conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during dry conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during dry conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt. 

	:Configuration:
		.. csv-table::
			:file: OHMCode_SummerDry.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OHMCode_SummerWet

	:Description:
		Code for OHM coefficients to use for this surface during wet conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during wet conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during wet conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during wet conditions in summer. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt. 

	:Configuration:
		.. csv-table::
			:file: OHMCode_SummerWet.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OHMCode_WinterDry

	:Description:
		Code for OHM coefficients to use for this surface during dry conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during dry conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during dry conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during dry conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt. 

	:Configuration:
		.. csv-table::
			:file: OHMCode_WinterDry.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OHMCode_WinterWet

	:Description:
		Code for OHM coefficients to use for this surface during wet conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during wet conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during wet conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt.  Code for OHM coefficients to use for this surface during wet conditions in winter. Links to SUEWS_OHMCoefficients.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_OHMCoefficients.txt. 

	:Configuration:
		.. csv-table::
			:file: OHMCode_WinterWet.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OHMThresh_SW

	:Description:
		Temperature threshold determining whether summer/winter OHM coefficients are applied [deg C] If 5-day running mean air temperature is greater than or equal to this threshold, OHM coefficients for summertime are applied; otherwise coefficients for wintertime are applied.  Temperature threshold determining whether summer/winter OHM coefficients are applied [deg C] If 5-day running mean air temperature is greater than or equal to this threshold, OHM coefficients for summertime are applied; otherwise coefficients for wintertime are applied.  Temperature threshold determining whether summer/winter OHM coefficients are applied [deg C] If 5-day running mean air temperature is greater than or equal to this threshold, OHM coefficients for summertime are applied; otherwise coefficients for wintertime are applied.  Temperature threshold determining whether summer/winter OHM coefficients are applied [deg C] If 5-day running mean air temperature is greater than or equal to this threshold, OHM coefficients for summertime are applied; otherwise coefficients for wintertime are applied. Not actually used for Snow surface as winter wet conditions always assumed. 

	:Configuration:
		.. csv-table::
			:file: OHMThresh_SW.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: OHMThresh_WD

	:Description:
		Soil moisture threshold determining whether wet/dry OHM coefficients are applied [-] If soil moisture (as a proportion of maximum soil moisture capacity) exceeds this threshold for bare soil and vegetated surfaces, OHM coefficients for wet conditions are applied; otherwise coefficients for dry coefficients are applied. Note that OHM coefficients for wet conditions are applied if the surface is wet. Not actually used for building and paved surfaces (as impervious).  Soil moisture threshold determining whether wet/dry OHM coefficients are applied [-] If soil moisture (as a proportion of maximum soil moisture capacity) exceeds this threshold for bare soil and vegetated surfaces, OHM coefficients for wet conditions are applied; otherwise coefficients for dry coefficients are applied. Note that OHM coefficients for wet conditions are applied if the surface is wet.  Soil moisture threshold determining whether wet/dry OHM coefficients are applied [-] If soil moisture (as a proportion of maximum soil moisture capacity) exceeds this threshold for bare soil and vegetated surfaces, OHM coefficients for wet conditions are applied; otherwise coefficients for dry coefficients are applied. Note that OHM coefficients for wet conditions are applied if the surface is wet. Not actually used for water surface (as no soil surface beneath).  Soil moisture threshold determining whether wet/dry OHM coefficients are applied [-] If soil moisture (as a proportion of maximum soil moisture capacity) exceeds this threshold for bare soil and vegetated surfaces, OHM coefficients for wet conditions are applied; otherwise coefficients for dry coefficients are applied. Note that OHM coefficients for wet conditions are applied if the surface is wet. Not actually used for Snow surface as winter wet conditions always assumed. 

	:Configuration:
		.. csv-table::
			:file: OHMThresh_WD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PipeCapacity

	:Description:
		Storage capacity of pipes [mm] Runoff amounting to less than the value specified here is assumed to be removed by pipes. 

	:Configuration:
		.. csv-table::
			:file: PipeCapacity.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PopDensDay

	:Description:
		Daytime population density (i.e. workers, tourists) [people ha -1 ] Population density is required if AnthropHeatMethod = 2 in RunControl.nml . The model will use the average of daytime and night-time population densities, unless only one is provided. If daytime population density is unknown, set to -999. 

	:Configuration:
		.. csv-table::
			:file: PopDensDay.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PopDensNight

	:Description:
		Night-time population density (i.e. residents) [people ha -1 ] Population density is required if AnthropHeatMethod = 2 in RunControl.nml . The model will use the average of daytime and night-time population densities, unless only one is provided. If night-time population density is unknown, set to -999. 

	:Configuration:
		.. csv-table::
			:file: PopDensNight.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PorosityMax

	:Description:
		full leaf-on summertime value Used only for DecTr (can affect roughness calculation)

	:Configuration:
		.. csv-table::
			:file: PorosityMax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PorosityMin

	:Description:
		leaf-off wintertime value Used only for DecTr (can affect roughness calculation)

	:Configuration:
		.. csv-table::
			:file: PorosityMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PrecipiLimAlb

	:Description:
		Limit for hourly precipitation when the ground is fully covered with snow. Then snow albedo is reset to AlbedoMax [mm]

	:Configuration:
		.. csv-table::
			:file: PrecipiLimAlb.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: PrecipLimSnow

	:Description:
		Auer (1974) [38]

	:Configuration:
		.. csv-table::
			:file: PrecipLimSnow.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: pres

	:Description:
		Barometric pressure [kPa]

	:Configuration:
		.. csv-table::
			:file: pres.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: qe

	:Description:
		Latent heat flux [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: qe.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: qf

	:Description:
		Anthropogenic heat flux [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: qf.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: QF_A_Weekday

	:Description:
		Use with AnthropHeatChoice = 2 Example values [W m -2 (Cap ha-1) -1 ] 0.3081 Järvi et al. (2011) [1]  0.1 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: QF_A_Weekday.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: QF_A_Weekend

	:Description:
		Use with AnthropHeatMethod = 2 Example values [W m -2 (Cap ha -1 ) -1 ] 0.3081 Järvi et al. (2011) [1]  0.1 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: QF_A_Weekend.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: QF_B_Weekday

	:Description:
		Use with AnthropHeatMethod = 2 Example values [W m -2 K -1 (Cap ha -1 ) -1 ] 0.0099 Järvi et al. (2011) [1]  0.0099 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: QF_B_Weekday.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: QF_B_Weekend

	:Description:
		Use with AnthropHeatMethod = 2 Example values [W m -2 K -1 (Cap ha -1 ) -1 ] 0.0099 Järvi et al. (2011) [1]  0.0099 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: QF_B_Weekend.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: QF_C_Weekday

	:Description:
		Use with AnthropHeatMethod = 2 Example values [W m -2 K -1 (Cap ha -1 ) -1 ] 0.0102 Järvi et al. (2011) [1]  0.0102 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: QF_C_Weekday.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: QF_C_Weekend

	:Description:
		Example values [W m -2 K -1 (Cap ha -1 ) -1 ] 0.0102 Järvi et al. (2011) [1]  0.0102 Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: QF_C_Weekend.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: q+_gkg

	:Description:
		specific humidity at the top of CBL (g kg -1 )

	:Configuration:
		.. csv-table::
			:file: q+_gkg.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: q_gkg

	:Description:
		specific humidiy in CBL (g kg -1 )

	:Configuration:
		.. csv-table::
			:file: q_gkg.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: qh

	:Description:
		Sensible heat flux [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: qh.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: qn

	:Description:
		Required if NetRadiationMethod = 1.

	:Configuration:
		.. csv-table::
			:file: qn.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: qs

	:Description:
		Storage heat flux [W m -2 ]

	:Configuration:
		.. csv-table::
			:file: qs.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: RadMeltFactor

	:Description:
		Hourly radiation melt factor of snow [mm W -1 h -1 ]

	:Configuration:
		.. csv-table::
			:file: RadMeltFactor.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: rain

	:Description:
		Rainfall [mm]

	:Configuration:
		.. csv-table::
			:file: rain.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: RH

	:Description:
		Relative Humidity [%]

	:Configuration:
		.. csv-table::
			:file: RH.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: RunoffToWater

	:Description:
		Fraction of above-ground runoff flowing to water surface during flooding [-] Value must be in the range 0-1. Fraction of above-ground runoff that can flow to the water surface in the case of flooding. 

	:Configuration:
		.. csv-table::
			:file: RunoffToWater.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: S1

	:Description:
		Related to soil moisture dependence [-] These will change in the future to ensure consistency with soil behaviour 

	:Configuration:
		.. csv-table::
			:file: S1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: S2

	:Description:
		Related to soil moisture dependence [mm] These will change in the future to ensure consistency with soil behaviour 

	:Configuration:
		.. csv-table::
			:file: S2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SatHydraulicCond

	:Description:
		Hydraulic conductivity for saturated soil [mm s -1 ]

	:Configuration:
		.. csv-table::
			:file: SatHydraulicCond.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SDDFull

	:Description:
		This should be checked carefully for your study area using modelled LAI from the DailyState output file compared to known behaviour in the study area. See section 2.2 Järvi et al. (2011) [1] ; Appendix A Järvi et al. (2014) [15] for more details. Example values [°C] -450 EveTr Järvi et al. (2011) [1]  -450 DecTr Järvi et al. (2011) [1]  -450 Grass Järvi et al. (2011) [1] 

	:Configuration:
		.. csv-table::
			:file: SDDFull.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: snow

	:Description:
		Required if SnowUse = 1

	:Configuration:
		.. csv-table::
			:file: snow.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SnowClearingProfWD

	:Description:
		Code for snow clearing profile (weekdays) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. e.g. 1 means use the characteristics specified in the row of input file SUEWS_Profiles.txt which has 1 in column 1 (Code). 

	:Configuration:
		.. csv-table::
			:file: SnowClearingProfWD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SnowClearingProfWE

	:Description:
		Code for snow clearing profile (weekends) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. e.g. 1 means use the characteristics specified in the row of input file SUEWS_Profiles.txt which has 1 in column 1 (Code). Providing the same code for SnowClearingProfWD and SnowClearingProfWE would link to the same row in SUEWS_Profiles.txt, i.e. the same profile would be used for weekdays and weekends. 

	:Configuration:
		.. csv-table::
			:file: SnowClearingProfWE.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SnowCode

	:Description:
		Code for snow surface characteristics Provides the link to column 1 of SUEWS_Snow.txt, which contains the attributes describing snow surfaces in this grid for this year. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Snow.txt. 

	:Configuration:
		.. csv-table::
			:file: SnowCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: snowDensMax

	:Description:
		Maximum snow density [kg m -3 ]

	:Configuration:
		.. csv-table::
			:file: snowDensMax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: snowDensMin

	:Description:
		Fresh snow density [kg m -3 ]

	:Configuration:
		.. csv-table::
			:file: snowDensMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SnowLimPatch

	:Description:
		Not needed if SnowUse = 0 in RunControl.nml . Example values [mm] 190 Paved Järvi et al. (2014) [15]  190 Bldgs Järvi et al. (2014) [15]  190 BSoil Järvi et al. (2014) [15]  Limit of snow water equivalent when the surface surface is fully covered with snow. Not needed if SnowUse = 0 in RunControl.nml . Example values [mm] 190 EveTr Järvi et al. (2014) [15]  190 DecTr Järvi et al. (2014) [15]  190 Grass Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: SnowLimPatch.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SnowLimRemove

	:Description:
		Not needed if SnowUse = 0 in RunControl.nml . Currently not implemented for BSoil surface Example values [mm] 40 Paved Järvi et al. (2014) [15]  100 Bldgs Järvi et al. (2014) [15] 

	:Configuration:
		.. csv-table::
			:file: SnowLimRemove.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SoilDensity

	:Description:
		Soil density [kg m -3 ]

	:Configuration:
		.. csv-table::
			:file: SoilDensity.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SoilDepth

	:Description:
		Depth of sub-surface soil store [mm] i.e. the depth of soil beneath the surface 

	:Configuration:
		.. csv-table::
			:file: SoilDepth.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SoilStoreCap

	:Description:
		SoilStoreCap must not be greater than SoilDepth.

	:Configuration:
		.. csv-table::
			:file: SoilStoreCap.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SoilTypeCode

	:Description:
		Code for soil characteristics below this surface Provides the link to column 1 of SUEWS_Soil.txt , which contains the attributes describing sub-surface soil for this surface type. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Soil.txt.  Code for soil characteristics below this surface Provides the link to column 1 of SUEWS_Soil.txt , which contains the attributes describing sub-surface soil for this surface type. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Soil.txt. 

	:Configuration:
		.. csv-table::
			:file: SoilTypeCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: StartDLS

	:Description:
		Start of the day light savings [DOY] See section on Day Light Savings . 

	:Configuration:
		.. csv-table::
			:file: StartDLS.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: StateLimit

	:Description:
		Currently only used for the water surface Currently only used for the water surface Surface state cannot exceed this value. Set to a large value (e.g. 20000 mm = 20 m) if the water body is substantial (lake, river, etc) or a small value (e.g. 10 mm) if water bodies are very shallow (e.g. fountains). WaterDepth (column 9) must not exceed this value.

	:Configuration:
		.. csv-table::
			:file: StateLimit.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: StorageMax

	:Description:
		Maximum water storage capacity for upper surfaces (i.e. canopy) Min and max values are to account for seasonal variation (e.g. leaf-on/leaf-off differences for vegetated surfaces). Not currently used for non-vegetated surfaces - set the same as StorageMin. Example values [mm] 0.48 Paved 0.25 Bldgs 0.8 BSoil Maximum water storage capacity for upper surfaces (i.e. canopy) Min/max values are to account for seasonal variation (e.g. leaf-off/leaf-on differences for vegetated surfaces) Only used for DecTr surfaces - set EveTr and Grass values the same as StorageMin. Example values [mm] 1.3 EveTr Breuer et al. (2003) [36]  0.8 DecTr Breuer et al. (2003) [36]  1.9 Grass Breuer et al. (2003) [36]  Maximum water storage capacity for upper surfaces (i.e. canopy) Min and max values are to account for seasonal variation - not used for water surfaces so set same as StorageMin.

	:Configuration:
		.. csv-table::
			:file: StorageMax.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: StorageMin

	:Description:
		Minimum water storage capacity for upper surfaces (i.e. canopy). Min/max values are to account for seasonal variation (e.g. leaf-on/leaf-off differences for vegetated surfaces). Not currently used for non-vegetated surfaces - set the same as StorageMax. Example values [mm] 0.48 Paved 0.25 Bldgs 0.8 BSoil Minimum water storage capacity for upper surfaces (i.e. canopy). Min/max values are to account for seasonal variation (e.g. leaf-off/leaf-on differences for vegetated surfaces). Example values [mm] 1.3 EveTr Breuer et al. (2003) [36]  0.3 DecTr Breuer et al. (2003) [36]  1.9 Grass Breuer et al. (2003) [36]  Minimum water storage capacity for upper surfaces (i.e. canopy). Min/max values are to account for seasonal variation - not used for water surfaces. Example values [mm] 0.5 Water

	:Configuration:
		.. csv-table::
			:file: StorageMin.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: SurfaceArea

	:Description:
		Area of the grid [ha].

	:Configuration:
		.. csv-table::
			:file: SurfaceArea.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_k1

	:Description:
		Thermal conductivity of the first layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_k1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_k2

	:Description:
		Thermal conductivity of the second layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_k2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_k3

	:Description:
		Thermal conductivity of the third layer[W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_k3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_k4

	:Description:
		Thermal conductivity of the fourth layer[W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_k4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_k5

	:Description:
		Thermal conductivity of the fifth layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_k5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_rhoCp1

	:Description:
		Volumetric heat capacity of the first layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_rhoCp1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_rhoCp2

	:Description:
		Volumetric heat capacity of the second layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_rhoCp2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_rhoCp3

	:Description:
		Volumetric heat capacity of the third layer[J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_rhoCp3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_rhoCp4

	:Description:
		Volumetric heat capacity of the fourth layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_rhoCp4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_rhoCp5

	:Description:
		Volumetric heat capacity of the fifth layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Surf_rhoCp5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_thick1

	:Description:
		Thickness of the first layer [m] for roofs (building surfaces) and ground (all other surfaces)

	:Configuration:
		.. csv-table::
			:file: Surf_thick1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_thick2

	:Description:
		Thickness of the second layer [m] (if no second layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Surf_thick2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_thick3

	:Description:
		Thickness of the third layer [m] (if no third layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Surf_thick3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_thick4

	:Description:
		Thickness of the fourth layer [m] (if no fourth layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Surf_thick4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Surf_thick5

	:Description:
		Thickness of the fifth layer [m] (if no fifth layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Surf_thick5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Tair

	:Description:
		Air temperature [°C]

	:Configuration:
		.. csv-table::
			:file: Tair.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: tau_a

	:Description:
		Time constant for snow albedo aging in cold snow [-]

	:Configuration:
		.. csv-table::
			:file: tau_a.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: tau_f

	:Description:
		Time constant for snow albedo aging in melting snow [-]

	:Configuration:
		.. csv-table::
			:file: tau_f.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: tau_r

	:Description:
		Time constant for snow density ageing [-]

	:Configuration:
		.. csv-table::
			:file: tau_r.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: TCritic

	:Description:
		Use with AnthropHeatMethod = 1

	:Configuration:
		.. csv-table::
			:file: TCritic.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: TempMeltFactor

	:Description:
		Hourly temperature melt factor of snow [mm °C -1 h -1 ] (In previous model version, this parameter was 0.12)

	:Configuration:
		.. csv-table::
			:file: TempMeltFactor.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: TH

	:Description:
		Upper air temperature limit [°C]

	:Configuration:
		.. csv-table::
			:file: TH.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Theta+_K

	:Description:
		potential temperature at the top of CBL (K)

	:Configuration:
		.. csv-table::
			:file: Theta+_K.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Theta_K

	:Description:
		potential temperature in CBL (K)

	:Configuration:
		.. csv-table::
			:file: Theta_K.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Tiair

	:Description:
		Indoor air temperature [˚C]

	:Configuration:
		.. csv-table::
			:file: Tiair.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Timezone

	:Description:
		Time zone [h] for site relative to UTC (east is positive). This should be set according to the times given in the meteorological forcing file(s).

	:Configuration:
		.. csv-table::
			:file: Timezone.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: TL

	:Description:
		Lower air temperature limit [°C]

	:Configuration:
		.. csv-table::
			:file: TL.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToBldgs

	:Description:
		Fraction of water going to `Bldgs`

	:Configuration:
		.. csv-table::
			:file: ToBldgs.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToBSoil

	:Description:
		Fraction of water going to `BSoil`

	:Configuration:
		.. csv-table::
			:file: ToBSoil.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToDecTr

	:Description:
		Fraction of water going to `DecTr`

	:Configuration:
		.. csv-table::
			:file: ToDecTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToEveTr

	:Description:
		Fraction of water going to `EveTr`

	:Configuration:
		.. csv-table::
			:file: ToEveTr.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToGrass

	:Description:
		Fraction of water going to `Grass`

	:Configuration:
		.. csv-table::
			:file: ToGrass.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToPaved

	:Description:
		Fraction of water going to `Paved`

	:Configuration:
		.. csv-table::
			:file: ToPaved.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToRunoff

	:Description:
		Fraction of water going to `Runoff`

	:Configuration:
		.. csv-table::
			:file: ToRunoff.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToSoilStore

	:Description:
		Fraction of water going to `SoilStore`

	:Configuration:
		.. csv-table::
			:file: ToSoilStore.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: ToWater

	:Description:
		Fraction of water going to `Water`

	:Configuration:
		.. csv-table::
			:file: ToWater.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: TrafficRate

	:Description:
		Traffic rate [veh km m-2 s-1] Can be used for CO2 flux calculation. Do not use in v2017a - set to -999 

	:Configuration:
		.. csv-table::
			:file: TrafficRate.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Troad

	:Description:
		Ground surface temperature [˚C] (used when TsurfChoice = 1 or 2)

	:Configuration:
		.. csv-table::
			:file: Troad.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Troof

	:Description:
		Roof surface temperature [˚C] (used when TsurfChoice = 1 or 2)

	:Configuration:
		.. csv-table::
			:file: Troof.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Tsurf

	:Description:
		Bulk surface temperature [˚C] (used when TsurfCoice = 0)

	:Configuration:
		.. csv-table::
			:file: Tsurf.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Twall

	:Description:
		Wall surface temperature [˚C] (used when TsurfChoice = 1)

	:Configuration:
		.. csv-table::
			:file: Twall.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Twall_e

	:Description:
		East-facing wall surface temperature [˚C] (used when TsurfChoice = 2)

	:Configuration:
		.. csv-table::
			:file: Twall_e.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Twall_n

	:Description:
		North-facing wall surface temperature [˚C] (used when TsurfChoice = 2)

	:Configuration:
		.. csv-table::
			:file: Twall_n.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Twall_s

	:Description:
		South-facing wall surface temperature [˚C] (used when TsurfChoice = 2)

	:Configuration:
		.. csv-table::
			:file: Twall_s.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Twall_w

	:Description:
		West-facing wall surface temperature [˚C] (used when TsurfChoice = 2)

	:Configuration:
		.. csv-table::
			:file: Twall_w.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: U

	:Description:
		Height of the wind speed measurement (z) is needed in SUEWS_SiteSelect.txt .

	:Configuration:
		.. csv-table::
			:file: U.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_k1

	:Description:
		Thermal conductivity of the first layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_k1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_k2

	:Description:
		Thermal conductivity of the second layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_k2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_k3

	:Description:
		Thermal conductivity of the third layer [W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_k3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_k4

	:Description:
		Thermal conductivity of the fourth layer[W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_k4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_k5

	:Description:
		Thermal conductivity of the fifth layer[W m -1 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_k5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_rhoCp1

	:Description:
		Volumetric heat capacity of the first layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_rhoCp1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_rhoCp2

	:Description:
		Volumetric heat capacity of the second layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_rhoCp2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_rhoCp3

	:Description:
		Volumetric heat capacity of the third layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_rhoCp3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_rhoCp4

	:Description:
		Volumetric heat capacity of the fourth layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_rhoCp4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_rhoCp5

	:Description:
		Volumetric heat capacity of the fifth layer [J m -3 K -1 ]

	:Configuration:
		.. csv-table::
			:file: Wall_rhoCp5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_thick1

	:Description:
		Thickness of the first layer [m] for building surfaces only; set to -999 for all other surfaces

	:Configuration:
		.. csv-table::
			:file: Wall_thick1.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_thick2

	:Description:
		Thickness of the second layer [m] (if no second layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Wall_thick2.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_thick3

	:Description:
		Thickness of the third layer [m] (if no third layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Wall_thick3.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_thick4

	:Description:
		Thickness of the fourth layer [m] (if no fourth layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Wall_thick4.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wall_thick5

	:Description:
		Thickness of the fifth layer [m] (if no fifth layer, set to -999.)

	:Configuration:
		.. csv-table::
			:file: Wall_thick5.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WaterDepth

	:Description:
		Set to a large value (e.g. 20000 mm = 20 m) if the water body is substantial (lake, river, etc) or a small value (e.g. 10 mm) if water bodies are very shallow (e.g. fountains). This value must not exceed StateLimit (column 8).

	:Configuration:
		.. csv-table::
			:file: WaterDepth.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WaterUseProfAutoWD

	:Description:
		Code for water use profile (automatic irrigation, weekdays) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. 

	:Configuration:
		.. csv-table::
			:file: WaterUseProfAutoWD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WaterUseProfAutoWE

	:Description:
		Code for water use profile (automatic irrigation, weekends) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. 

	:Configuration:
		.. csv-table::
			:file: WaterUseProfAutoWE.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WaterUseProfManuWD

	:Description:
		Code for water use profile (manual irrigation, weekdays) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. 

	:Configuration:
		.. csv-table::
			:file: WaterUseProfManuWD.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WaterUseProfManuWE

	:Description:
		Code for water use profile (manual irrigation, weekends) Provides the link to column 1 of SUEWS_Profiles.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_Profiles.txt. 

	:Configuration:
		.. csv-table::
			:file: WaterUseProfManuWE.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: wdir

	:Description:
		Currently not implemented

	:Configuration:
		.. csv-table::
			:file: wdir.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WetThreshold

	:Description:
		Depth of water which determines whether evaporation occurs from a partially wet or completely wet surface. Example values [mm] 0.6 Paved 0.6 Bldgs 1. BSoil Depth of water which determines whether evaporation occurs from a partially wet or completely wet surface. Example values [mm] 1.8 EveTr 1. DecTr 2. Grass Depth of water which determines whether evaporation occurs from a partially wet or completely wet surface. Example values [mm] 0.5 Water

	:Configuration:
		.. csv-table::
			:file: WetThreshold.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridBldgsCode

	:Description:
		Code that links to the fraction of water that flows from Bldgs surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridBldgsCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridBSoilCode

	:Description:
		Code that links to the fraction of water that flows from BSoil surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridBSoilCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridDecTrCode

	:Description:
		Code that links to the fraction of water that flows from DecTr surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridDecTrCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridEveTrCode

	:Description:
		Code that links to the fraction of water that flows from EveTr surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridEveTrCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridGrassCode

	:Description:
		Code that links to the fraction of water that flows from Grass surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridGrassCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridPavedCode

	:Description:
		Code that links to the fraction of water that flows from Paved surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt . Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridPavedCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: WithinGridWaterCode

	:Description:
		Code that links to the fraction of water that flows from Water surfaces to surfaces in columns 2-10 of SUEWS_WithinGridWaterDist.txt. Value of integer is arbitrary but must match code specified in column 1 of SUEWS_WithinGridWaterDist.txt. 

	:Configuration:
		.. csv-table::
			:file: WithinGridWaterCode.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Wuh

	:Description:
		External water use [ 3 ]

	:Configuration:
		.. csv-table::
			:file: Wuh.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: xsmd

	:Description:
		Observed soil moisture [ 3 m -3 or kg kg -1 ]

	:Configuration:
		.. csv-table::
			:file: xsmd.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: Year

	:Description:
		Year [YYYY] Years must be continuous. If running multiple years, ensure the rows in SiteSelect.txt are arranged so that all grids for a particular year appear on consecutive lines (rather than grouping all years together for a particular grid). 

	:Configuration:
		.. csv-table::
			:file: Year.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: z

	:Description:
		z must be greater than the displacement height. Forcing data should be representative of the local-scale, i.e. above the height of the roughness elements.

	:Configuration:
		.. csv-table::
			:file: z.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: z0

	:Description:
		Roughness length for momentum [m] Value supplied here is used if RoughLenMomMethod = 1 in RunControl.nml ; otherwise set to '-999' and a value will be calculated by the model (RoughLenMomMethod = 2, 3). 

	:Configuration:
		.. csv-table::
			:file: z0.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: zd

	:Description:
		Zero-plane displacement [m] Value supplied here is used if RoughLenMomMethod = 1 in RunControl.nml ; otherwise set to '-999' and a value will be calculated by the model (RoughLenMomMethod = 2, 3). 

	:Configuration:
		.. csv-table::
			:file: zd.csv
			:header-rows: 1
			:widths: 10 10 80


.. option:: zi0

	:Description:
		initial convective boundary layer height (m)

	:Configuration:
		.. csv-table::
			:file: zi0.csv
			:header-rows: 1
			:widths: 10 10 80

