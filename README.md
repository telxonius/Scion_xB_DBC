2010 Scion xB CAN Bus Database (DBC)
This repository contains a Controller Area Network (CAN) database file for the 2010 Scion xB (Second Generation)
with a 4-speed automatic transmission. This was a personal research project to map the vehicle's internal communication for data logging and hobbyist car hacking.
Project Overview
The goal was to reverse-engineer and document the CAN bus signals for a 2010 Scion xB
. Data was captured using a manual sniffing process and verified against real-time vehicle behavior.

    Vehicle: 2010 Scion xB
    Transmission: 4-Speed Automatic
    Capture Tool: SavvyCAN and "jhoinrch" RH02 Elite
    Protocol: CAN 2.0A (11-bit identifiers) at 500kbps

Mapped Signals
The included .dbc file contains several key signals found on the main bus, including:

    Engine: RPM, Engine Coolant Temp.
    Transmission: Shift Position (P/R/N/D).
    Chassis: Wheel Speeds (all 4 wheels), Brake Pedal Status, Steering Wheel Angle.
    Dashboard: Speedometer, Odometer, Indicators. and others

Files

    scion_xb_2010.dbc: The database file used to decode raw CAN messages.
    

How to Use

    Connect to the vehicle's OBD-II port using a CAN interface (e.g., Macchina J2534, Lawicel, or Arduino with CAN shield).
    Import the scion_xb_2010.dbc into SavvyCAN, Kayak, or Busmaster.
    The raw hex data will now be readable as human-friendly values (e.g., "750 RPM" instead of 0x02 EE).

Disclaimer
This project is for educational and research purposes only. Interfacing with a vehicle's CAN bus can be dangerous if you write data to the bus (spoofing). Use at your own risk. The author is not responsible for any damage caused to your vehicle.
