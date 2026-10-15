| Field | Specification |
|---|---|
| Description | Maintains essential chamber monitoring through emergency power when available; otherwise performs a safe shutdown. |
| Inputs | Main-power status, emergency-power availability, battery status. |
| Outputs | Power-transition result and shutdown status. |
| Reads | Power sensors, backup-power status, controller health. |
| Changes | Power source, operating permissions, shutdown status. |
| Sends/Alerts | Records the power-loss event and alerts Mission Control when communication remains available. |
| Assumes (precondition) | Power monitoring is active and the controller can detect the power condition. |
| Result (postcondition) | Emergency power is selected when available; otherwise the incident is recorded and the chamber performs its defined safe shutdown. |
