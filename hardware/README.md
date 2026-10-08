# Hardware notes

The schematic uses a 3.7 V LiPo cell, a K548 USB-C charger, and a K585 boost converter set to 5 V. The 5 V rail supplies the ESP32-S3 Zero and pump; sensors use the ESP32's 3.3 V rail.

## Schematic scope

The [schematic](plant_watering_controller.kicad_sch) contains the module connections for soil moisture, BH1750 light sensing, SHT31 temperature and humidity sensing, and an XSL-4510-P float switch. Check the instantiated ESP32 symbol and the exact board pin labels before wiring. Battery-voltage measurement is not drawn in this revision.

An IRLB3034 switches the pump on the low side. A 1N5819 diode is drawn across the motor, and the gate has a 100 ohm series resistor and 10 kohm pulldown.

## Recorded checks

The [saved ERC report](plant_watering_controller_erc.rpt), dated 19 June 2026, records 0 errors and 0 warnings. Four check types were disabled:

- Global label only appears once in the schematic
- Four connection points are joined together
- SPICE model issue
- Assigned footprint doesn't match footprint filters

This is a saved schematic check, not evidence of operation on hardware. No bench-test results are included.
