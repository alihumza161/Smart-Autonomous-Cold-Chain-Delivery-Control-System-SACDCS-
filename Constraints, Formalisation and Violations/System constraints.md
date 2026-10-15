| Constraint ID | Constraint in simple English | Why it is necessary |
| --- | --- | --- |
| CON-01 | The robot must not enter the crossing unless the barrier is open, no train is approaching, and the crossing is confirmed clear. | Prevents train–robot collisions. |
| CON-02 | If a train is present or approaching, the barrier must not be open. | Prevents vehicles entering a hazardous crossing. |
| CON-03 | The barrier must remain closed while a train is passing through the crossing. | Prevents premature opening. |
| CON-04 | The barrier may open only after the crossing is confirmed clear and the relevant sensors are healthy. | Prevents unsafe barrier release. |
| CON-05 | The robot must not enter `DELIVERING` unless it has reached the assigned destination and all delivery guards pass. | Prevents premature or unauthorised delivery. |
| CON-06 | When critical battery conditions make continued delivery unsafe, the robot must abandon delivery and follow the defined safe-return or Safe Mode policy. | Prevents battery depletion during an unsafe manoeuvre. |
| CON-07 | The active batch profile must match the batch physically stored in the chamber. | Prevents use of incorrect environmental limits. |
| CON-08 | Conservation must not be active unless the door is confirmed closed and essential sensors are healthy. | Prevents uncontrolled environmental exposure. |
| CON-09 | Environmental recovery must not be declared successful until measured temperature and humidity are within the active batch limits. | Prevents false recovery declarations and medicine spoilage. |
| CON-10 | The robot must not perform delivery release while the chamber door is open or a protection response is active. | Prevents unsafe medicine handling. |
| CON-11 | A critical thermal or battery condition must trigger Safe Mode within 3 seconds of detection. | Enforces the CR-01 safety deadline. |
| CON-12 | The system must support at least 20 simultaneously connected robots without mixing their command, telemetry, or event records. | Enforces the CR-02 capacity requirement and session isolation. |
| CON-13 | The robot must not enter the crossing when railway status is unknown, invalid, stale, or contradictory. | Ensures uncertainty is treated as unsafe. |
| CON-14 | On loss of crossing-system communication, the robot must remain outside the crossing until valid crossing permission is re-established. | Prevents entry using outdated railway information. |
| CON-15 | A command must not execute unless the operator is authenticated and authorised for that command. | Prevents unauthorised robot control. |
| CON-16 | Accepted commands and safety-related events must be recorded with robot identity, event time, and outcome. | Supports accountability, investigation, and recovery. |
