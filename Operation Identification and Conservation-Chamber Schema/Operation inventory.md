| Operation ID | Operation name | Purpose |
|---|---|---|
| OP-01 | Validate delivery request | Checks request format, destination, batch, and current mission eligibility. |
| OP-02 | Plan and start route | Calculates or selects a permitted route and starts navigation. |
| OP-03 | Detect and handle obstacle | Detects a route obstacle and initiates a safe avoidance manoeuvre. |
| OP-04 | Verify route clearance | Confirms the obstacle has cleared and the intended path is safe. |
| OP-05 | Authorise batch release | Verifies destination, batch identity, door status, and safety conditions before release. |
| OP-06 | Evaluate battery and return | Evaluates available energy and initiates safe return when required. |
| OP-07 | Load batch profile | Loads the medicine identity and permitted temperature/humidity limits. |
| OP-08 | Validate sensors and door | Checks essential sensor health and whether the chamber door is closed. |
| OP-09 | Correct environment and verify recovery | Corrects temperature/humidity and confirms recovery using measured values. |
| OP-10 | Authenticate and authorise command | Validates the operator identity, role, permissions, and command scope. |
| OP-11 | Execute emergency response | Inhibits hazardous activities and applies the configured safety response. |
| OP-12 | Manage robot sessions | Establishes and maintains multiple robot communication sessions. |
| OP-13 | Validate crossing permission | Checks crossing status and authorisation before a robot enters. |
| OP-14 | Validate crossing sensor data | Checks the validity, freshness, and consistency of railway interface data. |
| OP-15 | Acknowledge and report command status | Reports whether a command was received, accepted, executed, or rejected. |
| OP-16 | Record and recover event logs | Persists event records and restores them after restart. |
| OP-17 | Detect significant vibration | Evaluates vibration against the configured threshold and stabilisation interval. |
| OP-18 | Respond to door opening | Suspends conservation when the chamber door opens and initiates safety checks. |
| OP-19 | Manage power-loss response | Switches to emergency power or records the incident and shuts down safely. |
| OP-20 | Authorise batch removal | Permits removal only after the chamber is safe and no protection response is active. |
