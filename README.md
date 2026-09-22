# CAD Skill

Professional CAD engineering skill for AI-assisted Fusion 360 workflows.

## Purpose

This skill makes CAD generation **part-first, verification-first, and assembly-aware**.

Instead of creating one large monolithic design, it requires the CAD agent to:

1. Break the design into logical components.
2. Model each physical part independently.
3. Verify each part.
4. Save each part to the requested Fusion 360 cloud project/folder.
5. Build logical subassemblies.
6. Create the final assembly from the saved components.
7. Verify the complete assembly.

## Core Rules

- Parts first, assembly second.
- Save individual parts before assembling them.
- Do not create a huge monolithic final design.
- Use logical subassemblies for complex products.
- Preserve parametric design intent.
- Consider tolerances and tolerance stack-up.
- Check realistic clearances and fits.
- Consider DFM for the intended manufacturing process.
- Add fillets/chamfers where required for strength, safety, and manufacturability.
- Consider stress, strain, deformation, and factor of safety for load-bearing components.
- Check fastener access and assembly/service access.
- Verify motion and interference.
- Do not claim simulation results that were not actually performed.
- Do not invent critical dimensions, loads, materials, or tolerances.
- Maintain clear naming and revision control.
- Verify every component before it enters the assembly.

## Recommended Project Structure

```text
Project/
├── 00_Reference/
├── 01_Parts/
├── 02_Standard_Components/
├── 03_Subassemblies/
├── 04_Final_Assembly/
├── 05_Drawings/
├── 06_Exports/
└── 07_Revisions/
```

## Verification Flow

```text
MODEL
  ↓
CHECK
  ↓
SAVE PART
  ↓
VERIFY SAVE
  ↓
SUBASSEMBLY
  ↓
FINAL ASSEMBLY
  ↓
INTERFERENCE / MOTION CHECK
  ↓
ENGINEERING + DFM CHECK
  ↓
FINAL VERIFY
```

## Engineering Coverage

The skill covers:

- Parametric CAD
- Mechanical part decomposition
- Fusion 360 cloud organization
- Assemblies and subassemblies
- Tolerances and fits
- Clearance checks
- Stress/strain considerations
- Fillets and chamfers
- DFM
- CNC machining
- Sheet metal
- 3D printing
- Injection molding
- Laser/waterjet fabrication
- Fastener design
- Motion/kinematic checks
- Assembly/serviceability
- Revision control

## File

The complete skill specification is provided in [SKILL.md](SKILL.md).

## License

MIT License. See [LICENSE](LICENSE).
