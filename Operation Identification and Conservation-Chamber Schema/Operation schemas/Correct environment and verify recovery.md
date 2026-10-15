| Field | Specification |
|---|---|
| Description | Activates temperature or humidity correction and verifies the resulting environmental conditions. |
| Inputs | Measured temperature/humidity, batch limits, recovery deadline, actuator status. |
| Outputs | Correction result, verified environmental readings, recovery status. |
| Reads | Temperature and humidity sensors, batch profile, actuator feedback, timer. |
| Changes | Correction actuator commands and recovery status. |
| Sends/Alerts | Reports recovery success or raises a protection-mode alert if correction fails. |
| Assumes (precondition) | A valid batch profile exists, the sensors are healthy, and correction hardware is available. |
| Result (postcondition) | Recovery is declared successful only if fresh sensor readings are within the permitted limits; otherwise the chamber enters protection mode when the recovery deadline expires. |
