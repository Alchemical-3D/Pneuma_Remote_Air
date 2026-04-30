# 📋 Bill of Materials (BOM)

This list contains all the 3D-printed and physical hardware required to assemble the Pneuma Part Cooling system.

> [!NOTE]
> **Affiliate Links**
> Alchemical-3D has affiliate status with most of the links below. Purchases using these links helps fund the project at no cost to you!  Some of these links even provide a discount off the retail price.

> [!CAUTION]
> **Valve Selection**
> If you choose to configure your Pneuma with a solenoid valve, it is critical that it is **direct acting** or **vacuum acting**. Pressure-acting valves will not function correctly in this vacuum-based system. Some double solenoid valves are able to fully function as long as the core is shared between solenoids.   Please ask on our [Discord](https://discord.gg/r97kK5B7B7) if you are unsure about a specific valve. 

> [!NOTE]
> **Pump Specifications**
> When selecting a vacuum pump, ensure it meets the following minimum specifications for effective part cooling:
> *   **Flow Rate:** Greater than 10L/min (for part cooling only)
> *   **Pressure:** 70 kPa or better
> *   **Vacuum:** -40 kPa or better
> *   **Voltage:** Ensure the pump's voltage matches your intended power supply configuration. 

## 1. Printed Parts

Print these out using the guidelines specified in the [Print Settings](Print_Settings.md) page.

| Part File Name | Qty | Description / Notes | Material | Color |
| --- | :---: | --- | --- | --- |
| `Main_Body.stl` | 1 | Main Body | ABS/ASA | Primary |
| `Rear_Cover.stl` | 1 | Rear Cover | ABS/ASA | Primary |
| `Front_Cover.stl` | 1 | Front Cover | ABS/ASA | Primary |
| `Logo_Detail.stl` | 2 | Logo Detail | ABS/ASA | Accent |
| `Pump_Mount(s).stl` | 1 | Pump Mount | ABS/ASA | Primary |
| `Tube_Grommet.stl` | 3 | Tube Grommet | TPU | Any |
| `Plug_Grommet.stl` | 3 | Plug Grommet | TPU | Any |
| `Table_Mount.stl` | 2 | Optional Table Mount | TPU | Any |
| `Extrusion_Mount_A.stl` | 1 | Optional Extrusion Mount A | ABS/ASA | Primary |
| `Extrusion_Mount_B.stl` | 1 | Optional Extrusion Mount B | ABS/ASA | Primary |
| `Tube_Fitting.stl` | 3 | Fitting, Hardware Dependent | TPU | Any |

> [!NOTE]
> **Additional Printed Parts**
> Additional printed parts may be required for specific use cases, such as tube adaptors for vacuum pumps that have different outlet sizes than the standard pneumatic tubing. A folder will eventually be added to the repository containing a selection of these adaptors for the most common sizes (e.g. 6mm, 8mm, etc.).

## 2. Fasteners and Hardware

| Item | Qty (Est.) | Description |
| --- | :---: | --- |
| **[M3x5x4 Heatsets](https://kb-3d.com/store/inserts-fasteners-adhesives/278-brass-heat-set-threaded-insert-for-plastic-m3x5x4mm.html?affp=6182)** | 5 | Used in the Rear Cover for the Pump Mount |
| **[M3x10 SHCS](https://amzn.to/3P57ILQ)** | 2 | Foot Mounting (Extrusion or Table) |
| **[M3x8 SHCS](https://amzn.to/3P57ILQ)** | 2 | Pump Mounting |
| **[Pneumatic Tubing](https://amzn.to/3P3YzDd)** | 1 | Other diameters will require changes to BOM |
| **[Pneumatic Fitting (1/8 NPT, 6mm OD)](https://amzn.to/3P3YzDd)** | 1 | Valve Chamber Inlet  |
| **[Pneumatic Fitting Right Angle(1/8 NPT, 6mm OD)](https://amzn.to/3P3YzDd)** | 1 | Pump Intake: Helps with tubing bend radius |
| **[M5x12 BHSC](https://amzn.to/42p7gvb)** | 2 | Extrusion Mounting |
| **[M5 Roll in T Nut](https://kb-3d.com/store/extrusion-framing/252-t-nut-drop-inroll-in-20-series-6mm-slot-width-m5-threads-1657989339400.html?affp=6182)** | 2 | Extrusion Mounting |

## 3. Electronics

| Item | Qty | Description |
| --- | :---: | --- |
| **[Vacuum Pump(s)](https://amzn.to/41XWPhK)** | 1 | This link is for the version of the pump that is currently installed in the alpha.  |
| **[Solenoid Valve 3-Way Vacuum Direct Acting](https://amzn.to/3Qx0UXL)** | 1 | Optional, required for air temperature control. |
| **[20AWG High-Temp FEP Wire](https://kb-3d.com/store/wiring-connectors/5530-9177-3do-high-temperature-motion-rated-tc-fep-wire-multiple-sizes-colors.html?affp=6182#/color-black/wiregauge-20awg)** | As Needed | 20AWG, depends on pump current requirements, link is excellent option. |
| **[5-PIN Single Row Molex Micro-Fit 3.0](https://amzn.to/3ODzcbj)** | 1 Each | Male/Female Connectors, pins not included |

> [!IMPORTANT]
> **Part Flexibility & Modifications**
> There is flexibility in the hardware and components you can use for this build. However, please note that veering from the listed parts may require you to modify the 3D models to accommodate your specific hardware. To make this process easier, **STEP files are provided** in the GitHub repository for all printed parts. If you need help with modifications or have specific hardware requests, feel free to join our [Discord](https://discord.gg/r97kK5B7B7) and reach out!
