| Event ID | Event/condition | Meaning |
| --- | --- | --- |
| EV-01 | `PowerOn` | Robot power is enabled. |
| EV-02 | `InitialisationPassed` | Required startup checks succeed. |
| EV-03 | `DeliveryRequest` | Mission Control submits a delivery request. |
| EV-04 | `RequestValidated` | Destination, batch, permissions, and request format are valid. |
| EV-05 | `ObstacleDetected` | A relevant obstacle is detected in the planned path. |
| EV-06 | `ObstacleCleared` | The obstacle is no longer blocking the path. |
| EV-07 | `RouteVerifiedSafe` | The route is confirmed safe to resume. |
| EV-08 | `DestinationReached` | The assigned destination is reached. |
| EV-09 | `DeliveryCompleted` | The authorised delivery action completes. |
| EV-10 | `WarehouseReached` | The robot reaches its return point. |
| EV-11 | `CriticalBattery` | Battery capacity falls below the configured emergency level. |
| EV-12 | `CriticalThermal` | A monitored battery or chamber temperature crosses its critical threshold. |
| EV-13 | `CriticalFault` | A critical system fault is detected. |
| EV-14 | `LinkTimeout` | The remote link exceeds the allowed communication timeout. |
| EV-15 | `LinkRestored` | Communication is restored and passes validation. |
| EV-16 | `RecoveryAuthorised` | An authorised recovery procedure confirms that operation may resume. |
