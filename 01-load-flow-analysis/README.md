# LV Distribution Network Design (ETAP)

## Overview
This project models a simple low-voltage distribution system using ETAP.

The system represents a typical distribution setup from a 33kV grid down to 415V consumer loads.

## System Configuration

- Utility Grid: 33 kV
- Transformer: 1 MVA (33kV / 0.415kV)
- Busbar: 0.415 kV
- Loads:
  - Load 1: 150 kW
  - Load 2: 200 kW

## Network Structure

Grid → Transformer → Bus → Loads

## Analysis Performed

- Load Flow Analysis
- Voltage Drop Analysis
- Cable Impact on System Performance

## Initial Challenges

- Grid was incorrectly set to 0 MVAsc
- High voltage drop (~52%)
- Incorrect cable parameters

---

## Solutions Implemented

- Defined grid short circuit capacity (500 MVA)
- Selected appropriate cable types from library
- Optimized cable lengths

## Key Results

- Voltage stabilized within acceptable range
- Realistic power flow achieved
- Improved system reliability

## Key Learnings

- Accurate input data is critical in power system simulation
- Cable impedance directly affects voltage levels
- Engineering validation is as important as simulation

---

## Tools Used

- ETAP (Electrical Transient Analyzer Program)
