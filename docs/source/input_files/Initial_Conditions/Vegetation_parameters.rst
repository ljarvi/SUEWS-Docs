.. _Vegetation_parameters:

Vegetation parameters
~~~~~~~~~~~~~~~~~~~~~

.. option:: LeavesOutIntially

	:Requirement:
		Optional
	:Description:
		If the model run starts in winter when trees are bare, set LeavesOutIntially = 0 and the vegetation parameters will be set accordingly based on the values set in SUEWS_SiteInfo.xlsm. If the model run starts in summer when leaves are fully out, set LeavesOutIntially = 1 and the vegetation parameters will be set accordingly based on the values set in SUEWS_SiteInfo.xlsm. Not LeavesOutInitially can only be set to 0, 1 or -999 (fractional values cannot be used to indicate partial leaf-out). The value of LeavesOutInitially overrides any values provided for the individual vegetation parameters. To prevent LeavesOutInitially from setting the initial conditions, either omit it from the namelist or set to -999. If values are provided individually, they should be consistent the information provided in SUEWS_Veg.txt and the time of year. If values are provided individually, values for all required surfaces must be provided (i.e. specifying only albGrass0 but not albDecTr0 nor albEveTr0 is not permitted).
	:Configuration:
		to fill


.. option:: GDD_1_0

	:Requirement:
		Optional
	:Description:
		Cannot be negative. If leaves are already full, then this should be the same as GDDFull in SUEWS_Veg.txt. If winter , set to 0. It is important that the vegetation characteristics are set correctly (i.e. for the start of the run in summer/winter).
	:Configuration:
		to fill


.. option:: GDD_2_0

	:Requirement:
		Optional
	:Description:
		Cannot be positive If the leaves are full but in early/mid summer then set to 0. If late summer or autumn , this should be a negative value. If leaves are off , then use the values of SDDFull in SUEWS_Veg.txt to guide your minimum value. It is important that the vegetation characteristics are set correctly (i.e. for the start of the run in summer/winter).
	:Configuration:
		to fill


.. option:: LAIinitialEveTr

	:Requirement:
		Optional
	:Description:
		Initial LAI for evergreen trees. The recommended values can be found from SUEWS_Veg.txt 
	:Configuration:
		to fill


.. option:: LAIinitialDecTr

	:Requirement:
		Optional
	:Description:
		Initial LAI for deciduous trees. The recommended values can be found from SUEWS_Veg.txt 
	:Configuration:
		to fill


.. option:: LAIinitialGrass

	:Requirement:
		Optional
	:Description:
		Initial LAI for irrigated grass. The recommended values can be found from SUEWS_Veg.txt 
	:Configuration:
		to fill


.. option:: albEveTr0

	:Requirement:
		Optional
	:Description:
		Albedo of evergreen surface on day 0 of run
	:Configuration:
		to fill


.. option:: albDecTr0

	:Requirement:
		Optional
	:Description:
		Albedo of deciduous surface on day 0 of run
	:Configuration:
		to fill


.. option:: albGrass0

	:Requirement:
		Optional
	:Description:
		Albedo of grass surface on day 0 of run
	:Configuration:
		to fill


.. option:: decidCap0

	:Requirement:
		Optional
	:Description:
		Deciduous storage capacity on day 0 of run.
	:Configuration:
		to fill


.. option:: porosity0

	:Requirement:
		Optional
	:Description:
		Porosity of deciduous vegetation on day 0 of run. This varies between 0.2 (leaf-on) and 0.6 (leaf-off).
	:Configuration:
		to fill
