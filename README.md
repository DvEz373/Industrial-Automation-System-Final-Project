# Factory Simulation Project with Factory IO and Schneider Machine Expert Basic

## Overview
This project demonstrates a simulated factory automation system using **Factory IO** for virtual industrial environments and **Schneider Machine Expert Basic** for ladder programming. The goal is to implement and test various automation sequences using a combination of sensors, timers, and actuators in a digital twin setup.

## Project Components
- **Factory IO**: Virtual simulation environment to represent a realistic factory layout.
- **Schneider Machine Expert Basic**: Software used for programming the control logic using ladder diagrams.
- **Digital Input/Output (I/O) List**: Comprehensive list of inputs and outputs managed by the control logic, enabling sensor data reading and actuator control.
- **Timers**: Digital timers used for controlling process delays and scheduling operations.

## I/O List

| **Name**          | **Internal Address** | **Pin Address** | **Type** | **I/O Type**      | **Read/Write** |
|-------------------|----------------------|----------------|----------|------------------|----------------|
| RUNNING           | %M0                  | DI-1           | Digital  | Digital Input     | Read           |
| RETRO_1           | %M2                  | DI-2           | Digital  | Digital Input     | Read           |
| RETRO_2           | %M4                  | DI-3           | Digital  | Digital Input     | Read           |
| RETRO_5           | %M6                  | DI-4           | Digital  | Digital Input     | Read           |
| RETRO_6           | %M8                  | DI-5           | Digital  | Digital Input     | Read           |
| RETRO_9           | %M10                 | DI-6           | Digital  | Digital Input     | Read           |
| RETRO_10          | %M12                 | DI-7           | Digital  | Digital Input     | Read           |
| DIFFUSE_1         | %M13                 | DI-8           | Digital  | Digital Input     | Read           |
| DIFFUSE_2         | %M16                 | DI-11          | Digital  | Digital Input     | Read           |
| CLAMPED_1         | %M15                 | DI-10          | Digital  | Digital Input     | Write          |
| VISION_BLUE       | %M22                 | DI-17          | Digital  | Digital Input     | Read           |
| MEMORI_2          | %M103                | DI-20          | Digital  | Digital Input     | Read           |
| MC_START_1        | %M201                | DI-37          | Digital  | Digital Input     | Write          |
| CONV_2_6          | %M206                | DI-42          | Digital  | Digital Input     | Write          |
| GRAB_3            | %M219                | DI-55          | Digital  | Digital Input     | Write          |
| MOVE_X_3          | %M224                | DI-60          | Digital  | Digital Input     | Write          |
| CONV_4_10         | %M251                | DI-81          | Digital  | Digital Input     | Write          |
| PIVOT_TURN_1      | %M254                | DI-84          | Digital  | Digital Input     | Write          |
| TIMER_1           | %TM0                 | T-1            | Timer    | Digital Input     | -              |
| TIMER_2           | %TM1                 | T-2            | Timer    | Digital Input     | -              |

*For a full list of inputs and outputs, refer to the attached I/O table.*

## System Logic
The factory simulation consists of multiple conveyor belts, robotic arms, and sensor networks, which interact through the control logic designed in the ladder programming language. The control sequence initiates when the **RUNNING** signal is active. Sensors such as **RETRO** and **DIFFUSE** determine the state of parts moving on the conveyors, while **CLAMPED** signals indicate gripping mechanisms.

Timers are used to implement timed actions, such as conveyor movement and material handling. 

## Key Features
- **Factory IO Simulation**: 3D visualization of the factory layout.
- **Ladder Logic**: Automation control logic developed using Schneider Machine Expert Basic.
- **Real-Time Control**: Timers and sensors control the flow of operations.
- **Digital I/O Handling**: Input/output management with a focus on real-time process automation.

## Setup Instructions
1. Install **Factory IO** and create a virtual factory layout with conveyor belts, sensors, and actuators.
2. Open **Schneider Machine Expert Basic** and load the ladder logic program.
3. Assign I/O addresses based on the table provided above.
4. Run the simulation in **Factory IO** and verify the correct interaction between sensors, conveyors, and timers.

## Conclusion
This project demonstrates the integration of **Factory IO** and **Schneider Machine Expert Basic** in automating industrial processes. The system simulates real-world factory operations with a high level of control, making it a valuable tool for learning and testing industrial automation strategies.
