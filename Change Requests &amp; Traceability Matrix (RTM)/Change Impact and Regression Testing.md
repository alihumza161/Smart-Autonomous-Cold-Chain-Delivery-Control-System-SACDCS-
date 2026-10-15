## 2.5 Change Impact and Regression Testing

| Change Request | Mandatory Re-test Cases | Additional Verification |
|:---|:---|:---|
| CR-01 | TC-06, TC-10, TC-11, TC-13, TC-14 | Verify the 3-second deadline, trigger coverage, safe-state transitions, and timing under communication-link or sensor faults. |
| CR-02 | TC-09, TC-01, TC-07, TC-08 | Verify session isolation, command routing, telemetry association, logging, and rejection behaviour under a 20-robot load. |
| CR-03 | TC-07, TC-08, TC-01, TC-05 | Verify authentication, role-based permissions, delivery authorisation, command rejection, and audit logs. |

Regression tests should include the full command lifecycle:

1. Command received.
2. Operator authenticated.
3. Role permission validated.
4. Command accepted or rejected.
5. Accepted command executed exactly once.
6. Resulting robot state and telemetry reported.
7. Command outcome recorded in persistent logs.

Because the communication link has a delay of several seconds, the implementation must distinguish command receipt, command acceptance, execution, and final completion. A timeout alone must not cause the same command to be executed again.
