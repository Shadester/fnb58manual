# FNIRSI FNB58 USB Fast Charge Tester - Complete User Manual

## Table of Contents
1. [Device Overview](#device-overview)
2. [Physical Layout & Controls](#physical-layout--controls)
3. [Safety Warnings](#safety-warnings)
4. [Basic Operation](#basic-operation)
5. [Main Interface Pages](#main-interface-pages)
6. [Fast Charge Functions](#fast-charge-functions)
7. [Statistics Functions](#statistics-functions)
8. [Toolbox Functions](#toolbox-functions)
9. [Settings & Configuration](#settings--configuration)
10. [Connection Diagrams for Each Function](#connection-diagrams-for-each-function)
11. [PC Software & Firmware Updates](#pc-software--firmware-updates)
12. [Specifications](#specifications)
13. [Troubleshooting](#troubleshooting)

---

## Device Overview

The FNIRSI FNB58 is a high-reliability USB voltage and current detection meter with fast charging protocol support. It features:

- 2.0-inch full-color TFT LCD display with auto-rotation (gravity sensor)
- External 16-bit ADC for high precision measurements
- Dedicated PD protocol physical chip
- Multiple USB ports: USB-A, USB-C, and Micro-USB
- Support for QC2.0/3.0, PD2.0/3.0, FCP, SCP, AFC, VOOC, WARP, SuperVOOC protocols
- Bluetooth connectivity (blue model only)
- PC software support via Micro-USB connection

**Measurement Ranges:**
- Voltage: 4V - 28V (0V - 28V with external power)
- Current: 0A - 7A
- Power: 0W - 120W
- Capacity: 0 - 9999.99Ah
- Energy: 0 - 9999.99Wh
- Cable Resistance: 0 - 9999.9Ω

---

## Physical Layout & Controls

### Port Locations

**Top Edge:**
1. Micro-USB port (PC connection - for external power and PC software connection)
2. Three-way dial switch (Left/Center/Right navigation)
3. BACK button

**Bottom Edge:**
4. USB-C input port
5. Micro-USB input port
6. USB-A input port
7. USB-C output port
8. USB-A output port
9. PD Communication toggle switch (ON/OFF)

### Control Buttons

**Three-Way Dial Switch:**
- Press/Slide LEFT: Navigate left, decrease values
- Press CENTER: Confirm selection, enter menus, pause/resume
- Press/Slide RIGHT: Navigate right, increase values

**BACK Button:**
- Short press: Return to previous page, cancel operation
- Long press: Turn off/on screen backlight (works on all pages)

---

## Safety Warnings

⚠️ **CRITICAL SAFETY INFORMATION - READ BEFORE USE:**

1. **Voltage Limits:**
   - Do NOT connect monitoring interfaces to power supplies exceeding 28V
   - Do NOT connect PC port to power sources exceeding 16V

2. **Port Usage:**
   - Only ONE pair of monitoring interfaces (one input + one output) can work at a time
   - When one pair is active, do NOT connect equipment to other monitoring interfaces
   - Exception: PC connection port can be connected for external power

3. **Fast Charge Trigger:**
   - When using fast charge trigger, do NOT connect devices that cannot handle high voltage to any monitoring interface
   - Do NOT charge phones after triggering fast charge without proper verification

4. **PD Communication Switch:**
   - After using PD trigger/monitor/conversion/E-Marker functions, turn PD switch back to OFF position
   - Accidentally leaving PD switch ON with wrong connections can trigger unexpected high voltage

5. **Current Direction:**
   - Pay attention to current direction indicators on screen
   - Ensure proper input/output port usage

---

## Basic Operation

### Powering On the Device

The FNB58 can be powered in several ways:

**Method 1: Standard Testing (Recommended)**
- Connect: Power Source → FNB58 Input Port → Load Device
- Example: USB Charger → FNB58 USB-C Input → FNB58 USB-C Output → Phone
- Device powers on automatically when current flows through

**Method 2: External Power for Special Functions**
- Connect 5V power supply to Micro-USB (PC) port on top edge
- Used for: PD Listener, firmware updates, standalone operation
- Maximum voltage: 16V (typically use 5V)

**Method 3: Bootloader Mode (Firmware Updates)**
- Hold down CENTER button (middle position)
- While holding, connect Micro-USB cable to PC port
- Device enters bootloader mode for firmware updates

### Navigation Basics

**General Navigation Pattern:**
- LEFT/RIGHT buttons: Switch between pages or menu options
- CENTER button: Confirm selection or enter submenu
- BACK button: Cancel or return to previous page
- Long press BACK: Toggle screen backlight

**Four Main Pages (Cycle with LEFT/RIGHT):**
1. Concise Page - Basic voltage/current/power
2. Monitoring Page - Detailed statistics and energy data
3. Waveform Page - Real-time voltage/current curves
4. Application Page - Access to all advanced functions

---

## Main Interface Pages

### 1. Concise Page

**Display Information:**
- VBUS: Bus voltage
- IBUS: Bus current
- PBUS: Power (calculated)
- TEMP: Internal temperature sensor reading
- Current direction indicator
- Run/Pause status (green = running, red = paused)

**Functions:**
- Press CENTER: Toggle between Run (live data) and Pause (hold values)
- Shows only essential measurements

### 2. Monitoring Page

**Display Information:**
- Voltage, current, power (top section)
- NRG Statistics: Energy consumption data
- CAP: Capacity measurement
- NRG: Energy measurement
- Offline recording status
- Trigger protocol information
- Group number (if using multiple data sets)

**Functions:**
- Press CENTER: Enter recallable function menu
  - Previous group
  - Next group
  - Start/Clear offline records
  - Start time limit
- View accumulated energy and capacity data

### 3. Waveform Page

**Display Information:**
- Real-time voltage and current waveforms
- Time base settings
- Waveform mode indicator
- 9-hour maximum recording support

**Functions:**
- Long press LEFT: Decrease time base
- Long press RIGHT: Increase time base
- Press CENTER: Start/pause curve drawing
- Long press CENTER: Switch between modes (voltage/current/power curves)

**Four Waveform Modes:**
1. Voltage curve
2. Current curve
3. Power curve
4. Voltage + Current combined

### 4. Application Page

**Main Menu Options:**
- Fast Charge
- Statistics
- Toolbox
- Settings

Press CENTER on any option to enter that submenu.

---

## Fast Charge Functions

⚠️ **WARNING:** A safety warning will appear when entering Fast Charge functions. Read carefully and press CENTER to confirm.

**Connection for Fast Charge Testing:**
```
Power Source → FNB58 Input → FNB58 Output → Load Device (or no load for detection)
```

### 1. Automatic Detection

**Purpose:** Test which fast charging protocols a charger supports

**How to Use:**
1. Navigate to Application Page → Fast Charge → Automatic Detection
2. Press CENTER to start
3. Wait for test to complete (device may restart during PD testing - this is normal)
4. Results display: Green = Supported, Red = Not Supported

**Tested Protocols:**
- PD (Power Delivery) 2.0/3.0
- Apple 2.4A
- BC1.2 (Battery Charging)
- Samsung AFC
- Huawei FCP
- Huawei SCP
- Qualcomm QC2.0
- Qualcomm QC3.0
- VOOC/DASH/WARP
- SuperVOOC 1.0/2.0
- MTK PE+

**Important Notes:**
- Do NOT connect equipment to output during automatic detection
- Device will not respond to buttons during testing
- To exit mid-test: Physically unplug the meter
- After completion: Press CENTER to test again, or BACK to return

**Connection Diagram:**
```
[Charger] ---> [FNB58 Input Port] ---> [FNB58 Output Port] ---> (Leave empty or light load)
```

### 2. PD Trigger

**Purpose:** Manually trigger specific PD voltage/current profiles

**Prerequisites:**
- Turn PD Communication switch to ON position
- Use PD-compatible charger and device

**How to Use:**
1. Turn PD switch to ON
2. Navigate to Fast Charge → PD Trigger
3. Press CENTER to enter
4. Charger will send available voltage/current profiles (example: 7 profiles)
5. Press CENTER to highlight adjustment window (border turns green)
6. Use LEFT/RIGHT to select:
   - Gear selection (profiles 1-7)
   - Voltage adjustment (for PPS - Programmable Power Supply)
   - Current adjustment
7. Press CENTER to confirm selection
8. Press BACK to exit (IMPORTANT: Turn PD switch back to OFF)

**Typical PD Profiles Shown:**
- Profile 1: 5.00V @ 3.00A
- Profile 2: 9.00V @ 3.00A
- Profile 3: 12.00V @ 3.00A
- Profile 4: 15.00V @ 3.00A
- Profile 5: 20.00V @ 3.00A
- Profile 6-7: PPS (Programmable) 3.30-21.00V

**Connection Diagram:**
```
[PD Charger] ---> [FNB58 Type-C Input] ---> [FNB58 Type-C Output] ---> [PD Device]
                                      ^
                                      |
                              PD Switch: ON
```

### 3. QC2.0 Trigger

**Purpose:** Trigger Qualcomm Quick Charge 2.0 voltages

**How to Use:**
1. Navigate to Fast Charge → QC2.0
2. Press CENTER to enter
3. Use LEFT/RIGHT to select voltage: 5V, 9V, 12V, or 20V
4. Press CENTER to confirm and trigger
5. Press BACK to exit/return

**Connection Diagram:**
```
[QC2.0 Charger] ---> [FNB58 USB-A or Type-C Input] ---> [FNB58 Output] ---> [Device]
```

### 4. QC3.0 Trigger

**Purpose:** Trigger and adjust Qualcomm Quick Charge 3.0 voltages

**How to Use:**
1. Navigate to Fast Charge → QC3.0
2. Press CENTER to enter
3. Use LEFT/RIGHT to decrease/increase voltage in 0.2V steps
4. Range: 3.4V - 20.0V
5. Press LEFT/RIGHT repeatedly for faster adjustment
6. Press BACK to exit

**Connection Diagram:**
```
[QC3.0 Charger] ---> [FNB58 USB-A or Type-C Input] ---> [FNB58 Output] ---> [Device]
```

### 5. FCP Trigger

**Purpose:** Trigger Huawei Fast Charge Protocol

**How to Use:**
1. Navigate to Fast Charge → FCP
2. Press CENTER to enter
3. Use LEFT/RIGHT to select voltage
4. Operation similar to QC2.0
5. Press BACK to exit

**Connection Diagram:**
```
[Huawei FCP Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device]
```

### 6. SCP Trigger

**Purpose:** Trigger Huawei SuperCharge Protocol

**How to Use:**
1. Navigate to Fast Charge → SCP
2. Press CENTER to enter
3. Use LEFT/RIGHT to select voltage/current
4. Operation similar to QC2.0
5. Press BACK to exit

**Connection Diagram:**
```
[Huawei SCP Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device]
```

### 7. AFC Trigger

**Purpose:** Trigger Samsung Adaptive Fast Charging

**How to Use:**
1. Navigate to Fast Charge → AFC
2. Press CENTER to enter
3. Use LEFT/RIGHT to select voltage
4. Operation similar to QC2.0
5. Press BACK to exit

**Connection Diagram:**
```
[Samsung AFC Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device]
```

### 8. VOOC/WARP Trigger

**Purpose:** Trigger OnePlus VOOC/WARP Flash Charge

**How to Use:**
1. Navigate to Fast Charge → VOOC/WARP
2. Press CENTER to enter
3. Operation similar to QC2.0
4. Press BACK to exit

**Special Note:** Can use with "Soft DASH Cable" function if you don't have the special DASH cable

**Connection Diagram:**
```
[VOOC/WARP Charger] ---> [FNB58 USB-A Input] ---> [FNB58 Output] ---> [Device]
```

### 9. SuperVOOC 1.0/2.0 Trigger

**Purpose:** Trigger OnePlus SuperVOOC charging

**How to Use:**
1. Navigate to Fast Charge → SuperVOOC
2. Press CENTER to enter
3. Requires load >500mA connected to output
4. Only provides 10.5V
5. Press BACK to return (no other operations available)

**Connection Diagram:**
```
[SuperVOOC Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device >500mA load]
```

---

## Statistics Functions

Access: Application Page → Statistics → Press CENTER

### 1. Energy Statistics

**Purpose:** Track and record energy consumption and capacity over time

**Features:**
- 10 independent data groups (switchable)
- Each group tracks:
  - Capacity (Ah)
  - Energy (Wh)
  - Time elapsed
  - Average voltage
  - Average current

**How to Use:**
1. Navigate to Statistics → Energy Statistics
2. Use LEFT/RIGHT to select group (1-10)
3. Press CENTER to enter group
4. Data accumulates automatically while device is running
5. Press CENTER for options:
   - Switch group
   - Reset current group
   - Start/stop recording

**Connection Diagram:**
```
[Power Source] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device Under Test]

Note: Keep connected for duration of test. Data accumulates continuously.
```

### 2. Battery Capacity Calculation

**Purpose:** Calculate the actual capacity of batteries or power banks

**How to Use:**
1. Fully charge the battery/power bank
2. Connect: Battery → FNB58 → Load Device
3. Navigate to Statistics → Battery Capacity
4. Press CENTER to start recording
5. Let battery discharge completely while FNB58 monitors
6. Final capacity reading shows actual battery capacity

**Connection Diagram:**
```
[Battery/Power Bank] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Load Device]

Flow: Battery discharges through FNB58 to load
Measures: Total energy delivered by battery
```

### 3. Offline Recording

**Purpose:** Record data without PC connection for later analysis

**Features:**
- Records data to internal memory
- Can record multiple sessions
- Retrieve data via PC software later

**How to Use:**
1. Navigate to Statistics → Offline Recording
2. Press CENTER to enter
3. Options:
   - Start Offline Recording: Begin recording session
   - Clear Offline Recording: Delete all stored data
4. Data saves automatically
5. Connect to PC software later to download recorded data

**Connection Diagram:**
```
[Power Source] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device]

Note: Device operates normally while recording to internal memory
```

---

## Toolbox Functions

Access: Application Page → Toolbox → Press CENTER

### 1. Cable Resistance Detection

**Purpose:** Measure internal resistance of USB cables using differential voltage method

**Requirements:**
- Constant current load (0.5A - 1A recommended)
- Or device that draws stable current

**Step-by-Step Process:**

**Step 1: Calibrate (Record Reference)**
1. Navigate to Toolbox → Cable Resistance Detection
2. Connect: Charger → FNB58 Input → FNB58 Output → Constant Load
3. Adjust load to 0.5-1A steady current
4. Press CENTER to record reference voltage and current
5. Note the values shown under "Reference"

**Step 2: Measure Cable**
1. Disconnect everything
2. Connect: Charger → Cable Under Test → FNB58 Input → FNB58 Output → Same Load
3. Keep load current similar to reference (0.5-1A)
4. System automatically calculates cable resistance
5. Result displays in mΩ (milliohms)

**Connection Diagrams:**

**Calibration (Reference):**
```
[Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Constant Load 0.5-1A]

Press CENTER to record reference
```

**Cable Measurement:**
```
[Charger] ---> [Cable Under Test] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Same Load 0.5-1A]

System calculates resistance automatically
```

**Interpreting Results:**
- <100mΩ: Excellent cable
- 100-300mΩ: Good cable
- 300-500mΩ: Acceptable cable
- >500mΩ: Poor cable (will cause voltage drop and slow charging)
- >1000mΩ: Very poor cable (significant power loss)

### 2. PD Listener

**Purpose:** Monitor PD protocol negotiation between charger and device in real-time

**Requirements:**
- Turn PD Communication switch to ON
- External 5V power to PC port (Micro-USB)
- Two USB-C cables

**How to Use:**
1. Turn PD switch to ON
2. Connect 5V power supply to Micro-USB (PC) port
3. Navigate to Toolbox → PD Listener
4. Press CENTER to enter
5. Connect PD charger to Type-C IN port
6. Connect PD device to Type-C OUT port
7. Watch real-time PD negotiation messages

**Connection Diagram:**
```
                [5V Power Supply]
                        |
                        v
                [Micro-USB PC Port] (External power)
                        |
                   [FNB58 Body]
                        |
[PD Charger] ---> [Type-C IN Port]    [Type-C OUT Port] ---> [PD Device]
                        
                  PD Switch: ON

Monitor: Real-time PD protocol messages displayed on screen
```

**What You'll See:**
- Voltage and current requests
- PD message packets
- Negotiation success/failure
- Profile changes

**Troubleshooting:**
- If charger doesn't power up: Flip one USB-C cable 180° (CC pin orientation issue)

### 3. PD Converter

**Purpose:** Convert QC2.0 charger output to PD protocol for PD devices

**Use Case:** You have QC2.0-only charger but want to charge PD device

**Requirements:**
- QC2.0 charger (must support QC2.0, especially 20V mode)
- Turn PD Communication switch to ON

**How to Use:**
1. Turn PD switch to ON
2. Navigate to Toolbox → PD Converter
3. Press CENTER to enter
4. Connect QC2.0 charger to input
5. Press CENTER to select power window
6. Use LEFT/RIGHT to change maximum PD power
7. Important: Set to 5V when no device connected
8. Connect PD device to output
9. Press CENTER to confirm power setting

**Connection Diagram:**
```
[QC2.0 Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [PD Device]
                            ^
                            |
                    PD Switch: ON

FNB58 translates QC2.0 → PD protocol
```

**Warnings:**
- Not all QC2.0 chargers support 20V
- When device requests 20V, FNB58 checks if QC2.0 triggers successfully
- If voltage doesn't reach 20V, FNB58 cancels 20V and re-negotiates
- Always set to 5V before connecting devices to prevent damage

### 4. USB-C E-Marker Detection

**Purpose:** Read E-Marker chip data from USB-C cables

**What is E-Marker:**
E-Marker cables contain a chip in the USB-C connector that stores cable specifications:
- Maximum current capability (3A or 5A)
- USB data speed (USB 2.0, 3.1, etc.)
- Cable length
- Manufacturer information (VID/PID)

**Requirements:**
- USB-C cable with E-Marker chip (typically 60W+ cables or USB 3.x cables)
- Turn PD Communication switch to ON

**How to Use:**
1. Turn PD switch to ON
2. Navigate to Toolbox → E-Marker
3. Press CENTER to enter
4. Plug cable into Type-C output port
5. Cable information displays automatically

**Connection Diagram:**
```
[5V Power Supply] ---> [FNB58 Type-C Input] ---> [Cable Under Test] ---> [FNB58 Type-C Output]

PD Switch: ON
```

**Information Displayed:**
- Cable power rating (e.g., 100W, 60W)
- Maximum current (3A or 5A)
- USB data capability (USB 2.0, 3.1 Gen1, Gen2)
- Cable length
- Manufacturer VID (Vendor ID)
- Product ID
- Cable type (passive/active)

**If "No E-Marker" appears:**
- Cable doesn't have E-Marker chip
- Cable may be USB 2.0 only
- Cable may be rated <60W
- Not all cables require E-Markers

### 5. Read DASH Cable

**Purpose:** Read data from OnePlus DASH/VOOC cable's identification chip

**What is DASH Cable:**
OnePlus DASH cables have an extra contact in USB-A connector with identification chip for VOOC/WARP charging

**How to Use:**
1. Navigate to Toolbox → Read DASH Cable
2. Press CENTER to enter
3. Plug DASH cable's USB-A connector into FNB58 USB-A input port
4. Cable information displays

**Connection Diagram:**
```
[DASH Cable USB-A End] ---> [FNB58 USB-A Input Port]

Reads: Chip identification data
Shows: Cable specs and authentication info
```

**Information Shown:**
- Original data (raw hex)
- Parsed data (interpreted values)
- Cable authentication status

### 6. Soft DASH Cable

**Purpose:** Simulate DASH cable when you don't have one - enables VOOC/WARP charging with regular cable

**Use Case:** 
- You have VOOC/WARP charger
- Your phone needs DASH cable (USB-A to Type-C)
- You only have regular Type-C to Type-C cable

**How to Use:**
1. Navigate to Toolbox → Soft DASH Cable
2. Press CENTER to enable function
3. Connect: VOOC Charger → FNB58 USB-A Input → FNB58 Type-C Output → Type-C cable → Phone
4. FNB58 emulates the DASH cable chip
5. Phone should begin VOOC/WARP charging

**Connection Diagram:**
```
[VOOC/WARP Charger] ---> [FNB58 USB-A Input] ---> [FNB58 Type-C Output] ---> [Type-C Cable] ---> [Phone]
                                        ^
                                        |
                           FNB58 simulates DASH cable chip

Note: Charging power depends on Type-C cable quality
```

**Important Notes:**
- Not using official DASH cable means power depends on your Type-C cable
- High resistance cables will reduce charging power significantly
- Best used with quality low-resistance Type-C cables

### 7. Soft Apple 2.4A Accelerator

**Purpose:** Simulate Apple 2.4A charging by setting D+/D- pins to 2.7V

**Use Case:** Enable 5V @ 2.4A charging for Apple devices

**How to Use:**
1. Navigate to Toolbox → Soft Apple 2.4A
2. Press CENTER to enable
3. Connect Apple device
4. Device should charge at up to 2.4A (12W)

**Connection Diagram:**
```
[5V Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Apple Device]
                        ^
                        |
            D+/D- pins set to 2.7V

Enables: 5V @ 2.4A charging for Apple devices
```

**Boot Setting:**
- Can enable "Boot analog Apple 2.4A" in Settings
- When enabled, function activates automatically on boot
- Off by default

---

## Settings & Configuration

Access: Application Page → Settings → Press CENTER

### General Settings

**Display Brightness**
- Adjustable range: 1-100
- Use LEFT/RIGHT to adjust
- Press CENTER to confirm

**Language**
- Options: Chinese, English
- Use LEFT/RIGHT to select
- Press CENTER to confirm

**Auto Screen Rotation**
- Enable/Disable gravity sensor
- When enabled, screen rotates based on device orientation
- Use LEFT/RIGHT to toggle
- Press CENTER to confirm

**Screen Timeout**
- Set time before screen dims
- Options: 30s, 1min, 5min, Never
- Use LEFT/RIGHT to select
- Press CENTER to confirm

### Record Settings

**Data Recording Interval**
- Set how often data is recorded to memory
- Options: 0.1s, 0.5s, 1s, 2s, 5s, 10s
- Faster intervals = more data points but fills memory faster
- Use LEFT/RIGHT to select
- Press CENTER to confirm

**Waveform Recording**
- Enable/Disable automatic waveform recording
- Use LEFT/RIGHT to toggle
- Press CENTER to confirm

### Trigger Settings

**Auto Detection on Boot**
- Enable/Disable automatic fast charge protocol detection when device powers on
- Use LEFT/RIGHT to toggle
- Press CENTER to confirm

**Boot Analog Apple 2.4A**
- Enable/Disable Apple 2.4A function on boot
- Off by default
- Use LEFT/RIGHT to toggle
- Press CENTER to confirm

### System Settings

**Factory Reset**
- Reset all settings to factory defaults
- Clears all recorded data
- **WARNING: This cannot be undone**

**How to Perform Factory Reset:**
1. Navigate to Settings → System → Factory Reset
2. Press CENTER
3. Confirmation dialog appears
4. Press CENTER again to confirm
5. Device resets and restarts

### About

**Information Displayed:**
- Firmware version
- Hardware version
- Serial number
- Uptime (days, hours, minutes, seconds)
- Contact information

---

## Connection Diagrams for Each Function

### Basic Power Measurement

**Setup:** Measure charger output or device consumption

```
MEASURING CHARGER:
[Charger] ---> [FNB58 Input Port] ---> [FNB58 Output Port] ---> [Load Device]

MEASURING DEVICE CONSUMPTION:
[Power Source] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device Under Test]

Displays: Real-time voltage, current, power
```

### Fast Charge Protocol Testing

```
[Fast Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device or empty]

Functions:
- Automatic Detection: Leave output empty or light load
- Manual Trigger: Connect compatible device to output
- Protocol Testing: Output can be empty
```

### Cable Resistance Measurement

```
STEP 1 - CALIBRATION:
[Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Constant Load 0.5-1A]
Press CENTER to save reference

STEP 2 - MEASUREMENT:
[Charger] ---> [Cable to Test] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Same Load]
System calculates cable resistance
```

### E-Marker Reading

```
[5V Charger] ---> [FNB58 Type-C Input] ---> [Cable to Test] ---> [FNB58 Type-C Output]

PD Switch: ON

Note: Power must flow through the cable for E-marker interrogation to work
```

### PD Listener (Protocol Monitoring)

```
[5V Power] ---> [Micro-USB PC Port] (External power for FNB58)
                        |
                   [FNB58 Body]
                   /         \
[PD Charger] --> [Type-C IN]  [Type-C OUT] --> [PD Device]

PD Switch: ON
Displays: Real-time PD negotiation
```

### Battery Capacity Test

```
[Battery/Power Bank] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Load Device]

Process:
1. Fully charge battery first
2. Connect as shown
3. Start capacity measurement
4. Let battery discharge completely
5. Final reading shows actual capacity
```

### PD to QC Conversion

```
[QC2.0 Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [PD Device]

PD Switch: ON
FNB58 converts QC2.0 protocol to PD for device
```

### DASH Cable Simulation

```
[VOOC Charger USB-A] ---> [FNB58 USB-A Input] ---> [FNB58 Type-C Output] ---> [Type-C Cable] ---> [Phone]

Soft DASH enabled in Toolbox
FNB58 emulates DASH cable chip
```

### PC Connection for Logging

```
[USB Charger] ---> [FNB58 Input] ---> [FNB58 Output] ---> [Device Under Test]
                         |
                [Micro-USB PC Port] ---> [PC with FNB58 Software]

Functions:
- Real-time data logging
- Firmware updates
- Retrieve offline recordings
- Advanced analysis
```

---

## PC Software & Firmware Updates

### Installing PC Software

1. Download software from FNIRSI website (www.fnirsi.cn)
2. Extract ZIP file to any location (portable, no installation needed)
3. Run the executable file

**Software Features:**
- Real-time data logging at various sample rates
- Export data for analysis
- Trigger configuration
- Firmware updates
- Alarm settings
- Multiple device support

### Connecting to PC

**Method 1: Normal Operation with Logging**
1. Power FNB58 normally (through input/output ports)
2. Connect Micro-USB cable from PC port to computer
3. Software should auto-detect device
4. Begin logging

**Method 2: Bootloader Mode (Firmware Update)**
1. Ensure FNB58 is powered off
2. Hold down CENTER button
3. While holding, connect Micro-USB cable to PC port
4. Device enters bootloader mode
5. Software shows "Operating mode: bootloader"

### Updating Firmware

**Step 1: Enter Bootloader Mode**
- Method A: Hold CENTER button while plugging in Micro-USB to PC
- Method B: From software, click option to reboot to bootloader

**Step 2: Update Process**
1. Open FNB58 PC software
2. Click "System" tab
3. Verify "Operating mode: bootloader" is displayed
4. Click folder icon (Open File)
5. Navigate to firmware file (.ufn extension)
6. Select firmware file
7. Click upgrade icon (green recycle arrows)
8. Wait for upload to complete (do NOT disconnect)
9. Device automatically restarts when complete

**Firmware File Location:**
- Download from www.fnirsi.cn
- GitHub mirror: github.com/Rhomboid/fnb58-archive
- File extension: .ufn

**Important Notes:**
- Never disconnect during firmware update
- Ensure stable USB connection
- Keep device powered throughout update
- Update may take 2-5 minutes

### Data Logging

**Starting a Log:**
1. Connect FNB58 to PC
2. Set up your test (charger → FNB58 → device)
3. In software, select sample rate
4. Click "Start" to begin logging
5. Data saves to .cfn file (binary format)

**Sample Rates Available:**
- 10Hz (100ms interval)
- 5Hz (200ms interval)
- 1Hz (1 second interval)
- Slower rates (2s, 5s, 10s)

**Alarms:**
- Set voltage/current/power thresholds
- Software alerts when exceeded
- Useful for safety monitoring

---

## Specifications

### Electrical Specifications

**Voltage Measurement:**
- Range: 4V - 28V (with input power)
- Range: 0V - 28V (with external PC power)
- Resolution: 0.00001V (6-digit display)
- Accuracy: ±0.5% ±2 digits

**Current Measurement:**
- Range: 0A - 7A
- Resolution: 0.00001A (6-digit display)
- Accuracy: ±0.5% ±2 digits

**Power Calculation:**
- Range: 0W - 120W
- Resolution: 0.00001W (6-digit display)
- Calculated from V × I

**Capacity Measurement:**
- Range: 0 - 9999.99Ah
- Accumulates over time

**Energy Measurement:**
- Range: 0 - 9999.99Wh
- Accumulates over time

**Cable Resistance:**
- Range: 0 - 9999.9Ω
- Resolution: 0.1Ω
- Accuracy: ±1% ±5Ω
- Method: Differential voltage measurement

**Temperature:**
- Internal sensor
- Range: -10°C to 85°C
- Accuracy: ±2°C

### ADC Specifications

- Type: External 16-bit ADC
- Sampling rate: Up to 100Hz for continuous logging
- Low-speed waveform recording: 9 hours maximum

### Display

- Type: 2.0-inch TFT LCD
- Resolution: Full color
- Viewing angle: Ultra-wide
- Features: Auto-rotation via gravity sensor
- Brightness: Adjustable 1-100

### Physical Specifications

**Dimensions:**
- Approximately 70mm × 30mm × 15mm (with metal case)

**Weight:**
- Approximately 40g

**Case:**
- Metal construction (aluminum alloy)
- Four Torx screws for disassembly
- Good heat dissipation

**Ports:**
- 2× USB-C (input + output)
- 2× USB-A (input + output)  
- 1× Micro-USB (input + PC connection)

### Supported Protocols

**Fast Charging:**
- USB Power Delivery (PD) 2.0 / 3.0
- Qualcomm Quick Charge 2.0 / 3.0
- Huawei FCP (Fast Charge Protocol)
- Huawei SCP (SuperCharge Protocol)
- Samsung AFC (Adaptive Fast Charging)
- OnePlus VOOC / WARP / DASH
- OnePlus SuperVOOC 1.0 / 2.0
- MediaTek PE+ / PE+ 2.0
- Apple 2.4A

**Data/Cable:**
- USB-C E-Marker reading
- DASH cable identification

### Connectivity

**Bluetooth (Blue model only):**
- Android app support
- No iOS app available
- Real-time data viewing
- Remote triggering
- Alarm notifications

**PC Connection:**
- Micro-USB interface
- Windows software support
- Real-time logging
- Firmware updates
- Data export

### Operating Conditions

**Temperature:**
- Operating: 0°C to 40°C
- Storage: -20°C to 60°C

**Humidity:**
- <80% RH, non-condensing

### Power

**Device Power Consumption:**
- Typical: 50-100mW
- Display on: 100-200mW
- Powered by passthrough current or external 5V

**External Power Input:**
- Micro-USB (PC port)
- Input: 5V recommended (max 16V)
- Current: <100mA
- Used for: PD Listener, standalone operation

---

## Troubleshooting

### Power Issues

**Device Won't Turn On**

Problem: No display when connected

Solutions:
- Ensure current is flowing (need load device connected or charger providing power)
- Check that input and output ports are properly connected
- Try external power via Micro-USB (PC) port
- Verify charger is working
- Check USB cables are not damaged

**Device Keeps Restarting**

Problem: Random restarts during operation

Solutions:
- Normal during PD automatic detection (expected behavior)
- Check voltage not exceeding 28V
- Ensure good connections (not intermittent)
- Update to latest firmware
- Check for overheating

### Display Issues

**Screen is Blank but Device is On**

Solutions:
- Long press BACK button (backlight may be off)
- Check brightness setting in Settings → General
- Connect external power to Micro-USB port
- Device may need reset

**Screen Rotation Not Working**

Solutions:
- Enable auto-rotation in Settings → General
- Calibrate gravity sensor (firmware may have option)
- Update firmware

**Display Shows Wrong Values**

Solutions:
- Try factory reset: Settings → System → Factory Reset
- Update firmware
- Check connections (poor contact can cause erratic readings)

### Fast Charge Issues

**Automatic Detection Fails**

Problem: No protocols detected or wrong results

Solutions:
- Don't connect device to output during automatic detection
- Let test complete fully (may take 30-60 seconds)
- Some chargers may restart during PD testing (normal)
- Ensure charger supports the protocols being tested
- Try manual trigger for specific protocol

**PD Trigger Not Working**

Problem: Can't trigger PD voltages

Solutions:
- **CRITICAL:** Turn PD Communication switch to ON
- Use PD-compatible charger
- Use E-Marker cable for >60W (5A)
- After testing, turn PD switch back to OFF
- Some chargers require device connected to negotiate
- Try different USB-C cable

**QC2.0/3.0 Trigger Not Working**

Problem: Can't trigger QC voltages

Solutions:
- Ensure charger supports QC2.0 or QC3.0
- Use USB-A port or USB-A to C adapter
- Some chargers require minimum load (connect device)
- Verify charger with known QC device first

**Can't Trigger 20V**

Problem: 20V mode not working

Solutions:
- Must use QC2.0 charger that supports 20V
- Not all QC2.0 chargers support 20V
- Use FNB58's PD converter function if charger doesn't support 20V
- Check charger specifications

### E-Marker Issues

**"No E-Marker" Displayed**

Problem: Can't read cable E-Marker

Solutions:
- **CRITICAL:** Turn PD Communication switch to ON
- Not all cables have E-Markers (only 60W+, USB 3.x typically)
- Cable may be USB 2.0 only (<60W)
- Try providing external 5V power to Micro-USB (PC) port
- Cable may be damaged
- Try different cable to verify FNB58 works

**E-Marker Shows Wrong Info**

Solutions:
- Some cables have incorrectly programmed E-Markers
- Try reading with official manufacturer tool to compare
- Cable may be counterfeit

### Cable Resistance Measurement Issues

**Result Shows "NULL"**

Problem: Can't measure cable resistance

Solutions:
- Must record reference first (Step 1)
- Ensure using constant load or stable device consumption
- Load current should be 0.5-1A
- Current must be similar in both reference and measurement steps
- Press CENTER button to record reference
- Check all connections secure

**Result Seems Wrong**

Problem: Resistance reading is inconsistent

Solutions:
- Use more stable constant current load
- Ensure same current draw in both steps (reference vs measurement)
- Check all connections are tight (loose = extra resistance)
- Let device stabilize before recording reference
- Temperature can affect resistance (keep similar temp)

**Very High Resistance (>1000mΩ)**

Analysis:
- Cable is poor quality
- Cable may be damaged
- Cable is too long
- Using high gauge wire (thin conductors)
- Replace cable for better charging

### PD Listener Issues

**Can't See PD Messages**

Problem: PD Listener shows no data

Solutions:
- **CRITICAL:** Turn PD Communication switch to ON
- Connect 5V external power to Micro-USB (PC) port
- Use two USB-C cables (one charger side, one device side)
- Ensure PD device and charger (not just QC)
- Both cables must support PD
- Try flipping one USB-C cable 180° (CC pin issue)

**Charger Not Powering Up**

Solutions:
- Flip one USB-C cable connector 180°
- Some cables only have CC on one side
- Try different cables
- Ensure cables are PD-capable

### Bluetooth Issues (Blue Model Only)

**Can't Connect to App**

Solutions:
- Ensure Bluetooth model (blue finish)
- Android only - iOS not supported
- Enable Bluetooth on phone
- Download official FNB58 app
- Pair device in Bluetooth settings first
- Keep phone close to FNB58
- Try restarting both devices

**Connection Keeps Dropping**

Solutions:
- Reduce distance between phone and FNB58
- Close other Bluetooth apps
- Disable battery optimization for FNB58 app
- Update app to latest version
- Check for firmware update

### PC Software Issues

**Software Can't Detect Device**

Problem: PC doesn't recognize FNB58

Solutions:
- Check USB cable supports data (not charge-only)
- Try different Micro-USB cable
- Connect to Micro-USB port on FNB58 (not Type-C)
- Restart PC software
- Try different USB port on PC
- Check Windows Device Manager for USB device
- For bootloader: Hold CENTER button while connecting

**Can't Update Firmware**

Problem: Firmware update fails

Solutions:
- Enter bootloader mode properly:
  - Turn off FNB58
  - Hold CENTER button
  - Connect Micro-USB while holding
- Verify "Operating mode: bootloader" in software
- Use correct firmware file (.ufn extension)
- Ensure stable USB connection
- Don't disconnect during update
- Try different USB cable
- Try different USB port
- Download firmware again (may be corrupted)

**Data Logging Not Working**

Solutions:
- Ensure device is connected and powered
- Check sample rate setting
- Ensure sufficient disk space
- Try different save location
- Restart software

### General Issues

**Readings Seem Inaccurate**

Problem: Values don't match other meters

Solutions:
- Calibration may be needed (contact FNIRSI support)
- Compare with known good reference
- Check connections (resistance adds error)
- Temperature can affect readings
- Some variation normal between meters
- ±0.5% accuracy is within spec
- Update firmware

**Device Overheating**

Problem: FNB58 gets very hot

Solutions:
- Normal for high current (>5A) operation
- Ensure good ventilation
- Metal case designed for heat dissipation
- If >60°C internal temp, reduce current
- Let device cool between tests
- Don't exceed 7A rating

**Can't Enter Menu / Buttons Not Responding**

Solutions:
- Device may be in locked mode (during automatic detection)
- Unplug device to exit
- Long press BACK button
- Try factory reset
- Update firmware
- Check for physical button damage

**Factory Reset Needed**

When to perform factory reset:
- Settings corrupted
- Strange behavior
- After firmware update issues
- Before selling device

**How to Reset:**
1. Application Page → Settings → System → Factory Reset
2. Press CENTER twice to confirm
3. Wait for device to restart
4. All settings restored to defaults
5. All recorded data erased

### Error Messages

**"PD Switch OFF"**

Meaning: Trying to use PD function with switch off

Solution: Turn PD Communication switch to ON position

**"Need External Power"**

Meaning: Function requires 5V to Micro-USB port

Solution: Connect 5V power supply to Micro-USB (PC) port

**"Current Too Low"**

Meaning: For cable resistance or certain tests

Solution: Increase load to 0.5-1A range

**"Voltage Too High"**

Warning: Input voltage exceeds safe range

Solution: 
- Disconnect immediately
- Check charger output
- Maximum 28V for FNB58
- Do not exceed specifications

### Getting Help

**Official Support:**
- Website: www.fnirsi.cn
- Email: service@fnirsi.com or info@fnirsi.com
- Response time: Within 24 hours

**Warranty:**
- 2-year warranty (purchased from fnirsi.com)
- 30-day return/refund guarantee
- Lifetime technical support

**Resources:**
- User manual: Available on website
- Firmware updates: www.fnirsi.cn
- GitHub mirror: github.com/Rhomboid/fnb58-archive
- Community: Various tech forums and review sites

**Before Contacting Support:**
- Note firmware version (Settings → About)
- Note hardware version
- Describe problem in detail
- Include connection setup
- Try firmware update
- Try factory reset

---

## Safety Summary

### DO:
✅ Keep PD switch OFF when not using PD functions  
✅ Turn PD switch to ON only for: PD Trigger, PD Listener, PD Converter, E-Marker  
✅ Turn PD switch back to OFF after using these functions  
✅ Use only one input/output pair at a time  
✅ Provide external 5V power for PD Listener  
✅ Keep voltage under 28V at monitoring ports  
✅ Keep voltage under 16V at PC port  
✅ Update firmware regularly  
✅ Use quality USB cables  
✅ Allow proper ventilation during use  

### DON'T:
❌ Connect to power sources >28V at monitoring ports  
❌ Connect to power sources >16V at PC port  
❌ Use multiple input/output pairs simultaneously  
❌ Connect equipment to unused ports when one pair is active  
❌ Leave PD switch ON when not needed  
❌ Charge phones immediately after high-voltage trigger without verification  
❌ Exceed 7A current rating  
❌ Operate in extreme temperatures  
❌ Disconnect during firmware update  
❌ Use in wet or humid conditions  

---

## Quick Reference Card

### Button Functions:
- **LEFT:** Previous, Decrease
- **RIGHT:** Next, Increase  
- **CENTER:** Confirm, Enter, Pause
- **BACK:** Cancel, Return
- **BACK (Long):** Backlight toggle

### PD Switch Positions:
- **OFF:** Normal monitoring, QC functions, general use
- **ON:** PD Trigger, PD Listener, PD Converter, E-Marker reading

### Common Connections:

**Basic Monitoring:**
```
[Source] → [FNB58 In] → [FNB58 Out] → [Load]
```

**Cable Test:**
```
[Source] → [Cable] → [FNB58 In] → [FNB58 Out] → [Load 0.5-1A]
```

**E-Marker:**
```
[5V Source] → [FNB58 In] → [Cable] → [FNB58 Out]
PD Switch: ON
```

**PD Listener:**
```
[5V] → [Micro-USB PC Port]
[PD Charger] → [Type-C In] → [Type-C Out] → [PD Device]
PD Switch: ON
```

---

## Appendix: Understanding USB Charging Protocols

### USB Power Delivery (PD)

**What it is:** Modern universal fast charging standard

**Voltages:** 5V, 9V, 12V, 15V, 20V (PPS: 3.3-21V)

**Current:** Up to 5A (requires E-Marker cable)

**Power:** Up to 100W (20V × 5A)

**How it works:** Device and charger negotiate best voltage/current via CC pin

**Common uses:** Laptops, tablets, high-end phones

### Qualcomm Quick Charge

**QC2.0:**
- Voltages: 5V, 9V, 12V, 20V (fixed)
- Current: Up to 3A
- Power: Up to 60W
- Uses: Older Android phones

**QC3.0:**
- Voltages: 3.6V - 20V (200mV steps)
- Current: Up to 3A
- Finer voltage control than QC2.0
- Uses: Mid-range Android phones

**QC4/4+:**
- Integrated with PD
- Uses PPS (Programmable Power Supply)
- Better efficiency

### Huawei Protocols

**FCP (Fast Charge Protocol):**
- Voltages: 5V, 9V
- Current: 2A
- Power: 18W max
- Uses: Older Huawei phones

**SCP (SuperCharge Protocol):**
- Voltages: 5V, 9V, 10V
- Current: Up to 4A
- Power: Up to 40W
- Low-voltage high-current approach
- Uses: Newer Huawei/Honor phones

### OnePlus Protocols

**VOOC/DASH/WARP:**
- Voltage: 5V (low voltage)
- Current: 4-6A (high current)
- Power: 20-30W
- Requires special cable with extra contact
- Heat stays in charger, not phone
- Uses: OnePlus phones

**SuperVOOC:**
- Voltage: 10V (version 1.0) or 5V (version 2.0)
- Current: Up to 6.5A
- Power: 50-65W
- Dual-cell battery architecture
- Uses: OnePlus flagship phones

### Samsung AFC

**AFC (Adaptive Fast Charging):**
- Voltages: 5V, 9V
- Current: 1.67A - 2A
- Power: Up to 18W
- Uses: Samsung Galaxy phones
- Similar to QC2.0 but Samsung's implementation

### Apple Charging

**Standard USB:**
- 5V @ 1A = 5W

**iPad Charging:**
- 5V @ 2.4A = 12W
- Requires D+/D- at 2.7V

**USB-PD:**
- Modern iPhones/iPads use PD
- 20W, 30W, 65W chargers
- Uses USB-C to Lightning cable

### Battery Charging (BC1.2)

**Standard USB-PD precursor:**
- DCP: 5V @ 1.5A
- CDP: 5V @ 1.5A (with data)
- Older standard, widely supported

### E-Marker Cables

**Purpose:** Store cable capabilities

**Required for:**
- USB-C cables rated >60W (5A)
- USB-C cables with USB 3.1+ data
- Cables >1 meter length (sometimes)

**Information stored:**
- Maximum current (3A or 5A)
- Maximum voltage
- USB data speed
- Cable length
- Manufacturer ID
- Cable type (passive/active)

**Not required for:**
- Basic USB 2.0 cables
- 60W and under cables (3A max)
- Short cables

---

**End of Manual**

For latest updates, firmware, and support:
- Website: www.fnirsi.cn
- Email: service@fnirsi.com
- GitHub Mirror: github.com/Rhomboid/fnb58-archive

Document Version: 1.0
Created: 2024
Device: FNIRSI FNB58 USB Fast Charge Tester

---

**Note:** This manual was compiled from official FNIRSI documentation, user guides, and community resources. While comprehensive, always refer to the latest official documentation from FNIRSI for the most up-to-date information, especially regarding firmware updates and new features.