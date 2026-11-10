# ⚙️ Print Settings for Pneuma Part Cooling

Print structural enclosure components in **ASA / ABS** (for thermal resistance) or **PETG**, and print structural mounts in **ASA / ABS**. Print the vibration-isolation grommets, blanking plugs, and table-mount feet (`Pneuma_201 - TPU_Grommet.stl`, `Pneuma_201 - Plug_Grommet_TPU.stl`, and `Pneuma_201 - Table_Mount_TPU.stl`) in **TPU**.

> [!IMPORTANT]
> **Exclude Reference CAD Mesh (`Pneuma_201 - Vacuum_Pump.stl`)**
> Do **not** print `Pneuma_201 - Vacuum_Pump.stl` (`60.00 x 60.00 x 126.00 mm`, `190.80 cm³`). It is a COTS reference model of the internal diaphragm pump included in `STL_Files/` for assembly visualization only.

## Slicer Recommendations

*(Structural `ABS`/`ASA` parameters below apply strictly to rigid enclosure and mount parts—do not copy `40%` structural infill onto the `TPU` vibration isolators.)*

| Parameter | Structural Rigid Parts (`ABS` / `ASA` / `PETG`) | Vibration-Isolation Elastomers (`TPU`) |
| :--- | :--- | :--- |
| **Target Parts** | `Main_Body`, `Rear_Cover`, `Front_Cover`, `Logo_Detail`, `Pump_Mount`, `Extrusion_Mount_A/B` | `TPU_Grommet`, `Plug_Grommet_TPU`, `Table_Mount_TPU`, As-Needed Tube Fittings |
| **Material / Shore Hardness** | **ASA / ABS** (Enclosure & Mounts) or **PETG** (Enclosure only) | **TPU** (`[TBD: tpu_shore_hardness]`) |
| **Nozzle Diameter** | `[TBD: nozzle_diameter]` | `[TBD: tpu_nozzle_diameter]` |
| **Layer Height** | `0.2mm` | `[TBD: tpu_layer_height]` |
| **Extrusion Width** | `[TBD: extrusion_width]` | `[TBD: tpu_extrusion_width]` |
| **Wall Perimeters (Loops)** | `4` | `[TBD: tpu_wall_loops]` |
| **Top / Bottom Solid Layers** | `5` | `[TBD: tpu_top_bottom_layers]` |
| **Infill Type & Percentage** | `40%` `Grid` or `Gyroid` | `[TBD: tpu_infill_percentage]` |
| **Supports** | `[TBD: support_requirements]` | `[TBD: tpu_support_requirements]` |

### Calibration Notes
- **Dimensional Accuracy:** Verify filament flow and shrinkage compensation before printing the full enclosure so `M3x5x4mm` brass heat-set inserts and mating covers seat cleanly without splitting layers.

Once your parts are printed, proceed to the [Assembly Guide](Assembly_Guide.md) and cross-check hardware against the [Bill of Materials](BOM.md).

***
*Documentation prepared with AI editorial assistance • Engineered & maintained by Alchemical-3D.*
