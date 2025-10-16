# Project DSX

A custom dual-system handheld that combines original Nintendo DS Lite hardware with a modern computer mode.

## Goals
- Capture DS Lite top-screen RGB signal video and output to an OLED via FPGA.
- Utilize original bottom resistive touch screen to retain original touch “feel”.
  - Use as mouse for emulation mode? Tap into analog X/Y signals from original hardware and convert into USB HID (would need a touch controller).
  - Maybe include a screen on the bottom as well so it is clear exactly where you are clicking? Or just use it as a trackpad?
  - Perhaps it can have different modes, such as a telemetry/stats mode.
- Provide a second "PC/emulation" mode.
  - Use Raspberry Pi or Mini PC for initial testing of switching.
  - Switch to a custom board with an open SoC later.
- Physically switch between modes.
  - Maybe make it a software choice in the future (similar to Nvidia dGPU/iGPU switching)? Doing that on the DS side might require custom firmware.
- Custom power system: USB-C PD charging + Li-ion battery with safe switching.
- Compact, ergonomic enclosure and user interface.

## Architecture
1. **DS Mode** — DS Lite board runs natively; FPGA samples top-screen RGB + sync and repackages to the OLED. Thumbstick input is translated into four discrete directions (eight when diagonals are detected).
2. **Computer Mode** — SBC boots Linux/Windows and drives the OLED directly. Controls are routed via microcontroller (USB HID). Original DS resistive touch panel is routed as a mouse.
3. **Power** — Li-ion with USB-C PD charge controller. MOSFET switching isolates the inactive system.
![alt text](([https://github.com/canersaka/projectdsx/blob/main/hardware/schematics/Second%20Schematic%20Draft.png]))
## Status
**10/15/25 Week 1:** Planning and parts research. Focus: DS signal capture and FPGA pipeline.

## Parts
- DS Lite donor (motherboard + bottom LCD/touch) — donor unit
- Top OLED 5.5" (HDMI driver board)
- FPGA dev board (TBD)
- Logic analyzer (to help convert DS Lite signals to a modern display)
- Raspberry Pi 5 (for initial testing)
- USB-C PD module + voltage regulator, 2×21700 cells (?), MOSFET for switching
- RP2040 (?), for buttons, switches, power telemetry
- Small speakers, fan, buttons, 3D print for shell
  - Maybe use original speakers and buttons?
- Add analog thumbsticks (from 3DS?)
  - Would require translation to function directly with DS hardware as the original never included analog thumbstick support.
