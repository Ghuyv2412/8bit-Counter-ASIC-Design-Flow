# 8bit-Counter-ASIC-Design-Flow
RTL-to-GDSII physical design flow of an 8-bit synchronous counter using Synopsys Design Compiler and IC Compiler with SAED 90nm technology.
# 8-bit Counter ASIC Design Flow

A complete RTL-to-Physical-Design flow for an 8-bit synchronous counter using
Synopsys Design Compiler (DC) and Synopsys IC Compiler (ICC1) with the
SAED 90nm standard-cell library.

---

## 1. Project Overview

This project implements and evaluates an 8-bit synchronous counter through
a standard ASIC design flow, from RTL design and synthesis to physical design,
timing analysis, and LVS verification.

The main objective is to understand the relationship between:

- RTL design
- Logic synthesis
- Timing constraints
- Standard-cell mapping
- Floorplanning
- Power planning
- Placement
- Clock Tree Synthesis (CTS)
- Routing
- Static Timing Analysis (STA)

##2. Design Flow

                    RTL
                     │
                     ▼  
              RTL Simulation
                     │
                     ▼
                 Synthesis
          (Synopsys Design Compiler)
                     │
                     ▼
              Gate-Level Netlist
                     │
                     ▼
                Floorplanning
                     │
                     ▼
              Power Planning
                     │
                     ▼
                 Placement
                     │
                     ▼
           Clock Tree Synthesis
                     │
                     ▼
                  Routing
                     │
                     ▼
             Timing Analysis

##3. Tools and Technology

Technology:	            SAED 90nm
Logic Synthesis:        Synopsys Design Compiler
Physical Design:	      Synopsys IC Compiler
ICC Version:            D-2010.03-ICC-SP4
Standard Cell Library:	SAED90nm
Timing Libraries:      	saed90nm_min, saed90nm_typ, saed90nm_max
Clock Period:          	20 ns
Target Frequency:      	50 MHz
Metal Layers:          	9 routable metal layers


##4. Repository Structure

.
├── src/
│   └── counter.v
│
├── tb/
│   └── counter_tb.v
│
├── dc/
│   └── dc_script.tcl
│
├── icc/
│   └── icc_script.tcl
│
├── sdc/
│   └── counter_SDC.sdc
│
├── netlist/
│   └── counter_NL.v
│
├── reports/
│   ├── synthesis/
│   ├── placement/
│   ├── cts/
│   ├── routing/
│   └── lvs/
│
├── images/
│   ├── floorplan.png
│   ├── placement.png
│   ├── cts.png
│   └── routing.png
│
└── README.md

Floorplan:
<img width="2556" height="1287" alt="Screenshot 2026-09-20 202003" src="https://github.com/user-attachments/assets/5aa69488-a9f6-40a0-8de4-fbfbd91cc125" />

Cts:
<img width="2557" height="1282" alt="Screenshot 2026-09-20 202232" src="https://github.com/user-attachments/assets/9e3119b8-133d-4dee-b10f-26fa65bbf4d9" />

Routing:
<img width="2556" height="1285" alt="Screenshot 2026-09-20 202116" src="https://github.com/user-attachments/assets/fa81f534-e971-4c39-884e-aa4ce0b02aa0" />



