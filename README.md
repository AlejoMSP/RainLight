# RainLight

Automotive rain light — 10-LED vertical array, KiCad project.

## Overview

10 red LEDs (D1–D10) in a vertical strip, each with its own current-limiting
resistor (R1–R10, 510Ω), powered from a 12V automotive source via a DTM04-2P
2-pin wire-pigtail connector (J1). Sized for a Chanzon 10mm red LED
(Vf ≈ 2.0V @ 20mA) running off battery/alternator voltage.

## Status

- **Schematic**: Rev 1.2, complete. See comments in the title block for revision
  history (LED polarity fix, per-LED resistor conversion, connector addition).
- **PCB**: in progress — footprint placement and routing underway.

## Key specs

| Item | Value |
|---|---|
| LEDs | D1–D10, red, THT 10mm (`LED_THT:LED_D10.0mm`) — Chanzon 10mm red, Vf ≈ 2.0V @ 20mA |
| Resistors | R1–R10, 510Ω, THT axial (`Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P7.62mm_Horizontal`) |
| Row spacing | ~16.4mm |
| Power input | J1, DTM04-2P wire pigtail, 2 pads (`Connector_Wire:SolderWire-0.75sqmm_1x02_P4.8mm_D1.25mm_OD2.3mm`) |
| Supply | 12V automotive |
| Per-LED current | ~19.6mA @ 12V nominal (R = (12V − 2V) / 20mA ≈ 500Ω, rounded to 510Ω) |

## Files

- `RainLight.kicad_pro` — project file
- `RainLight.kicad_sch` — schematic
- `RainLight.kicad_pcb` — PCB layout

`RainLight.kicad_prl` (local project settings) is gitignored — it's per-machine
session state, not meaningful to version.
