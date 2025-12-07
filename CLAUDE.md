# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository contains a comprehensive user manual for the FNIRSI FNB58 USB Fast Charge Tester. It is a documentation-only repository with no source code, build process, or development dependencies.

## File Structure

- `FNIRSI_FNB58_Complete_Manual.md` - Complete user manual (1680+ lines) covering:
  - Device overview and specifications
  - Physical layout and controls
  - Safety warnings and operating procedures
  - Main interface pages (Concise, Monitoring, Waveform, Application)
  - Fast charge protocol functions (PD, QC2.0/3.0, FCP, SCP, AFC, VOOC, SuperVOOC)
  - Statistics functions (energy tracking, battery capacity calculation, offline recording)
  - Toolbox functions (cable resistance, PD listener, E-Marker detection, etc.)
  - Settings and configuration
  - Detailed connection diagrams for each function
  - PC software usage and firmware updates
  - Technical specifications
  - Comprehensive troubleshooting guide

## Document Structure

The manual is organized into 13 main sections with detailed subsections. Key architectural elements:

1. **Connection Diagrams**: Each function includes ASCII-art connection diagrams showing proper device hookup
2. **Safety Warnings**: Critical safety information is prominently placed and repeated where relevant
3. **Step-by-Step Procedures**: Functions with multiple steps (e.g., cable resistance detection) are broken down into numbered steps
4. **Protocol Reference**: Appendix includes detailed explanations of USB charging protocols (PD, QC, FCP, SCP, etc.)

## Working with This Documentation

When editing or analyzing this manual:

- **Device has 3 main port areas**: Top edge (Micro-USB PC port + controls), Bottom edge (5 USB ports + PD switch)
- **PD Communication Switch**: Critical safety component - must be ON for PD functions (PD Trigger, PD Listener, PD Converter, E-Marker), OFF otherwise
- **Four main interface pages**: Concise → Monitoring → Waveform → Application (cycle with LEFT/RIGHT buttons)
- **Voltage limits**: 28V max at monitoring ports, 16V max at PC port
- **Port usage rule**: Only ONE input/output pair can be active at a time

## Key Device Capabilities

- Measurement ranges: 4-28V, 0-7A, 0-120W, cable resistance 0-9999.9Ω
- Protocol support: PD 2.0/3.0, QC2.0/3.0, FCP, SCP, AFC, VOOC/WARP, SuperVOOC
- E-Marker cable chip reading
- Real-time PD protocol monitoring (PD Listener mode)
- Protocol conversion (QC2.0 to PD)

## Common Connection Patterns

```
Basic Monitoring:
[Power Source] → [FNB58 Input] → [FNB58 Output] → [Load Device]

Cable Resistance (2-step process):
Step 1: [Charger] → [FNB58 In] → [FNB58 Out] → [Constant Load 0.5-1A]
Step 2: [Charger] → [Cable Under Test] → [FNB58 In] → [FNB58 Out] → [Same Load]

PD Listener:
[5V Power] → [Micro-USB PC Port]
[PD Charger] → [Type-C IN] → [Type-C OUT] → [PD Device]
(PD Switch: ON)
```

## Safety-Critical Information

When modifying safety sections, preserve these critical warnings:
- PD switch must be returned to OFF after PD functions to prevent accidental high voltage
- Only one input/output pair active at a time
- No devices connected to unused ports during operation
- Voltage limits strictly enforced (28V monitoring, 16V PC port)
- Never disconnect during firmware updates
