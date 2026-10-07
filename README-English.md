# Schematic and PCB Design Notes

[中文](README.md) | [English](README-English.md)

This repository organizes learning materials about schematic capture, PCB design, EDA tools, component footprints, and electronic soldering. The content is based on the PDF and DOCX materials in `docs/` and is suitable for electronics engineering, embedded hardware, and PCB beginners.

## Materials

### Schematic and PCB Design

- [PDF course material](docs/原理图与PCB制作.pdf)
- [DOCX editable version](docs/原理图与PCB制作.docx)

### Soldering Skills

- [PDF course material](docs/焊接技能.pdf)
- [DOCX editable version](docs/焊接技能.docx)

## Learning Roadmap

```text
EDA and project fundamentals
    ├── EDA software and PCB industry tools
    ├── EasyEDA environment
    ├── Drawing units and project management
    └── Complete schematic-to-PCB workflow
            ↓
Schematic design
    ├── Search and place components
    ├── Power, ground, and net connections
    ├── Component names, references, and orientation
    └── DRC
            ↓
PCB design
    ├── Create a PCB from the schematic
    ├── Board outline and component placement
    ├── Routing, copper pours, and net labels
    ├── Silkscreen adjustment and DRC
    └── 3D preview and manufacturing outputs
            ↓
Advanced design
    ├── Multilayer boards, blind/buried vias, and teardrops
    ├── File import and export
    ├── Custom symbols and footprints
    └── Footprint dimensions and component binding
            ↓
Projects and soldering
    ├── Adjustable resistor and independent-button circuits
    ├── 74HC138 decoder
    ├── 74HC245 signal driver
    ├── LM358 PWM generator
    └── Soldering iron, solder, and rework tools
```

## Contents

### Chapter 1: EasyEDA Schematic and PCB Quick Start

- Understand the purpose of EDA (Electronic Design Automation).
- Learn the basic use of common PCB design tools and EasyEDA.
- Manage accounts, software, projects, and local project files.
- Understand the complete workflow from component selection and library preparation to schematic capture, PCB generation, manufacturing, and validation.
- Use `inch`, `mm`, and `mil` as drawing units.
- Use a button-and-LED circuit to learn component search, placement, wiring, property adjustment, and reference management.
- Generate a PCB from a schematic and complete the board outline, placement, routing, net labels, copper pour, and silkscreen.
- Use DRC to check connection problems and inspect a 3D PCB preview.
- Understand the preparation of PCB manufacturing files and component orders.

### Chapter 2: PCB Manufacturing Fundamentals

- Understand the definition, purpose, and basic structure of a PCB.
- Learn the benefits of PCB technology, including density, reliability, designability, manufacturability, testability, assembly, and maintainability.
- Understand common PCB EDA tools and basic manufacturing documentation.
- Learn component-placement principles:
  - Group electrically related components into functional modules.
  - Place connectors near board edges and clearly mark orientation, voltage level, and polarity.
  - Separate high-voltage, low-voltage, high-current, high-frequency, and heat-generating circuits appropriately.
  - Place decoupling and filter capacitors close to power-entry points or power-conversion devices.
- Learn PCB-routing principles:
  - Set trace width and clearance according to current, frequency, fabrication capability, and signal-integrity requirements.
  - Avoid routing corners sharper than 90 degrees.
  - Pay attention to spacing and interference control for high-speed and high-frequency signals.

### Chapter 3: EDA Techniques

- Add net labels and no-connect markers in batches.
- Troubleshoot airwires that remain after a copper pour.
- Import external images and logos.
- Configure multilayer boards and create or place blind and buried vias.
- Use teardrops to improve the mechanical strength and electrical reliability of trace-to-pad connections.
- Distinguish local `.eprj` projects from browser `.epro` projects.
- Import, export, and convert project files.

### Chapter 4: Custom Symbols and Component Footprints

- Create custom schematic symbols in standard and professional modes.
- Draw a footprint manually, using an 0805 capacitor as an example.
- Generate a footprint with a footprint wizard, using CH340N as an example.
- Check footprint dimensions.
- Bind schematic symbols to personal footprints.
- Learn common DIP, QFP, SOP, QFN, and BGA packages.
- Understand imperial and metric package codes for chip resistors and capacitors.
- Understand trace width, clearance, and common PCB design units.

### Chapter 5: Schematic and PCB Projects

- Use an adjustable resistor to control LED brightness.
- Use an independent button to control an LED.
- Build a 3-to-8 decoder with 74HC138.
- Use 74HC245 to improve signal-drive capability.
- Use LM358 to generate a PWM square wave.
- Follow the complete process of component selection, schematic capture, DRC, PCB conversion, placement, routing, copper pour, silkscreen, and final checks.

### Soldering Skills

- Understand the use cases of basic and temperature-controlled soldering irons.
- Learn the role of solder alloy and flux.
- Distinguish leaded and lead-free solder and maintain adequate ventilation.
- Use reusable adhesive putty to hold components during soldering.
- Use a magnifier to inspect small components and solder joints.
- Use a solder sucker for desoldering and rework.

## PCB Design Workflow

```text
Requirements analysis
  ↓
Component selection
  ↓
Confirm or create symbols and footprints
  ↓
Schematic capture
  ↓
Schematic DRC
  ↓
Generate PCB
  ↓
Board outline and component placement
  ↓
Routing and copper pour
  ↓
Silkscreen and net labels
  ↓
PCB DRC and visual inspection
  ↓
3D inspection and manufacturing output
  ↓
PCB fabrication, soldering, debugging, and testing
```

## Engineering Checkpoints

| Stage | Main checks |
| --- | --- |
| Component selection | Parameters, footprint, pinout, availability, and alternatives |
| Schematic | Power, ground, net names, connections, references, and unused pins |
| Schematic DRC | Floating pins, shorts, unconnected nets, and rule warnings |
| PCB placement | Functional grouping, connector direction, voltage spacing, thermal design, and decoupling |
| PCB routing | Trace width, clearance, corners, return paths, interference, and current capacity |
| PCB DRC | Clearance, shorts, unconnected nets, board outline, and design rules |
| Manufacturing preparation | Layers, outline, silkscreen, footprints, Gerber files, BOM, and assembly requirements |
| Soldering and debugging | Polarity, joints, cold solder, solder bridges, supply voltage, and power-up sequence |

## Suggested Study Process

1. Complete the button-and-LED project first to learn the full schematic-to-PCB loop.
2. Run schematic DRC before starting PCB placement and routing.
3. Check the datasheet, package dimensions, pinout, and purchasing information during component selection.
4. Divide power, interfaces, control, clock, and signal sections before routing connections between modules.
5. After PCB completion, perform DRC, 3D inspection, silkscreen inspection, and manufacturing-file checks.
6. Before soldering, verify component orientation, polarity, package, and pad mapping.

## Directory Structure

```text
schematic-and-pcb-design/
├── README.md
├── README-English.md
└── docs/
    ├── 原理图与PCB制作.pdf
    ├── 原理图与PCB制作.docx
    ├── 焊接技能.pdf
    └── 焊接技能.docx
```

## Current Scope

The repository currently focuses on course PDFs, DOCX source files, and a learning index. It does not include additional EDA projects, Gerber manufacturing files, or physical-board photos. Future work can add schematic files, PCB projects, BOMs, manufacturing outputs, and soldering records for the course examples.

## Keywords

`Schematic` `PCB Design` `EDA` `EasyEDA` `JLCEDA` `DRC` `PCB Layout` `PCB Routing` `Footprint` `Symbol` `Gerber` `BOM` `Soldering`
