
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


The parameters and their setting instructions are provided in the tables below:

* :numref:`{number} Model run options <Model_run_options>`
* :numref:`{number} Time related options <Time_related_options>`
* :numref:`{number} File related options <File_related_options>`
* :numref:`{number} Options related to disaggregation of input data <Options_related_to_disaggregation_of_input_data>`
* :numref:`{number} netCDF related options <netCDF_related_options>`

.. _Model_run_options:
.. csv-table:: Model_run_options
  :widths: 5 5 100 30
  :header-rows: 1
  :file: Model_run_options.csv


.. _Time_related_options:
.. csv-table:: Time_related_options
  :header-rows: 1
  :file: Time_related_options.csv


.. _File_related_options:
.. csv-table:: File_related_options
  :header-rows: 1
  :file: File_related_options.csv


.. _Options_related_to_disaggregation_of_input_data :
.. csv-table:: Options_related_to_disaggregation_of_input_data
  :header-rows: 1
  :file: Options_related_to_disaggregation_of_input_data.csv


.. _netCDF_related_options:
.. csv-table:: netCDF_related_options
  :header-rows: 1
  :file: netCDF_related_options.csv


