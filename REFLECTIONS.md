# Reflections

## Stage 0
I would check the Open-Meteo Air Quality API documentation and make a test request for historical CO2 data before choosing a data source.

## Stage 1
I predicted CO2 would rise as the Northern Hemisphere moved from summer into autumn, when plant growth generally removes less CO2 from the air.

## Stage 2
No. This API returned a complete series, but other sources can miss days; gap detection makes those missing dates visible instead of hiding them.

## Stage 3
A rolling mean helps smooth short spikes in either city. Exponential smoothing gives more weight to new readings, so it responds faster when values change.

## Stage 4
If every API retry fails, the fetch script raises an error before writing new data. The workflow stops, leaving the previously committed data files unchanged.

## Stage 5
I would trust the projection for about three days. The recent readings vary sharply, and a straight-line trend from one seasonal window may not continue.

## Stage 6
I kept both Le Mans and Paris and compare their trends. The analysis functions use dates and numeric values, not city names or coordinates, so they work for both.
