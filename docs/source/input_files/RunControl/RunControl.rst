.. _RunControl:
.. _RunControl.nml:

RunControl.nml
--------------

The file **RunControl.nml** is a namelist that specifies the options for
the model run. It must be located in the same directory as the
executable file.

A sample file of **RunControl.nml** looks like

.. literalinclude:: RunControl.nml


.. note::
     - In *Linux* and *Mac*, please add an empty line after the end slash.
     - The file is not case-sensitive.
     - The parameters and variables can appear in any order.


The parameters and their setting instructions are provided through the links below:


* :ref:`Model_run_options`

      .. hlist::
        + :option:`CBLuse`
        + :option:`SnowUse`
        + :option:`SOLWEIGUse`
        + :option:`NetRadiationMethod`
        + :option:`EmissionMethod`
        + :option:`StorageHeatMethod`
        + :option:`OHMIncQF`
        + :option:`StabilityMethod`
        + :option:`RoughLenHeatMethod`
        + :option:`RoughLenMomMethod`
        + :option:`SMDMethod`
        + :option:`WaterUseMethod`


* :ref:`File_related_options`

      .. hlist::
        + :option:`FileCode`
        + :option:`FileInputPath`
        + :option:`FileOutputPath`
        + :option:`MultipleMetFiles`
        + :option:`MultipleInitFiles`
        + :option:`MultipleESTMFiles`
        + :option:`KeepTstepFilesIn`
        + :option:`KeepTstepFilesOut`
        + :option:`WriteOutOption`
        + :option:`SuppressWarnings`


* :ref:`Time_related_options`

      .. hlist::
        + :option:`Tstep`
        + :option:`ResolutionFilesIn`
        + :option:`ResolutionFilesInESTM`
        + :option:`ResolutionFilesOut`


* :ref:`Options_related_to_disaggregation_of_input_data`

      .. hlist::
        + :option:`DisaggMethod`
        + :option:`KdownZen`
        + :option:`RainDisaggMethod`
        + :option:`RainAmongN`
        + :option:`MultRainAmongN`
        + :option:`MultRainAmongNUpperI`
        + :option:`DisaggMethodESTM`

* :ref:`netCDF_related_options`

      .. hlist::
        + :option:`ncMode`
        + :option:`nRow`
        + :option:`nCol`






.. toctree::
   :maxdepth: 1
   :hidden:

   Model_run_options
   Time_related_options
   File_related_options
   Options_related_to_disaggregation_of_input_data
   netCDF_related_options
