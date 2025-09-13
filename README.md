# Project Orion – RK3588S Development Board

A powerful, compact, and open-source development board built from scratch around the **Rockchip RK3588S** SoC. Designed for **makers, students, and professionals**, Orion balances high performance, expandability, and modern connectivity in a hand-designed SBC form factor. The board runs **Linux (Armbian/Ubuntu/Debian)** and supports advanced **AI, multimedia, and IoT applications**.

---

**About the creator**  
I am 19 years old and just starting university as an **Electronics Engineering** student. With prior experience in hobby electronics and PCB design, I’m using Project Orion to dive into **high-speed interfaces (LPDDR5, PCIe Gen3, USB 3.1, HDMI 2.1, MIPI)**, **power sequencing with PMICs**, and **Linux bring-up on a modern ARM SoC**. This project is both a functional SBC and a deep learning journey into advanced hardware design.

---

## ✨ Key Features
- **SoC:** Rockchip RK3588S (Octa-core: 4× Cortex-A76 + 4× Cortex-A55, Mali-G610 MP4 GPU, 6 TOPS NPU)
- **Memory:** Up to 16 GB LPDDR5 RAM (soldered BGA)
- **Storage:**
  - Onboard eMMC (up to 128 GB)
  - microSD card slot (boot or expansion)
  - NVMe SSD via M.2 (2242/2280, PCIe 3.0 x2)
- **Connectivity:**
  - 2.5G Ethernet (RJ45, optional PoE-PD)
  - Wi-Fi 6/6E + Bluetooth 5.2 via M.2 E-key
  - 4G/5G modem support via M.2 B-key (Quectel RM502Q, EG25-G, etc.)
  - GNSS/GPS supported through cellular modules
- **I/O:**
  - 40-pin GPIO header (Pi-compatible pinout)
  - Interfaces: SPI, I²C, UART, PWM, ADC, GPIO
  - Native **CAN-FD** (RK3588S integrated support)
- **Display & Camera:**
  - 1× HDMI 2.1 (up to 8K@60fps output)
  - 1× MIPI-DSI (4 lanes, high-res LCD support)
  - 2× MIPI-CSI (camera input)
- **USB & Expansion:**
  - USB-C with Power Delivery (data + power)
  - 2× USB 3.1 Gen1 Host
  - 2× USB 2.0 Host/OTG
  - Dual M.2 slots (B-key for cellular, E-key for Wi-Fi/BT, M-key for NVMe SSD)
- **Power:**
  - USB-C PD input (STUSB4500 controller)
  - RK806 PMIC for SoC sequencing + regulators
  - Single-cell LiPo battery support (BQ25895 charger + power-path)
  - Fuel gauge (MAX17055)
- **Form Factor:**
  - Compact ~100 × 80 mm PCB
  - 6–8 layer HDI design with impedance-controlled routing
  - Active cooling support (fan or heatsink)

---

## 🛠 Project Goals
- Create a **next-generation SBC** with the RK3588S SoC for AI, robotics, edge computing, and embedded Linux development.
- Provide a **learning-first approach** to high-speed BGA/DDR design, PMIC integration, and Linux bring-up.
- Deliver **open hardware documentation** (schematics, PCB files, BOM, block diagrams).
- Keep board size within **<10 × 10 cm** while balancing complexity and manufacturability.
- Showcase a **journey in advanced PCB design**, covering:
  - LPDDR5 high-speed layout and length-matching
  - PCIe/USB 3.1/HDMI 2.1 differential pair routing
  - Power sequencing with RK806 PMIC
  - Thermal design (copper pours, heatsink mounting)
  - Bring-up of U-Boot, kernel, and device tree

---

## 📂 Repository Structure

/docs → Block diagrams, design notes, datasheets
/hardware → KiCad schematics, PCB layout, Gerbers
/firmware → Bootloader (U-Boot), Device Tree, kernel patches
/software → Rootfs setup, build scripts, test utilities
/cad → Mechanical drawings, 3D STEP models
/production → BOM, assembly files, test

---

## 🖼 Block Diagram
![Block Diagram](docs/block-diagram/orion_block_diagram.jpg)

---

## 🚀 Getting Started (Future)
1. Flash the provided Armbian/Ubuntu image to microSD or eMMC.
2. Connect display (HDMI 2.1 / MIPI), keyboard, and power via USB-C.
3. Boot into Linux and expand storage if needed.
4. Optional: Insert Wi-Fi/BT or cellular M.2 module and configure networking.

---

## 📡 Roadmap
- [ ] Finalize block diagram & power tree
- [ ] Schematic capture in KiCad (SoC + PMIC + DDR + I/O)
- [ ] DDR5 routing & 6–8 layer PCB layout
- [ ] Prototype manufacturing (JLCPCB HDI) + bring-up
- [ ] Linux boot (U-Boot + Armbian)
- [ ] Validate peripherals (Ethernet, PCIe, USB 3.1, HDMI 2.1, CSI/DSI, CAN-FD)
- [ ] Release open-source hardware files and documentation

---

## ⚖ License
- Hardware: **CERN OHL-S** (Open Hardware License, Strongly Reciprocal)  
- Software: **GPLv3** / **Apache 2.0** depending on component

---

## 🤝 Contributing
Contributions are welcome!
- Suggest new features
- Help test Linux builds
- Share improvements for schematics/PCB layout
- Submit demos or software support patches

---

## 📢 Status
🚧 **Work in Progress** – This repo documents the journey of designing and building a complete SBC from scratch around the RK3588S.

Follow along and contribute as we bring **Project Orion** to life ✨
