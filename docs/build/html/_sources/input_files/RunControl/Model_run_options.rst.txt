.. _Model_run_options:

Model run options
~~~~~~~~~~~~~~~~~

.. option:: CBLuse

	:Requirement:
		Required
	:Description:
		Determines whether a CBL slab model is used to calculate temperature and humidity.
	:Configuration:
		.. csv-table::
			:file: CBLuse.csv
			:header-rows: 1
			:widths: auto


.. option:: SnowUse

	:Requirement:
		Required
	:Description:
		Determines whether the snow part of the model runs.
	:Configuration:
		.. csv-table::
			:file: SnowUse.csv
			:header-rows: 1
			:widths: auto


.. option:: SOLWEIGUse

	:Requirement:
		Required
	:Description:
		Determines whether a high resolution radiation model to calculate mean radiant temperate should be used (SOLWEIG). NOTE: this option will considerably slow down the model since SOLWEIG is a 2D model.
	:Configuration:
		.. csv-table::
			:file: SOLWEIGUse.csv
			:header-rows: 1
			:widths: auto


.. option:: NetRadiationMethod

	:Requirement:
		Required
	:Description:
		Determines method for calculation of radiation fluxes.
	:Configuration:
		.. csv-table::
			:file: NetRadiationMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: AnthropHeatMethod

	:Requirement:
		Required
	:Description:
		Determines method for QF calculation.
	:Configuration:
		.. csv-table::
			:file: AnthropHeatMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: AnthropCO2Method

	:Requirement:
		Required
	:Description:
		Determines method for CO2 calculation.
	:Configuration:
		.. csv-table::
			:file: AnthropCO2Method.csv
			:header-rows: 1
			:widths: auto


.. option:: StorageHeatMethod

	:Requirement:
		Required
	:Description:
		Determines method for calculating storage heat flux ΔQS.
	:Configuration:
		.. csv-table::
			:file: StorageHeatMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: OHMIncQF

	:Requirement:
		Required
	:Description:
		Determines whether the storage heat flux calculation uses Q* or (Q*+QF).
	:Configuration:
		.. csv-table::
			:file: OHMIncQF.csv
			:header-rows: 1
			:widths: auto


.. option:: StabilityMethod

	:Requirement:
		Required
	:Description:
		Defines which atmospheric stability functions are used.
	:Configuration:
		.. csv-table::
			:file: StabilityMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: RoughLenHeatMethod

	:Requirement:
		Required
	:Description:
		Determines method for calculating roughness length for heat.
	:Configuration:
		.. csv-table::
			:file: RoughLenHeatMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: RoughLenMomMethod

	:Requirement:
		Required
	:Description:
		Determines how aerodynamic roughness length (z0m) and zero displacement height (zdm) are calculated.
	:Configuration:
		.. csv-table::
			:file: RoughLenMomMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: SMDMethod

	:Requirement:
		Required
	:Description:
		Determines method for calculating soil moisture deficit (SMD).
	:Configuration:
		.. csv-table::
			:file: SMDMethod.csv
			:header-rows: 1
			:widths: auto


.. option:: WaterUseMethod

	:Requirement:
		Required
	:Description:
		Defines how external water use is calculated.
	:Configuration:
		.. csv-table::
			:file: WaterUseMethod.csv
			:header-rows: 1
			:widths: auto
