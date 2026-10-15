| Change ID | Req. ID | Old Requirement | New Requirement | Reason |
|---|---|---|---|---|
| CR-01 | NFR-01 | The robot shall enter Safe Mode when a critical battery or thermal condition is detected. | The robot shall enter Safe Mode within 3 seconds when chamber or battery temperature exceeds the critical threshold or battery capacity falls below the emergency level. | Adds explicit trigger conditions and a measurable response deadline. |
| CR-02 | NFR-02 | The system shall support communication with multiple robots simultaneously. | The system shall support at least 20 simultaneously connected robots. | Defines the minimum concurrent-robot capacity for the pilot. |
| CR-03 | FR-10 | Only authenticated operators shall be permitted to issue robot commands. | The system shall require authenticated and role-authorised operators before accepting any robot command. | Requires both identity verification and permission checking. |
