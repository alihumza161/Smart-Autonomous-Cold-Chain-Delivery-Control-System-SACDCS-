| Failure condition | Detection | Required response | Verification |
| --- | --- | --- | --- |
| Train detector failure | Self-diagnostic or inconsistent sensor readings | Treat crossing status as unknown; inhibit robot entry and alert the railway operator. | TC-14 |
| Barrier actuator failure | Commanded barrier position differs from measured position beyond the permitted response time. | Declare a crossing fault, prevent entry, and issue an alarm. | Barrier fault-injection test |
| Railway communication loss | Heartbeat timeout or invalid message sequence | Deny new crossing permission; robot remains outside the crossing. | TC-10, TC-14 |
| Stale railway data | Timestamp exceeds the configured freshness limit | Reject the data and require a fresh, validated crossing status. | Stale-message test |
| Contradictory train sensors | Independent train-detection channels disagree | Treat the crossing as unsafe until the discrepancy is resolved. | Sensor-disagreement test |
| Chamber temperature or humidity sensor failure | Self-test failure or invalid reading | Suspend normal conservation, activate the defined protection response, and alert the operator. | Chamber fault-injection test |
| Robot-to-control link loss | Communication watchdog expires | Apply the local safe-response policy and reject stale commands. | TC-10 |
