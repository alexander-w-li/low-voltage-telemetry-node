# Low Voltage Telemetry Node

## Overview
This project implements a low-voltage power monitoring system using an ESP32 and INA219 current sensor. The system measures voltage, current, and power of a test load in real time.

## Features
- Real-time voltage measurement
- Real-time current measurement
- Power calculation (mW)
- I2C communication between ESP32 and INA219

## Hardware
- ESP32
- INA219 current sensor
- LED + 220Ω resistor (test load)
- Breadboard and jumper wires

## Wiring
- ESP32 3V3 → INA219 VCC and VIN+
- ESP32 GND → INA219 GND
- ESP32 D21 → INA219 SDA
- ESP32 D22 → INA219 SCL
- INA219 VIN- → LED (positive)
- LED → resistor → GND

## Example Output
Voltage: ~3.3V  
Current: ~5–6 mA  
Power: ~20 mW  

## Challenges
- Intermittent readings due to a poor VIN- solder joint, fixed via reflow
- Breadboard row misalignment causing open circuit, fixed by verifying node-by-node

## Notes
This project was used to validate low-voltage current sensing and basic telemetry functionality using a controlled load.
