# Bhoomi Shiv (EDP) — KiCad PCB

A fully validated 2-layer KiCad 10 PCB design for the **Bhoomi Shiv** agricultural IoT device,
part of the **MEOSA EDP** project.

## Board Specifications
- **Dimensions**: 110 mm × 100 mm, 2-layer
- **MCU**: ESP32-S3 DevKitC-1 N16R8 (mounted via dual 1×22 female pin sockets)
- **Power**: 1S2P Li-ion battery → TP4056 charger → MT3608 5V boost → 1N5819 Schottky protection
- **Peripherals**:
  - Soil Moisture Sensor (JST-XH 3-pin)
  - DS18B20 Waterproof Temperature Probe (JST-XH 3-pin, 1-Wire with 4.7k pull-up)
  - SSD1306 0.96" I2C OLED Display (JST-XH 4-pin)
  - AS7265x Triad Spectral Sensor (JST-XH 4-pin, shared I2C bus)
  - Piezo Buzzer with 2N2222 NPN driver & 1N4148 flyback diode (JST-XH 2-pin)
  - User tactile test button with hardware debounce (10k PU, 1k series, 100nF filter)
- **External Charge Input**: JST-XH 2-pin 5V USB input → TP4056

## Verification Status
| Check | Result |
|---|---|
| ERC (Electrical Rules Check) | ✅ 0 Errors |
| DRC (Design Rules Check) | ✅ 0 Violations |
| Unconnected Items | ✅ 0 |
| Ground Plane (B.Cu) | ✅ Continuous solid GND pour |

## Project Files
| File | Description |
|---|---|
| `Bhoomi_shiv(edp).kicad_pro` | KiCad 10 Project |
| `Bhoomi_shiv(edp).kicad_sch` | Full Schematic |
| `Bhoomi_shiv(edp).kicad_pcb` | PCB Layout |
| `BOM_Bhoomi_shiv.csv` | Bill of Materials |
| `drc_report.rpt` | DRC Verification Report |
| `erc_report.rpt` | ERC Verification Report |
| `render_top.png` | 3D Top View |
| `render_bot.png` | 3D Bottom View |
| `gerbers/` | Gerber + Excellon drill files for fabrication |

## Manufacturing
Send the `gerbers/` folder to JLCPCB / PCBWay / any fab house.
- **Layers**: 2
- **Board size**: 110 × 100 mm
- **Min trace/space**: 0.25 mm / 0.25 mm
- **Drill**: Excellon format, included in `gerbers/`
- **Surface finish**: HASL or ENIG recommended
