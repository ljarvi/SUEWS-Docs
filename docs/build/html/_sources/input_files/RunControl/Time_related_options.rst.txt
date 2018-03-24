.. _Time_related_options:

Time related options
~~~~~~~~~~~~~~~~~~~~

.. option:: Tstep

	:Requirement:
		Required

	:Description:
		Specifies the model time step [s]. A value of 300 s (5 min) is strongly recommended. The time step cannot be less than 1 min or greater than 10 min, and must be a whole number of minutes that divide into an hour (i.e. options are 1, 2, 3, 4, 5, 6, 10 min or 60, 120, 180, 240, 300, 360, 600 s).
	:Configuration:
		to fill


.. option:: ResolutionFilesIn

	:Requirement:
		Required

	:Description:
		Specifies the resolution of the input files [s] which SUEWS will disaggregate to the model time step. 1800 s for 30 min or 3600 s for 60 min are recommended. (N.B. if ResolutionFilesIn is not provided, SUEWS assumes ResolutionFilesIn = Tstep.)
	:Configuration:
		to fill


.. option:: ResolutionFilesInESTM

	:Requirement:
		Optional

	:Description:
		Specifies the resolution of the ESTM input files [s] which SUEWS will disaggregate to the model time step.
	:Configuration:
		to fill


.. option:: ResolutionFilesOut

	:Requirement:
		Required

	:Description:
		Specifies the resolution of the output files [s]. 1800 s for 30 min or 3600 s for 60 min are recommended.
	:Configuration:
		to fill
