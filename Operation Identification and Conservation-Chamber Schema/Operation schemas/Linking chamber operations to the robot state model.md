| Event/operation | Chamber effect | Robot-state effect | Required behaviour |
|---|---|---|---|
| OP-18: Door opens during conservation | Conservation is suspended. | Prevent entry into `DELIVERING`, or suspend an ongoing delivery action. | Hold the delivery until the chamber is verified safe. |
| OP-09: Correction fails | Chamber enters protection mode. | Block `DELIVERING`; enter the configured safe response if the fault is critical. | Do not release medicine while protection is active. |
| OP-19: Main power fails | Switch to backup power or shut down safely. | May trigger `SAFE_MODE`. | Prevent unsafe delivery and report the incident when possible. |
| OP-08: Essential sensor fails | Conservation eligibility becomes false. | Prevent delivery or trigger the defined safety response. | Do not treat missing sensor data as proof of safety. |
