# CactusCon 14 Badge (CC14)

Hardware design files and build resources for the **CactusCon 14** conference badge by **Badge Pirates**.

This repo is organized so you can quickly find what you need to **manufacture PCBs**, **print enclosures**, and **inspect the design** in KiCad.

## Quick links

- Schematics (PDF): [`Schematics/CC14.pdf`](Schematics/CC14.pdf)
- Interactive BOM (HTML): [`bom/ibom.html`](bom/ibom.html)
- KiCad project + board files: [`CAD/`](CAD/)
- Gerbers (main + outer): [`CAD/gerbers/`](CAD/gerbers/)
- 3D printable parts (STL/3MF): [`STL/`](STL/)
- Art assets: [`Art/`](Art/)

## Repository layout

- **`CAD/`**
  - KiCad project files (`.kicad_pro`, `.kicad_sch`, `.kicad_pcb`)
  - 3D exports (`.step`)
  - **Gerbers** + drill files (see `CAD/gerbers/`)
- **`Schematics/`**
  - Human-readable schematic export(s) (PDF)
- **`bom/`**
  - Interactive BOM output (`ibom.html`)
- **`STL/`**
  - 3D printable enclosure parts (STL and 3MF)
- **`Art/`**
  - Logo/graphics assets used for silkscreen, cases, etc.

## Manufacturing notes

### PCB fabrication

Use the Gerbers in:

- `CAD/gerbers/` (main board)
- `CAD/gerbers/Outer/` (outer/attendee board)

Most fabs will accept the `.zip` in those folders if present; otherwise, zip the `.gbr` and `.drl` files for upload.

### Assembly

- Start with the **schematic PDF** to understand power and connectors.
- Use the **Interactive BOM** (`bom/ibom.html`) for placement help.

### Enclosure / prints

STL/3MF files live under `STL/`:

- `STL/BadgeBackCover/`
- `STL/BadgeBatteryCover/`

## Tooling

Primary design tool: **KiCad** (project files are under `CAD/`).

## License

- Software/content license: see [`LICENSE`](LICENSE)
- Hardware license: **CERN-OHL-S v2** (see [`LICENSE-HARDWARE.md`](LICENSE-HARDWARE.md))

## Contributing / fixes

PRs are welcome—especially for:

- Documentation improvements (build steps, part notes, printing tips)
- File organization / clearer naming
- Known-issues + troubleshooting notes

If you make changes that affect manufacturing outputs, please regenerate and commit the updated exports (schematic PDF, BOM, gerbers/STEP) as appropriate.
