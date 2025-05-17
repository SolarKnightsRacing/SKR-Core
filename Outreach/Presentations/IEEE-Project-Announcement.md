
Could help with: brainstorming, design, building, or troubleshooting
**1. Battery pack**
We must design and build an approximately 5kWh lithium-based energy storage system.
  
  - Storage bank
    - Strings
      - Modules
       - Cells COTS
  - Battery Management System (BMS) COTS
  - HV Contactors COTS
  - HV Fuse COTS
  - Bus bars and HV wiring
  - Ventilation system

 - Skills
	 - Power electronics

**2. Battery Protection System (BPS)**
  The BPS (not to be confused with the BMS) is a required component for vehicles that Race in the American Solar Challenge.
 ```
8.3.A.5 Active Protection: System in which measurements are constantly monitored and where actions are taken immediately without operator intervention to open the Main Power Contactors should a battery Protection Fault occur. Any protection faults will latch such that a manual clearing process is required by the driver with the vehicle not in motion and only after faults have been verified clear by the protection system.
```

- Skills
	- PCB design
	- CAN protocol

**3. Power Control Modules**
We plan to divide our low-voltage power control to individual PCM boards throughout the vehicle. Functions that are usually handled by a singular PDM like: power switching, over/under current/voltage protection, and power tracking telemetry, will be delegated to one board per switched item. i.e. One PCM for the left headlight and another PCM for the right headlight.

- Skills
	- PCB Design
	- CAN protocol
	- Power electronics

**4. Driver Control Panel GUI**
  Despite the apprehension about touch-screen controls for cars, most of the non-critical driver controls will only be available through the Driver Control Panel via a Graphical User Interface (GUI). The driver control panel will be running a Real-Time Operating System (RTOS) to guarantee controls will be predictable and reliable.
 
 - Skills
	 - Embedded programming
	 - Rust
	 - OxidOS, tock, or some other RTOS
	 - CAN protocol
	 - UI Design
