# 📋 Bill of Materials (BOM)

This list contains all the 3D-printed and physical hardware required to assemble the dual-pump Pneuma Part Cooling system.

*Note: Quantities for hardware fasteners trace to verified CAD/assembly sources or carry an explicit `[TBD: ...]` marker where dual-pump / enclosure counts are pending physical verification. Keeping spare hardware on hand is recommended.*

> [!NOTE]
> **Affiliate Links**
> Alchemical-3D has affiliate status with most of the links below. Purchases using these links help fund the project at no cost to you, and some links provide a discount off the retail price.

> [!NOTE]
> **Pump Specifications**
> When selecting diaphragm vacuum pumps (`pump_cool` and `pump_warm`), make sure they meet the following minimum specifications for effective part cooling:
> * **Flow Rate:** Greater than `10L/min` (for part cooling only)
> * **Pressure:** `70 kPa` or better
> * **Vacuum:** `-40 kPa` or better
> * **Voltage:** Ensure the pump voltage matches your intended power supply configuration (`[TBD: pump_supply_voltage]`).

## 1. Printed Parts

Print these components using the guidelines specified in [Print Settings](Print_Settings.md). Do **not** print `Pneuma_201 - Vacuum_Pump.stl` (`60.00 x 60.00 x 126.00 mm`), which is included in `STL_Files/` strictly as a COTS pump reference mesh.

| Part File Name (`STL_Files/`) | Qty | Material | Color / Role | Description / Notes |
| :--- | :---: | :---: | :---: | :--- |
| `Pneuma_201 parts - Main_Body.stl` | `1` | `ABS/ASA` | Primary | Main Enclosure Body (`72.00 x 160.40 x 166.40 mm`) |
| `Pneuma_201 parts - Rear_Cover.stl` | `1` | `ABS/ASA` | Primary | Rear Enclosure Cover (`7.00 x 160.40 x 166.40 mm`) |
| `Pneuma_201 parts - Front_Cover.stl` | `1` | `ABS/ASA` | Primary | Front Enclosure Cover (`5.60 x 160.40 x 166.40 mm`) |
| `Pneuma_201 - Logo_Detail.stl` | `2` | `ABS/ASA` | Accent | Logo Accent Inlay (`3.40 x 25.00 x 25.00 mm`) |
| `Pneuma_201 - Pump_Mount.stl` | `2` | `ABS/ASA` | Primary | Internal Pump Mount (`22.00 x 41.40 x 55.03 mm`; `1` per pump) |
| `Pneuma_201 - TPU_Grommet.stl` | `3` | `TPU` | Any | Pneumatic Tube Pass-Through Grommet (`6.40 x 14.98 x 15.00 mm`; as needed) |
| `Pneuma_201 - Plug_Grommet_TPU.stl` | `3` | `TPU` | Any | Port Blanking Plug Grommet (`5.60 x 15.00 x 15.00 mm`; as needed for unused ports) |
| `Pneuma_201 - Table_Mount_TPU.stl` | `2` | `TPU` | Any | Optional Table / Surface Vibration-Isolator Foot (`7.00 x 10.00 x 45.00 mm`) |
| `Pneuma_201 - Extrusion_Mount_A.stl` | `1` | `ABS/ASA` | Primary | Optional `20`-Series Extrusion Mount A (`19.00 x 29.00 x 77.40 mm`) |
| `Pneuma_201 - Extrusion_Mount_B.stl` | `1` | `ABS/ASA` | Primary | Optional `20`-Series Extrusion Mount B (`19.00 x 29.00 x 77.40 mm`) |
| As-Needed Printed Tube Fittings (`[TBD: optional_tube_adapter_stl_files]`) | `3` *(As Needed)* | `TPU` | Any | Hardware-dependent tube retention fittings or barb adaptors |

> [!NOTE]
> **As-Needed Tube Fittings vs. Blanking Plugs**
> Depending on your plumbing layout and pump barb sizes, enclosure pass-through ports (`5`x `Ø12.00mm` ports on `Main_Body`) can be populated with `Pneuma_201 - TPU_Grommet.stl` tube grommets, sealed with `Pneuma_201 - Plug_Grommet_TPU.stl` blanking plugs, or fitted with printed tube fittings (`[TBD: optional_tube_adapter_stl_files]`) as needed to hold the tubing.

## 2. Fasteners and Hardware

