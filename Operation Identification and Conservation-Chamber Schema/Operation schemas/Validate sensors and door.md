| Field | Specification |
|---|---|
| Description | Performs startup and recovery checks for essential sensors and door status. |
| Inputs | Sensor self-test results, door switch status, sensor diagnostic data. |
| Outputs | Sensor-health result and door-safety result. |
| Reads | Temperature, humidity, vibration, power, and door sensors. |
| Changes | Sensor-validation status and conservation eligibility. |
| Sends/Alerts | Raises an alert if any essential sensor fails or the door is not closed. |
| Assumes (precondition) | The chamber controller has power sufficient to execute the checks. |
| Result (postcondition) | Conservation eligibility is true only when all essential sensors pass and the door is confirmed closed. |
