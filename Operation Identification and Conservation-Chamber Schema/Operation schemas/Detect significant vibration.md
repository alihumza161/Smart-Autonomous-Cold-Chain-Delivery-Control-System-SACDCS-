| Field | Specification |
|---|---|
| Description | Detects excessive vibration and suspends activities that could damage the medicine or compromise delivery. |
| Inputs | Measured vibration, configured threshold, stabilisation period. |
| Outputs | Vibration status and stabilisation result. |
| Reads | Vibration sensor, timer, current chamber activity. |
| Changes | Risky-activity permission and vibration-event status. |
| Sends/Alerts | Notifies the controller and operator when vibration exceeds the threshold. |
| Assumes (precondition) | The vibration sensor has passed its self-check. |
| Result (postcondition) | Risky activities remain suspended until vibration stays below the threshold continuously for the required stabilisation period. |
