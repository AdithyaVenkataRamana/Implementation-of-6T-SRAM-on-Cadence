# Implementation-of-6T-SRAM-on-Cadence
# 6T SRAM Cell Design using Cadence Virtuoso

---

## 🧾 Abstract

This project focuses on the transistor-level design and simulation of a **6-Transistor (6T) Static Random-Access Memory (SRAM)** cell using **Cadence Virtuoso**. The 6T SRAM is a widely used memory element in digital systems due to its speed, low power consumption, and stability. The objective is to design a functional SRAM cell and validate its key operations — **Write**, **Read**, and **Hold** — through schematic design and transient simulation.

---

## 1. Introduction

SRAM (Static Random-Access Memory) is a crucial component in modern digital electronics, particularly in high-speed memory applications such as caches, register files, and buffers. Unlike DRAM, SRAM does not require periodic refreshing, making it faster and more reliable.

The **6T SRAM cell** is composed of:
- **Two cross-coupled inverters** (for data storage)
- **Two access transistors** (for controlling read/write operations)

This project aims to replicate the standard 6T SRAM cell and test its functionality under typical conditions using Cadence Virtuoso.

---

## 2. Design Overview
![Image](https://github.com/user-attachments/assets/ea1603f0-43f6-4fb8-a3ed-a5b6d9108583)
The structure of the 6T SRAM includes the following transistors:
- **M1 & M2:** PMOS pull-up transistors
- **M3 & M4:** NMOS pull-down transistors
- **M5 & M6:** NMOS access transistors connected to bitlines

### Key Nodes:
- **Q and Q̅:** Internal storage nodes
- **BL and BL̅:** Bitlines used for read/write
- **WL:** Wordline that enables access during read/write

The cell operates in three modes:
- **Hold:** WL is LOW, cell retains its state
- **Write:** WL is HIGH, data is written through bitlines
- **Read:** WL is HIGH, data is read from bitlines without disturbing internal state

---

## 3. Design Methodology

The design and simulation were carried out in Cadence Virtuoso using the following steps:

### 📐 Schematic Design:
- Constructed the 6T cell using standard CMOS transistors.
- Connected the access transistors to BL, BL̅, and WL for read/write control.
- Designed cross-coupled inverters to maintain bistable data storage.

### Transient Simulation:
- Simulated write, read, and hold conditions using test benches.
- Observed internal node voltages and bitline behavior.

###  Simulation Environment:
- **VDD:** 1.8V
- **Technology Node:** (Specify if known)
- **Tools Used:** Cadence Virtuoso Schematic Editor, ADE for simulation

---

## 4. Simulation and Results
![Image](https://github.com/user-attachments/assets/ec958d4d-f788-4f6b-9f01-bc6982fc708f)
![Image](https://github.com/user-attachments/assets/2fad8deb-3a48-4bd2-ba05-0c94b6d94563)
![Image](https://github.com/user-attachments/assets/e4688903-3bf0-4db6-ae7e-a9de2cc4168a)
###  Write Operation:
- Bitlines set to the desired value.
- WL activated (HIGH).
- Internal node Q/Q̅ flips to reflect bitline input.

###  Read Operation:
- Bitlines precharged.
- WL activated (HIGH).
- Output observed without affecting internal state.

###  Hold Operation:
- WL disabled (LOW).
- Cell retains stored value indefinitely.

Simulation waveforms show successful transitions during write, correct data readout, and robust state holding, validating the 6T SRAM design.

---

## 5. Conclusion

The 6T SRAM cell was successfully implemented and tested using Cadence Virtuoso. Simulation results confirm that the cell correctly performs read, write, and hold operations. This foundational design can be extended to create larger memory arrays and serve as a base for memory-centric VLSI designs.

---

## 👨‍💻 Author

**Adithya Venkata Ramana**  
VLSI Design Enthusiast | SRAM | CMOS Circuits | Cadence Virtuoso

---

## 📜 License

This project is released for educational and non-commercial use only. Attribution is appreciated.
