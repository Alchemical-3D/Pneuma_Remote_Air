<div align="center">

# 🌬️ Pneuma Part Cooling

[![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)](#)
[![Cooling](https://img.shields.io/badge/Cooling-Compressed%20Air-blue)](#)
[![Ecosystem](https://img.shields.io/badge/Ecosystem-Alchemical--3D-purple)](#)
[![Ecosystem](https://img.shields.io/badge/Ecosystem-A3DP-orange)](#)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE.md)

> [!NOTE]
> **Dual-Pump Architecture**
> Pneuma has recently been upgraded to a dual-pump system (removing the previous direct-acting solenoid valve). This allows for independent, granular control over ambient room air and warm internal chamber air.

A professional, high-performance pneumatic part cooling system designed for the Alchemical-3D ecosystem. Pneuma utilizes vacuum pump(s) and tubes to deliver highly precise, compressed air cooling to toolheads such as the Alembic.

<p align="center">
  <img src="Images/Assembly/Pneuma_Complete_Ext.png" width="45%" alt="Pneuma Image 1" />
  &nbsp;
  <img src="Images/Assembly/Pneuma_Complete_Table.png" width="45%" alt="Pneuma Image 2" />
</p>

</div>

<br>

## 📚 Documentation Index

Everything you need to set up and configure the Pneuma system:

| Category | Description |
| :--- | :--- |
| 📋 **[Bill of Materials (BOM)](BOM.md)** | The comprehensive checklist of printed parts, pumps, tubing, and hardware needed. |
| 🛠️ **[Assembly Guide](Assembly_Guide.md)** | A step-by-step mastercloth for putting the Pneuma system together. |
| ⚙️ **[Print Settings](Print_Settings.md)** | Essential slicer configurations, material recommendations, and orientation rules for the enclosures. |

<br>

---
> [!IMPORTANT]
> **Alpha Release**
> This project is currently in the **Alpha phase** of development. Please expect ongoing changes, updates, and improvements to the designs and documentation as the system evolves.

> [!TIP]
> **Looking for a Compatible Toolhead?**<br>
> *If you're interested in this project, check out the **[Alembic Toolhead](https://github.com/Alchemical-3D/Alembic_Toolhead)** project! It is a lightweight, high-performance toolhead designed for the Alchemical-3D ecosystem to utilize Pneuma's remote compressed air architecture.*

## 🌪️ System Capabilities & Benefits

Pneuma provides an alternative approach to part cooling by relocating airflow generation away from the toolhead. By utilizing remote vacuum pumps and pneumatic tubing, Pneuma offers several distinct advantages:

- **Targeted Cooling:** By replacing wide-area blowers with focused, high-velocity air at the nozzle exit, Pneuma and a compatible toolhead will help improve overhangs and fine details.
- **Air Source Control:** When paired with Klipper, users can dynamically select their air source—switching between ambient room air or warm internal chamber air. Pneuma utilizes dual dedicated pumps for this, providing extensive and reliable options for makers to best suit their needs.
- **Smart Macro Integration:** Pneuma uses custom Klipper macros to seamlessly intercept standard part cooling commands (`M106`/`M107`). The system can be commanded manually through the Klipper interface, or entirely through your slicer's standard G-code by embedding a simple mode toggle in your filament profiles.
- **Lightweight Toolheads:** Due to removing the typical 4010 or 5015 blowers, toolheads like the [Alembic](https://github.com/Alchemical-3D/Alembic_Toolhead) shed mass, directly benefiting mechanical properties during operation such as acceleration and jerk.
- **Noise Mitigation:** Pneuma utilizes carefully selected, enclosed pumps (similar to premium aquarium & medical equipment) designed to run quieter than typical "Berd Air" or unshielded pressurized air setups, and when configured properly, can be quieter than the fans themselves.
- **Enhanced Visibility:** Removing bulky fans provides a clearer, less obstructed view of the extrusion process, aiding in visual or camera-based print monitoring.
- **Adaptable Performance:** The modular design allows users to swap pump capacities to better suit their specific cooling needs and materials.

---

## ✨ Key Specifications & Features

- **Cooling Delivery:** High-speed compressed air routed via dedicated pneumatic tubing.
- **Pump Integration:** Low noise, reliable vacuum pump operation.
- **Ecosystem Synergy:** Fully compatible with the Alchemical-3D [Alembic](https://github.com/Alchemical-3D/Alembic_Toolhead) and the A3DP gantry kit, also able to support other berd-air toolheads.
- **Professional Package:** Engineered for repeatability, simple service, and long-term reliability.

---

## 🎛️ Firmware & Control

Pneuma relies on a custom Klipper macro to intelligently route standard part cooling commands to the correct pump. This allows you to retain all native slicer cooling behaviors while utilizing dual air sources.

### Klipper Configuration
The required configuration file can be found here: **[Pneuma_Control.cfg](Firmware/Pneuma_Control.cfg)**

1. **Install:** Place the `Pneuma_Control.cfg` file in your Klipper configuration directory and `[include]` it in your `printer.cfg`.
2. **Assign Pins:** Open the file and assign the correct MCU pins for your Cool Pump and Warm Pump. 
3. **Remove Old Fans:** Ensure you comment out or delete your default `[fan]` component in `printer.cfg` to prevent conflicts.

### How to Use
The system intercepts standard `M106` (fan on) and `M107` (fan off) commands. You can dynamically switch which pump receives these commands using the `SET_PNEUMA_MODE` macro.

**Available Modes:**
- `MODE=COOL` : Routes all cooling commands to the dedicated external cool air pump. Ideal for PLA, PETG, and materials needing maximum thermal extraction.
- `MODE=WARM` : Routes all cooling commands to the internal chamber pump. Ideal for ABS, ASA, and materials sensitive to drafts or warping.
- `MODE=DUAL` : Spins up *both* pumps simultaneously when cooling is requested. Reserved for extreme airflow needs.
- `MODE=OFF` : Completely disables part cooling routing to both pumps, ignoring slicer commands until a new mode is set.

**Implementation Examples:**
- **Via Slicer:** Add `SET_PNEUMA_MODE MODE=WARM` to your filament start G-code for ABS/ASA, or `MODE=COOL` for PLA.
- **Via Console:** Type `SET_PNEUMA_MODE MODE=DUAL` in the Klipper terminal for a quick override.
- **Automatic Routing:** When the slicer requests cooling (e.g., `M106 S255`), Klipper will automatically send the PWM signal only to the active pump(s). If you change modes mid-print, the current fan speed is immediately routed to the new pump!

***

## ⚖️ License

This project is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License**. See the [LICENSE.md](LICENSE.md) file for details.

***

**[Join the Discord!](https://discord.gg/aE49DW2xXe)**

> ☕ **Did you find this guide helpful?** 
> 
> My projects are open-source and free for the community. If you've enjoyed my designs and want to support my work, consider [leaving me a tip on Ko-fi](https://ko-fi.com/alchemical3d)! 
>
> [![Ko-Fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/alchemical3d)

