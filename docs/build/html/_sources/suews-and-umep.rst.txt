SUEWS and UMEP
==============


SUEWS can be run as a standalone model but also can be used within
`UMEP <http://urban-climate.net/umep/UMEP_Manual>`__. There are numerous
tools included within UMEP to help a user get started. The `SUEWS
simple <http://urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_Urban_Energy_Balance_.28SUEWS.2C_simple.29>`__
within UMEP is a fast way to start using SUEWS.

The version of SUEWS within UMEP is the complete model. Thus all options
that are listed in this manual are available to the user. In the UMEP
`SUEWS
simple <http://urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_Urban_Energy_Balance_.28SUEWS.2C_simple.29>`__
runs all options are set to values to allow intial exploration of the
model behaviour.

The version of SUEWS within UMEP is a more recent release of the model
than the independent SUEWS release.

.. list-table::
	:widths: 5 5 10 70
	:header-rows: 1
	:stub-columns: 2

	* - 
	  - UMEP
	  - 
	  - Description

	* - Pre-Processor 
	  - Meteorological Data
	  - `Prepare Existing Data`_ 
	  - Transforms meteorological data into UMEP format

	* - 
	  - 
	  - `Download data (WATCH)`_ 
	  - Prepare meteorological dataset from `WATCH` 

	* - 
	  - Spatial Data
	  - `Spatial Data Downloader`_ 
	  - Plugin for retrieving geodata from online services suitable for various UMEP related tools

	* - 
	  - 
	  - `LCZ Converter`_ 
	  - Conversion from Local Climate Zones (LCZs) in the WUDAPT database into SUEWS input data

	* - 
	  - Urban land cover
	  - `Land Cover Reclassifier`_
	  - Reclassifies a grid into UMEP format land cover grid. Land surface models 

	* - 
	  - 
	  - `Land Cover Fraction (Point)`_ 
	  - Land cover fractions estimates from a land cover grid based on a specific point in space

	* - 
	  - 
	  - `Land Cover Fraction (Grid)`_ 
	  - Land cover fractions estimates from a land cover grid based on a polygon grid

	* - 
	  - Urban Morphology
	  - `Morphometric Calculator (Point)`_ 
	  - Morphometric parameters from a DSM based on a specific point in space

	* - 
	  - 
	  - `Morphometric Calculator (Grid)`_ 
	  - Morphometric parameters estimated from a DSM based on a polygon grid

	* - 
	  - 
	  - `Source Area Model (Point)`_ 
	  - Source area calculated from a DSM based on a specific point in space.

	* - 
	  - SUEWS input data
	  - `SUEWS Prepare`_ 
	  - Preprocessing and preparing input data for the SUEWS model

	* - Processor 
	  - Anthropogenic Heat (|QF|)
	  - `LQF`_
	  - Spatial variations anthropogenic heat release for urban areas

	* - 
	  - 
	  - `GQF`_ 
	  - Anthropogenic Heat (|QF|).

	* - 
	  - Urban Energy Balance
	  - `SUEWS (Simple)`_ 
	  - Urban Energy and Water Balance.

	* - 
	  - 
	  - `SUEWS (Advanced)`_ 
	  - Urban Energy and Water Balance.

	* - Post-Processor 
	  - Urban Energy Balance
	  - `SUEWS analyser`_ 
	  - Plugin for plotting and statistical analysis of model results from SUEWS simple and SUEWS advanced

	* - 
	  - Benchmark
	  - `Benchmark System`_ 
	  - For statistical analysis of model results, such as SUEWS

.. _Prepare Existing Data: http://urban-climate.net/umep/UMEP_Manual#Meteorological_Data:_MetPreprocessor

.. _Download data (WATCH): http://www.urban-climate.net/umep/UMEP_Manual#Meteorological_Data:_Download_data_.28WATCH.29

.. _Spatial Data Downloader: http://www.urban-climate.net/umep/UMEP_Manual#Spatial_Data:_Spatial_Data_Downloader

.. _LCZ Converter: http://www.urban-climate.net/umep/UMEP_Manual#Spatial_Data:_LCZ_Converter

.. _Land Cover Reclassifier: http://urban-climate.net/umep/UMEP_Manual#Urban_Land_Cover:_Land_Cover_Reclassifier

.. _Land Cover Fraction (Point): http://urban-climate.net/umep/UMEP_Manual#Urban_Land_Cover:_Land_Cover_Reclassifier
 
.. _Land Cover Fraction (Grid): http://urban-climate.net/umep/UMEP_Manual#Urban_Land_Cover:_Land_Cover_Fraction_.28Grid.29

.. _Morphometric Calculator (Point): http://urban-climate.net/umep/UMEP_Manual#Urban_Morphology:_Morphometric_Calculator_.28Point.29

.. _Morphometric Calculator (Grid): http://urban-climate.net/umep/UMEP_Manual#Urban_Morphology:_Morphometric_Calculator_.28Grid.29

.. _Source Area Model (Point): http://urban-climate.net/umep/UMEP_Manual#Urban_Morphology:_Source_Area_.28Point.29

.. _SUEWS Prepare: http://urban-climate.net/umep/UMEP_Manual#Pre-Processor:_SUEWS_Prepare

.. _LQF: http://www.urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_LQF

.. _GQF: http://www.urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_GQF

.. _SUEWS (Simple): http://urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_Urban_Energy_Balance_.28SUEWS.2C_simple.29

.. _SUEWS (Advanced): http://urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_Urban_Energy_Balance_.28SUEWS.2FBLUEWS.2C_advanced.29

.. _SUEWS analyser: http://urban-climate.net/umep/UMEP_Manual#Urban_Energy_Balance:_SUEWS_Analyser

.. _Benchmark System: http://urban-climate.net/umep/UMEP_Manual#Benchmark_System

