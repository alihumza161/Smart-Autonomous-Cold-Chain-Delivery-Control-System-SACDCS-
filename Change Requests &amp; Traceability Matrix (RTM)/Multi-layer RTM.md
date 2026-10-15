

| Requirement | State/Transition | Operation | Constraint | Test | Risk |
|---|---|---|---|---|---|
| FR-01 | ST-01: `IDLE → NAVIGATING` | OP-01 Validate delivery request | CON-01 | TC-01, TC-02 | High |
| FR-02 | ST-01: `IDLE → NAVIGATING` | OP-02 Plan and start route | CON-02 | TC-01 | High |
| FR-03 | ST-02: `NAVIGATING → AVOIDING_OBSTACLE` | OP-03 Detect and handle obstacle | CON-03 | TC-03 | Critical |
| FR-04 | ST-03: `AVOIDING_OBSTACLE → NAVIGATING` | OP-04 Verify route clearance | CON-03 | TC-04 | Critical |
| FR-05 | ST-04: `NAVIGATING → DELIVERING` | OP-05 Authorise batch release | CON-04, CON-05 | TC-05 | Critical |
| FR-06 | ST-05: `NAVIGATING → RETURNING` | OP-06 Evaluate battery and return | CON-06 | TC-06 | Critical |
| FR-07 | Chamber transition CH-01 | OP-07 Load batch profile | CON-07 | Chamber profile test | High |
| FR-08 | Chamber transition CH-02 | OP-08 Validate sensors and door | CON-08 | Chamber startup test | Critical |
| FR-09 | Chamber transition CH-03 | OP-09 Correct environment and verify recovery | CON-09 | TC-11 | Critical |
| FR-10 | Command processing transition CMD-01 | OP-10 Authenticate and authorise command | CON-10 | TC-07, TC-08 | Critical |
| NFR-01 | `* → SAFE_MODE` | OP-11 Execute emergency response | CON-11 | TC-06 | Critical |
| NFR-02 | Communication session establishment | OP-12 Manage robot sessions | CON-12 | TC-09 | High |
| SAF-01 | Crossing approach/entry guard | OP-13 Validate crossing permission | CON-13 | TC-12 | Critical |
| SAF-04 | Crossing interface fault transition | OP-14 Validate crossing sensor data | CON-14 | TC-14 | Critical |
| NFR-04 | Command acknowledgement/reporting | OP-15 Acknowledge and report command status | CON-15 | Delayed-link test | High |
| NFR-05 | Event persistence | OP-16 Record and recover event logs | CON-16 | Restart/log recovery test | High |

`* → SAFE_MODE` means that any applicable operational state may transition to Safe Mode when the corresponding critical trigger is detected.

The operation IDs are defined in Task 4. The state IDs are defined in Task 3, and the constraint IDs are formalised in Task 5.

completion. A timeout alone must not cause the same command to be executed again.
