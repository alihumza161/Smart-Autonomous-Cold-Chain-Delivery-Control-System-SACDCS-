| Field | Specification |
|---|---|
| Description | Suspends normal conservation when the door opens during active conservation. |
| Inputs | Door-open event, current chamber state, environmental readings. |
| Outputs | Conservation-suspension status and safety-check result. |
| Reads | Door sensor, temperature/humidity sensors, sensor-health data, active batch profile. |
| Changes | Conservation eligibility, activity permissions, and recovery status. |
| Sends/Alerts | Generates a door-open alert and records the incident. |
| Assumes (precondition) | The chamber is powered and door-status monitoring is available. |
| Result (postcondition) | Conservation is suspended while the door is open and remains suspended after closure until the required environmental and sensor checks pass. |
