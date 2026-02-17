# Changelog

All notable changes to the **DermScope REVIVE** carrier PCB design will be documented in this file.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) conventions.  
Version numbers follow `MAJOR.MINOR.PATCH` — hardware revisions use `V1`, `V2`, etc.

---

## [V2] — 2026-02-17 — Current Release

> Production-ready carrier PCB for INVENSOM-6UL SOM. Impedance-controlled 4-layer design with full DermScope REVIVE peripheral set.

### ✅ Added
- **MIPI CSI 4-Lane** camera interface for high-resolution skin imaging sensor
- **MIPI DSI 4-Lane** display interface routed to MIPI DSI → HDMI/LVDS converter
- **HDMI 1.4** output connector for external display support
- **LVDS** display connector as secondary display output
- **USB HUB** IC providing 4× USB 2.0 Type-A host ports (2× dual connectors)
- **OTG Micro USB** connector for device/host dual-role operation
- **TP4056 Li-Ion charge module** for single-cell battery management
- **Over & Reverse Voltage Protection** circuit on power input rails
- **Buck-up battery** rail for RTC and backup power retention
- **MCP3208-B** 8-channel 12-bit SPI ADC (eCSPI2) with J1103 and ADC_Conn outputs
- **GPIO Lens Interface** (J1100) via GPIO_EXP 1–7 for polarization filter switching
- **GPIO EXT CON** via GPIO_EXP 2–6 for external optics/LED control
- **UART3 → J1101** and **I2C4 → J1102** expansion connectors
- **Selection Header** for UART2/UART4 debug via USB TTL
- **Boot Mode** and **Boot Config** jumper headers
- **SD Card** connector via SDIO2
- Impedance control implemented for all high-speed signal layers
- ENIG (Immersion Gold) surface finish applied across full board
- Via tenting applied to all non-functional vias
- 4-layer PCB stack-up with controlled dielectric core (1.27 mm prepreg)
- 2×2 panel configuration with 5 mm breakaway edge strips

### ⚙️ PCB Specifications (V2)
- Board size: 90 × 62 mm
- Layer count: 4
- Material: FR4, 1.6 ±0.16 mm
- Min trace/space: 4 mil / 4 mil
- Surface finish: ENIG
- Solder mask: Green (Top & Bottom)
- Silkscreen: White (Top & Bottom)

---

## [V1] — 2025 — Initial Prototype

> First prototype carrier board for INVENSOM-6UL. Basic peripheral validation and power system proof of concept.

### ✅ Added
- Initial carrier board layout for INVENSOM-6UL SOM footprint
- Basic power supply circuit (+5V, VBAT rails)
- Micro USB charging input
- UART debug interface
- Preliminary display connector routing
- Basic GPIO breakout headers

### ⚠️ Known Issues (resolved in V2)
- Impedance control not implemented on V1
- MIPI CSI/DSI routing not optimized for signal integrity
- USB HUB not present — only single USB OTG port
- No ADC expansion circuit
- GPIO lens interface not implemented
- No over/reverse voltage protection circuit

---

## Roadmap

| Version | Target | Description |
|---------|--------|-------------|
| V2 | ✅ Done | Full peripheral set, impedance-controlled, production-ready |
| V2.1 | 🔄 Planned | Polarization LED driver integration, minor BOM optimization |
| V3 | 🔮 Future | Upgraded camera pipeline, higher resolution display interface, form-factor reduction |

---

*Maintained by the DermScope REVIVE design team for [Revive Medical Technology](https://rmt-usa.com/)*
