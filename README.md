# PCB-Design-of-ESP32-Power-Supply-Battery-Management-
(12V Input → 2S Li-ion Charging → 5V Regulation)

## 📌 Project Overview
This repository contains the **complete PCB design** of a **power supply and battery management system** intended for an **ESP32-based embedded system** (Infinity Pool Control System).

The design includes:
- Dual buck converters
- 2S Li-ion battery charging path
- BMS integration
- Regulated 5V output for ESP32
- Fully custom schematic, PCB layout, and 3D visualization

The entire design process was carried out following **datasheet-based component selection**, **PCB design rules**, and **real-world hardware constraints**.

---

## 🔌 Power Architecture

### Workflow Explanation
- **12V DC Input:** External power source (SMPS or adapter).
- **Buck Converter (12V → 8.4V):** Steps down voltage to safely charge the 2S Li-ion battery pack.
- **2S Li-ion Battery Pack:** Provides energy storage for backup operation.
- **2S BMS:** Protects the battery from overcharge, overdischarge, and overcurrent conditions.
- **Buck Converter (8.4V → 5V):** Regulates battery voltage to a stable 5V supply.
- **ESP32 / External Load:** Main controller and peripherals powered by regulated 5V.

This workflow ensures **safe charging**, **battery protection**, and **stable power delivery** to the ESP32 system.

---

## ⚙️ Functional Blocks

### 1. 12V Input Stage
- Accepts external **12V DC input**
- Input filtering capacitors added for noise suppression
- Designed for SMPS or adapter input

### 2. 8.4V Buck Converter (Battery Charging Rail)
- Steps down 12V to **8.4V**
- Used as charging voltage for **2S Li-ion battery pack**
- Designed using **LM2596-based topology**
- Output connected to BMS input

### 3. Battery Management System (BMS)
- Supports **2S Li-ion configuration**
- Provides:
  - Overcharge protection
  - Overdischarge protection
  - Overcurrent / short-circuit protection
- Ensures safe battery operation during charge and discharge

### 4. 5V Buck Converter (ESP32 Supply)
- Converts battery voltage (7.4V–8.4V) to **regulated 5V**
- Designed to handle ESP32 peak current demands
- Stable output for MCU, display, and peripherals

---

## 🧩 PCB Design Workflow

This project follows a **complete professional PCB development flow**:

1. **Schematic Design**
   - All components selected based on datasheets
   - Proper feedback networks for buck converters
   - Correct grounding and power net separation

2. **Custom Libraries**
   - Custom schematic symbols created where required
   - Custom PCB footprints designed using manufacturer dimensions
   - Pin spacing, pad size, and polarity verified

3. **3D Component Models**
   - 3D bodies added for all major components
   - Ensured correct height, orientation, and placement
   - Used for mechanical and enclosure validation

4. **PCB Layout & Routing**
   - Proper trace width for power paths
   - Short, low-impedance feedback loops
   - Star grounding where required
   - High-current paths carefully routed
   - Silkscreen labels for connectors and components

5. **Finalization**
   - Design Rule Check (DRC) passed
   - Layout verified against schematic
   - Ready for fabrication and assembly

---

## 🖼️ Project Outputs
The repository includes:
- Schematic design
- PCB layout
- 3D PCB visualization
- Power routing verification
- Connector labeling for easy assembly

(Images included in repository for reference)

---

## 🛠 Tools Used
- **Altium Designer Software:** Altium Designer/Proteus (as applicable)
- **3D Modeling:** Integrated PCB 3D viewer
- **Datasheets:** Manufacturer reference documents
- **Design Rules:** Standard low-voltage PCB constraints

---






