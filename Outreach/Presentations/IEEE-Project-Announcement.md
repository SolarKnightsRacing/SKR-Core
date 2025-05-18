
Could help with: brainstorming, design, building, or troubleshooting
**1. Battery pack**
We must design and build an approximately 5kWh lithium-based energy storage system.
The design is summarized below:  
  - Storage bank
    - Strings
      - Modules
       - Cells 
  - Battery Management System (BMS) 
  - HV Contactors 
  - HV Fuse 
  - Bus bars and HV wiring
  - Ventilation system

Skills: Power electronics  

**2. Battery Protection System (BPS)**
  The BPS, not to be confused with the Battery Management System (BMS), is a required component for vehicles that Race in the American Solar Challenge. The BPS is the primary system which applies "Active Protection" for the vehicle. Measurements are constantly monitored from sources such as the CAN bus and actions are taken to automatically put the car in a safe state by opening the main power contactors. (ASC 2026 Regulation 8.3.A.5)

Skills: PCB design, CAN protocol

**3. Power Control Modules**
We plan to distribute our low-voltage power control to individual Power Control Modules throughout the vehicle. Functions that are usually handled by a singular Power Distributuion Module like: power switching, over/under current protection, over/under voltage protection, and power tracking, will be delegated to one board per switched item. i.e. One PCM for the left headlight and another for the right headlight. These modules will be connected to the main CAN bus as their primary form of control.

Skills: PCB Design, CAN protocol, Power electronics

**4. Driver Control Panel GUI**
  Despite the apprehension that most of us share about touch-screen controls in cars, most of the non-critical driver controls will only be available through the Driver Control Panel via a Graphical User Interface. The driver control panel will be running a Real-Time Operating System (RTOS) to guarantee controls will be predictable and reliable.
 
Skills:  Embedded programming,  Rust,  OxidOS, tock, or some other RTOS,  CAN protocol,  UI Design

Contact info:
