.. _Above_Ground_State:

Above Ground State
~~~~~~~~~~~~~~~~~~

.. option:: PavedState

	:Requirement:
		Optional
	:Description:
		If unknown, model assumes dry surfaces (acceptable as rainfall or irrigation will update these states quickly).
	:Configuration:
		to fill


.. option:: BldgsState

	:Requirement:
		Optional
	:Description:
		If unknown, model assumes dry surfaces (acceptable as rainfall or irrigation will update these states quickly).
	:Configuration:
		to fill


.. option:: EveTrState

	:Requirement:
		Optional
	:Description:
		If unknown, model assumes dry surfaces (acceptable as rainfall or irrigation will update these states quickly).
	:Configuration:
		to fill


.. option:: DecTrState

	:Requirement:
		Optional
	:Description:
		If unknown, model assumes dry surfaces (acceptable as rainfall or irrigation will update these states quickly).
	:Configuration:
		to fill


.. option:: GrassState

	:Requirement:
		Optional
	:Description:
		If unknown, model assumes dry surfaces (acceptable as rainfall or irrigation will update these states quickly).
	:Configuration:
		to fill


.. option:: BSoilState

	:Requirement:
		Optional
	:Description:
		If unknown, model assumes dry surfaces (acceptable as rainfall or irrigation will update these states quickly).
	:Configuration:
		to fill


.. option:: WaterState

	:Requirement:
		Optional
	:Description:
		For a large water body (e.g. river, sea, lake) set WaterState to a large value, e.g. 20000 mm; for small water bodies (e.g. ponds, fountains) set WaterState to smaller value, e.g. 1000 mm. This value must not exceed StateLimit specified in SUEWS_Water.txt . If unknown, model uses value of WaterDepth specified in SUEWS_Water.txt .
	:Configuration:
		to fill
