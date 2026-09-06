## Titan-Racing-Baja-SAE (2026-2027)
Titan Racing Baja SAE is an engineering club for students to design, build and race a custom off-road vehicle for the annual collegiate competition. Designing and building a car requires us to apply engineering problems to the real world. We gain invaluable skills in design, manufacturing, and project management that prepare us for professional careers. At **CSUF**, our Baja SAE team consists of 14 members, and our goal is to compete in the BAJA SAE competition that is in **Tucson, Arizona** in **May 2027**. We are divided into four subteams:

- Chassis / Ergonomics 
- Drivetrain  
- Suspension  
- Vehicle Dynamics / Data Acquisition

---

## Vehicle Dynamics & Data Acquisition
For the **Vehicle Dynamics / Data Acquisition (VD/DAQ)** subteam, the focus is heavily on the electrical, sensor data, and data analysis side of work on the car.

We currently implemented **8 sensors** on the Baja car, all connected to an Teensy 4.1-based DAQ system to record performance data during testing and competition runs. Our goal for this year is to add more critical sensors which will bring the total to **12 sensors**.

The current system logs:
- Vehicle velocity
- Distance traveled  
- Time
- Engine RPM (Primary)
- CVT RPM (Secondary)
- CVT belt temperature
- 6-axis motion data   
- Brake pressure bias
- Vehicle position (GPS)  

All sensor data is routed through a **Teensy 4.1**, allowing each run to be logged directly to an microSD card. The recorded data is then processed and analyzed in **MATLAB** to evaluate vehicle performance, CVT behavior, braking balance, and driver inputs.

Live transmission of recorded data is available to the pit crew through the usage of a XBee RF Module and supporting components.
