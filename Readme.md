                             _      _ _     
                            | |    (_) |    
   ___ _ __ ___   ___  _ __ | |     _| |__  
  / _ \ '_ ` _ \ / _ \| '_ \| |    | | '_ \
 |  __/ | | | | | (_) | | | | |____| | |_) |
  \___|_| |_| |_|\___/|_| |_|______|_|_.__/

Arduino Energy Monitoring Library - For SparkCore
*****************************************************************

This is the emonLib optimized for the SparkCore.
Thanks Glyn Hudson for writing this nice piece of code. If you want more info about this project:
http://openenergymonitor.org/emon/

Forked from https://github.com/openenergymonitor/EmonLib

# EmonLib

## Examples

More info on: https://openenergymonitor.org/emon/buildingblocks/how-to-build-an-arduino-energy-monitor-measuring-current-only

## Referenece

### `EnergyMonitor`

`EnergyMonitor emon;`

Creates an object to interact with the current sensor.
Example: current_only.ino

### `current`

`emon.current(input pin, calibration)`

Connects the current sensor object with the correct pin and sets the calibration value.
This should be called once in `setup`
Example: current_only.ino

### `calcIrms`

`double Irms = emon.calcIrms(number_of_samples)`

Calculate the Irms for a number of samples. The function will read the amount of samples and return a double.
Example: current_only.ino

### `voltage`

`emon.voltage(input pin, calibration, phase_shift)`

Example: voltage_and_current.ino
More info: https://openenergymonitor.org/emon/buildingblocks/ct-and-ac-power-adaptor-installation-and-calibration-theory
