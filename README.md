Developed with: CADe_SIMU v.4.0 || 
Project Type: Electrical & Control System Simulation || 
Date: October 26, 2023 || 
Author: Ayitey Martin / University of Energy and Natural Resources ||

1. Executive Summary:

This report details the comprehensive design, development, and simulation of a Four-Way Traffic Light Control System using CADe_SIMU software. The project successfully emulates the standard operational logic of an urban intersection by implementing a conflict-free, time-sequenced control circuit. The system utilizes electromechanical components such as timing relays, auxiliary relays, and indicator lamps to manage traffic flow between the North-South and East-West corridors. The simulation validates the system's safety, reliability, and potential for adaptation into more complex smart traffic management solutions.

3. Introduction:
Traffic congestion and accidents at intersections remain a significant challenge in urban infrastructure. A robust traffic light control system is fundamental to ensuring pedestrian safety and vehicular flow efficiency. This project addresses this need by creating a scalable and reliable control model.

CADe_SIMU was selected as the primary development environment due to its robust library of electrical components and its ability to simulate real-time sequential logic without the need for physical hardware prototyping. The project transitions from a theoretical understanding of sequential logic to a practical, verifiable simulation model.

3. Project Objectives:
The primary goals of this development project are:

Design: To construct a comprehensive electrical schematic that accurately represents a four-way intersection control system.

Simulation: To execute the simulation to verify the predetermined Red, Yellow, and Green light sequences for conflicting traffic directions.

Application: To demonstrate the application of core electrical engineering principles—specifically, Sequential Control and Time-Delay Logic—in solving real-world logistical problems.

Validation: To ensure zero overlap in conflicting signal directions (North-South vs. East-West), thereby proving the system's operational safety.

4. Tools & Technologies:
   
4.1 Software:
CADe_SIMU: An advanced electrical circuit design and simulation tool capable of representing complex control circuits using ladder logic and relay schematics.

4.2 Hardware Components (Simulated):
The system is constructed using the following virtual components:

Component	Function:
Timers (ON-Delay)	Set the duration for Green and Yellow light phases.
Electromagnetic Relays	Act as logical switches to alternate power between different traffic directions.
Indicator Lamps	Visually represent the Red, Yellow, and Green lights for each direction.
Push Buttons/Switches	Initiate the simulation sequence.
Power Supply	Provides the necessary voltage to the control circuit.

4.3 Methodology:
The project employs a Sequential Control Logic methodology, where the activation of one timer triggers a relay, which in turn activates the next timer, ensuring a cascading and conflict-free sequence.


5. System Architecture & Operational Logic
5.1 Phase Sequence:
The system operates on a standard 4-phase cycle to manage traffic flow effectively:

Phase 1 (North-South Green):

North-South = Green; East-West = Red.

Phase 2 (North-South Yellow):

North-South = Yellow; East-West = Red.

Phase 3 (East-West Green):

North-South = Red; East-West = Green.

Phase 4 (East-West Yellow):

North-South = Red; East-West = Yellow.

5.2 Control Logic Diagram:
The flow of control relies on an interlocking mechanism:

The Green Timer (NS) energizes the North-South Relay (Green).

When the timer expires, it de-energizes the Green relay and powers the Yellow Timer (NS) .

The Yellow Timer powers the North-South Yellow Relay.

Upon expiration, the Yellow Timer resets the system, allowing the East-West Relay to activate.

This interlocking ensures that the East-West circuit cannot be energized while the North-South circuit is active.


6. Simulation & Results:
6.1 Visual Representation
The CADe_SIMU interface provides a live visual feedback of the circuit. Lamps turn Red, Yellow, and Green according to the timing sequence, while the status of timers and relays is displayed numerically.

6.2 Results Analysis
Cycle Completion: The simulation runs continuously without halting errors, completing all four phases in a loop.

Safety: Successfully implemented an "Interlock" mechanism. The Red lights were always active for the opposing direction when a Green light was active, confirming a 100% conflict-free scenario.

Timing Adjustability: The ON-Delay timer settings were easily adjusted from 1 second (simulation) to 10 seconds (demonstration), showcasing the system's flexibility for different traffic densities.

6.3 Simulation Snapshot: https://drive.google.com/file/d/1TKAUFJ8wGY_ujFaICz1382fZu_exlYfX/view?usp=sharing