| Item | Qty | Description / Mating Joint |
| :--- | :---: | :--- |
| **[M3x5x4mm Heatsets](https://kb-3d.com/store/inserts-fasteners-adhesives/278-brass-heat-set-threaded-insert-for-plastic-m3x5x4mm.html?affp=6182)** | `5` (`[TBD: CONFLICT — 5 in BOM vs 2 Ø4.70mm on Main_Body + 6 Ø4.70mm on Rear_Cover STEP]`) | Brass heat-set threaded inserts for `Pneuma_201 parts - Rear_Cover.stl`, `Pneuma_201 parts - Main_Body.stl`, and `Pneuma_201 - Pump_Mount.stl` |
| **[M3x10 SHCS](https://amzn.to/3P57ILQ)** | `2` | Foot Mounting (`Pneuma_201 - Extrusion_Mount_A.stl` / `Pneuma_201 - Extrusion_Mount_B.stl` or `Pneuma_201 - Table_Mount_TPU.stl`) |
| **[M3x8 SHCS](https://amzn.to/3P57ILQ)** | `2` (`[TBD: confirm_4x_M3x8_SHCS_for_dual_pump_mounts]`) | Pump Mounting (`Pneuma_201 - Pump_Mount.stl`) |
| **Rear Cover & Enclosure Fasteners** | `[TBD: rear_cover_to_main_body_m3_screw_length_and_qty]` | M3 fasteners securing `Pneuma_201 parts - Rear_Cover.stl` to `Pneuma_201 parts - Main_Body.stl` |
| **[Pneumatic Tubing (`6mm OD`)](https://amzn.to/3P3YzDd)** | `1` (`[TBD: tubing_length_m]`) | `6mm OD` pneumatic line; other diameters require fitting/grommet changes |
| **[Pneumatic Fitting (`1/8 NPT`, `6mm OD`)](https://amzn.to/3P3YzDd)** | `1` (`[TBD: dual_pump_straight_fitting_qty]`) | Straight pressure-side / outlet fitting |
| **[Pneumatic Fitting Right Angle (`1/8 NPT`, `6mm OD`)](https://amzn.to/3P3YzDd)** | `1` (`[TBD: dual_pump_right_angle_fitting_qty]`) | Pump intake fitting to maintain tubing bend radius |
| **[M5x12 BHCS](https://amzn.to/42p7gvb)** | `2` | Extrusion Mounting (`Pneuma_201 - Extrusion_Mount_A.stl` / `Pneuma_201 - Extrusion_Mount_B.stl`) |
| **[M5 Roll-In T-Nut](https://kb-3d.com/store/extrusion-framing/252-t-nut-drop-inroll-in-20-series-6mm-slot-width-m5-threads-1657989339400.html?affp=6182)** | `2` | `20`-series (`6mm` slot width) extrusion mounting |

## 3. Electronics

| Item | Qty | Description |
| :--- | :---: | :--- |
| **[Vacuum Pump(s)](https://amzn.to/4ubXFnG)** | `2` | Dual-Pump configuration (`1`x `pump_cool` + `1`x `pump_warm`; `1` pump for legacy single-pump builds) |
| **[20AWG High-Temp FEP Wire](https://kb-3d.com/store/wiring-connectors/5530-9177-3do-high-temperature-motion-rated-tc-fep-wire-multiple-sizes-colors.html?affp=6182#/color-black/wiregauge-20awg)** | As Needed | `20AWG` motion-rated TC-FEP wire (sized to pump current requirements) |
| **[5-PIN Single Row Molex Micro-Fit 3.0](https://amzn.to/3ODzcbj)** | `1` Each | Male/Female connector housings (crimp pins sold separately) |

> [!NOTE]
> **Legacy Single-Pump + Solenoid Valve Variant (`v1.x`)**
> Pneuma `v2.x` uses two independent pumps (`pump_cool` and `pump_warm`) and requires **zero solenoid valves**. If you are maintaining a legacy single-pump build with a **[3-Way Solenoid Valve](https://amzn.to/3Qx0UXL)** (`Pneuma_201 - 1-8-NPT Direct_Action_Valve.step`, `32.00 x 39.00 x 55.00 mm`), it **must** be a **direct-acting** or **vacuum-acting** valve (or a dual-solenoid valve sharing a common core)—standard pressure-assisted pilot valves will not switch reliably in a vacuum-intake system. Feel free to ask in our [Discord](https://discord.gg/aE49DW2xXe) if you are unsure about a specific valve.

> [!IMPORTANT]
> **Part Flexibility & Modifications**
> Veering from the listed parts may require modifying the 3D models to accommodate your specific hardware. **STEP files are provided** in [`STEP_Files/`](STEP_Files/) for all printed parts to make customization straightforward. If you need help with modifications or have specific hardware questions, join our [Discord](https://discord.gg/aE49DW2xXe) and reach out!

***
*Documentation prepared with AI editorial assistance • Engineered & maintained by Alchemical-3D.*
