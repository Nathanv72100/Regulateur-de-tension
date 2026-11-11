# USB-C Power Delivery Voltage Module

A custom-designed USB-C Power Delivery (PD) voltage selection board based on the **CH224K** controller.

This project aims to provide a compact PCB capable of negotiating a power supply voltage through a USB-C PD source.

## Project Overview

The board uses the CH224K USB-C PD trigger controller to communicate with a compatible USB-C Power Delivery charger and request a supported voltage profile.

The project includes:
- A USB-C input connector.
- A CH224K USB PD negotiation controller.
- Configuration pins (CFG1, CFG2, CFG3).
- A selection switch.
- Passive components for circuit configuration.
- A custom-designed PCB.

## Main Components

| Component | Reference | Quantity |
|---|---|---:|
| CH224K PD Controller | U1 | 1 |
| USB-C Connector | USB1 | 1 |
| Configuration Switch | U2 | 1 |
| 1 µF Capacitor | C1 | 1 |
| 1 kΩ Resistors | R1, R3, R4, R6 | 4 |
| 10 kΩ Resistor | R5 | 1 |
| 2-pin Headers | H1, H2 | 2 |
<img width="917" height="234" alt="image" src="https://github.com/user-attachments/assets/0509dc3a-81f1-4657-99b9-3f53337a120b" />

## Design

The electronic schematic and PCB layout were designed using **EasyEDA**.

The project files are available in this repository:

- `regulateur.json` – Electronic schematic.
- `PCB_régulateur de tension.json` – PCB design.

## How It Works

1. Connect a compatible USB-C PD power supply.
2. The CH224K communicates with the power supply.
3. The configuration pins determine the requested voltage profile.
4. The power supply negotiates the requested voltage.
5. The negotiated voltage is made available at the board's output.

## Important Notes

- The power supply must support USB Power Delivery.
- The CH224K handles PD negotiation; it is not, by itself, a DC-DC voltage regulator.
- Available output voltages depend on the power supply and the CH224K configuration.
- Output voltage and current limits must be verified before connecting any load.
- The board should be tested before being used with sensitive electronics.

## Project Status

**Hardware design:** PCB and schematic designed.
<img width="451" height="853" alt="image" src="https://github.com/user-attachments/assets/a83ae16c-6ddf-43fe-a91a-4ad903acd8e6" />

**Testing:** Not yet documented.

**Next steps:**
- Manufacture the PCB.
- Assemble the components.
- Test USB-C PD negotiation.
- Verify output voltage and current.
- Validate the board under load.

## Tools & Technologies

- EasyEDA
- PCB Design
- USB-C Power Delivery
- CH224K Controller
- Electronic Circuit Design

## Author

Designed by **nathanv72100**.

---

*This project is an electronics design project focused on USB-C Power Delivery and custom PCB development.*
