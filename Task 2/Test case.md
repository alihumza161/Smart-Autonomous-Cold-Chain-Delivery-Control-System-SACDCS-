
| Test ID | Test Scenario | Expected Result | Risk |
|---|---|---|---|
| TC-01 | Submit a valid delivery request while the robot is `IDLE`. | Request is validated, accepted, and logged; robot enters `NAVIGATING`. | High |
| TC-02 | Submit a delivery request with a missing destination or invalid batch ID. | Request is rejected; robot remains `IDLE`; rejection is logged. | High |
| TC-03 | Detect an obstacle while navigating. | Navigation is suspended; robot enters `AVOIDING_OBSTACLE`. | Critical |
| TC-04 | Confirm that an obstacle has been cleared. | Robot resumes `NAVIGATING` only after route-safety confirmation. | Critical |
| TC-05 | Reach the destination with a valid delivery authorisation and safe chamber. | Robot enters `DELIVERING`; delivery outcome is reported and logged. | Critical |
| TC-06 | Inject a critical battery or chamber-temperature condition. | Safe Mode is entered within 3 seconds; unsafe delivery actions are inhibited. | Critical |
| TC-07 | Send a command without authentication. | Command is rejected and logged; no robot action occurs. | Critical |
| TC-08 | Send a command from an authenticated operator without the required role permission. | Command is rejected and logged; no robot action occurs. | Critical |
| TC-09 | Connect 20 robots simultaneously and generate telemetry traffic. | All 20 remain correctly associated with command and telemetry sessions. | High |
| TC-10 | Disconnect the communication link during navigation. | Robot follows the defined communication-loss safety policy; stale commands are not executed. | Critical |
| TC-11 | Cause temperature to exceed the configured chamber limit. | Correction is activated; sensor readings determine whether recovery succeeded. | Critical |
| TC-12 | Attempt railway-crossing entry while the barrier is closed or train presence is detected. | Entry is blocked; the event and operator alert are recorded. | Critical |
| TC-13 | Open the chamber door during conservation. | Conservation is suspended; resumption requires safety verification. | Critical |
| TC-14 | Inject railway sensor failure or stale crossing data. | Crossing is treated as unsafe; robot entry is prevented and an alert is generated. | Critical |
ceptance, execution, and final completion. A timeout alone must not cause the same command to be executed again.
