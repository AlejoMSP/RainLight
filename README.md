# RainLight

Automotive rain light — 10-LED vertical array, KiCad project.

## Overview

10 red/amber LEDs (D1–D10) in a vertical strip, each with its own current-limiting
resistor (R1–R10, 1.2kΩ), powered from a 12V automotive source via a DTM04-2P
2-pin wire-pigtail connector (J1). Designed to run off battery/alternator voltage
(9–14.4V) at ~10mA per LED.

## Status

- **Schematic**: Rev 1.2, complete. See comments in the title block for revision
  history (LED polarity fix, per-LED resistor conversion, connector addition).
- **PCB**: in progress — footprint placement and routing underway.

## Key specs

| Item | Value |
|---|---|
| LEDs | D1–D10, red/amber, THT 5mm (`LED_THT:LED_D5.0mm`) |
| Resistors | R1–R10, 1.2kΩ, 1206 SMD (`Resistor_SMD:R_1206_3216Metric`) |
| Row spacing | 12.7mm (0.5") |
| Power input | J1, DTM04-2P wire pigtail, 2 pads (`Connector_Wire:SolderWire-0.75sqmm_1x02_P4.8mm_D1.25mm_OD2.3mm`) |
| Supply | 12V automotive (9–14.4V operating range) |
| Per-LED current | ~10mA @ 13.8V nominal |

## Files

- `RainLight.kicad_pro` — project file
- `RainLight.kicad_sch` — schematic
- `RainLight.kicad_pcb` — PCB layout

`RainLight.kicad_prl` (local project settings) is gitignored — it's per-machine
session state, not meaningful to version.
