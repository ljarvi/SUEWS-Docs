.. _File_related_options:

File related options
~~~~~~~~~~~~~~~~~~~~

.. option:: FileCode

	:Requirement:
		Required

	:Description:
		Two-letter site identification code (e.g. He, Sc, Kc).
	:Configuration:
		to fill


.. option:: FileInputPath

	:Requirement:
		Required

	:Description:
		Input directory.
	:Configuration:
		to fill


.. option:: FileOutputPath

	:Requirement:
		Required

	:Description:
		Output directory.
	:Configuration:
		to fill


.. option:: MultipleMetFiles

	:Requirement:
		Required
	:Description:
		Specifies whether one single meteorological forcing file is used for all grids or a separate met file is provided for each grid.
	:Configuration:
		.. csv-table::
			:file: MultipleMetFiles.csv
			:header-rows: 1
			:widths: auto


.. option:: MultipleInitFiles

	:Requirement:
		Required
	:Description:
		Specifies whether one single initial conditions file is used for all grids at the start of the run or a separate initial conditions file is provided for each grid.
	:Configuration:
		.. csv-table::
			:file: MultipleInitFiles.csv
			:header-rows: 1
			:widths: auto


.. option:: MultipleESTMFiles

	:Requirement:
		Optional
	:Description:
		Specifies whether one single ESTM forcing file is used for all grids or a separate file is provided for each grid.
	:Configuration:
		.. csv-table::
			:file: MultipleESTMFiles.csv
			:header-rows: 1
			:widths: auto


.. option:: KeepTstepFilesIn

	:Requirement:
		Optional
	:Description:
		Specifies whether input meteorological forcing files at the resolution of the model time step should be saved.
	:Configuration:
		.. csv-table::
			:file: KeepTstepFilesIn.csv
			:header-rows: 1
			:widths: auto


.. option:: KeepTstepFilesOut

	:Requirement:
		Optional
	:Description:
		Specifies whether output meteorological forcing files at the resolution of the model time step should be saved.
	:Configuration:
		.. csv-table::
			:file: KeepTstepFilesOut.csv
			:header-rows: 1
			:widths: auto


.. option:: WriteOutOption

	:Requirement:
		Optional
	:Description:
		Specifies which variables are written in the output files.
	:Configuration:
		.. csv-table::
			:file: WriteOutOption.csv
			:header-rows: 1
			:widths: auto


.. option:: SuppressWarnings

	:Requirement:
		Optional
	:Description:
		Controls whether the warnings.txt file is written or not.
	:Configuration:
		.. csv-table::
			:file: SuppressWarnings.csv
			:header-rows: 1
			:widths: auto
