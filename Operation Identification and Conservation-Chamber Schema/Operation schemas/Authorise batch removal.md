| Field | Specification |
|---|---|
| Description | Determines whether a batch can be removed without violating chamber safety requirements. |
| Inputs | Removal request, chamber-safety status, protection-response status, door status. |
| Outputs | Removal permission or rejection. |
| Reads | Sensor-health status, environmental readings, protection-mode status, batch identity. |
| Changes | Removal authorisation and associated audit record. |
| Sends/Alerts | Reports approval or rejection and records the decision. |
| Assumes (precondition) | A batch is present and its identity is known. |
| Result (postcondition) | Removal is permitted only when the chamber is safe and no protection response is active; otherwise removal is denied. |
