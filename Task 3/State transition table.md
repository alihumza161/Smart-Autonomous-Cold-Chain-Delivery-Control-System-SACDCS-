| Transition ID | Current state + event | Next state | Req. ID | Valid? | Verification evidence |
| --- | --- | --- | --- | --- | --- |
| ST-TR-01 | `OFF + PowerOn` | `IDLE` after successful initialisation | FR-01 | Valid, with startup guard | TC-01 and startup test |
| ST-TR-02 | `IDLE + DeliveryRequest` with valid request | `NAVIGATING` | FR-01, FR-02 | Valid | TC-01 |
| ST-TR-03 | `IDLE + DeliveryRequest` with invalid request | `IDLE` | FR-01 | Valid | TC-02 |
| ST-TR-04 | `NAVIGATING + ObstacleDetected` | `AVOIDING_OBSTACLE` | FR-03 | Valid | TC-03 |
| ST-TR-05 | `AVOIDING_OBSTACLE + ObstacleCleared` and `RouteVerifiedSafe` | `NAVIGATING` | FR-04 | Valid | TC-04 |
| ST-TR-06 | `NAVIGATING + DestinationReached` and delivery guards pass | `DELIVERING` | FR-05 | Valid | TC-05 |
| ST-TR-07 | `DELIVERING + DeliveryCompleted` | `RETURNING` | FR-05 | Valid | Delivery completion and return test |
| ST-TR-08 | `RETURNING + WarehouseReached` | `IDLE` | FR-06 | Valid | Return-to-warehouse test |
| ST-TR-09 | `NAVIGATING + CriticalBattery` | `RETURNING` or `SAFE_MODE`, according to the emergency policy | FR-06, NFR-01 | Valid only if policy is explicit | TC-06 |
| ST-TR-10 | `NAVIGATING + CriticalThermal` | `SAFE_MODE` | NFR-01, SAF-02 | Valid | TC-06 |
| ST-TR-11 | `AVOIDING_OBSTACLE + CriticalBattery` | `RETURNING` if safe movement remains possible; otherwise `SAFE_MODE` | FR-06, SAF-02 | Valid only with safety guard | Fault-injection test |
| ST-TR-12 | `DELIVERING + CriticalBattery` | `SAFE_MODE` or a defined controlled-abort state | SAF-02 | Valid only if delivery stops safely | Fault-injection test |
| ST-TR-13 | Any active state + `CriticalFault` | `SAFE_MODE` | SAF-02 | Valid | TC-06 |
| ST-TR-14 | `NAVIGATING + LinkTimeout` | `LINK_LOST` | NFR-04 | Valid | TC-10 |
| ST-TR-15 | `LINK_LOST + LinkRestored` and session validation succeeds | Previous safe operational state or controlled recovery state | NFR-04 | Valid only after validation | TC-10 |
| ST-TR-16 | `SAFE_MODE + RecoveryAuthorised` | Appropriate recovered state, often `IDLE` | SAF-02 | Valid only after all safety guards pass | Recovery test |
| ST-TR-17 | `IDLE + DestinationReached` | `DELIVERING` | FR-05 | Invalid | Negative transition test |
| ST-TR-18 | `AVOIDING_OBSTACLE + DestinationReached` | `DELIVERING` | FR-04, FR-05 | Invalid | Negative transition test |
| ST-TR-19 | `SAFE_MODE + DeliveryRequest` | `NAVIGATING` | SAF-02 | Invalid without authorised recovery | Safety interlock test |
| ST-TR-20 | `LINK_LOST + StaleCommand` | Command execution | FR-10, NFR-04 | Invalid | TC-10 |
