| State ID | State name | Meaning | Entry condition | Exit condition |
| --- | --- | --- | --- | --- |
| ST-00 | `OFF` | Robot is switched off or not operational. | Power is off. | Power-on and initialisation succeed. |
| ST-01 | `IDLE` | Robot is operational and waiting for a delivery request. | Startup succeeds or robot returns to the warehouse. | A valid delivery request is accepted. |
| ST-02 | `NAVIGATING` | Robot follows its planned route. | Valid delivery request or obstacle clearance. | Destination reached, obstacle detected, critical battery, link lost, or critical fault. |
| ST-03 | `AVOIDING_OBSTACLE` | Robot suspends normal route navigation and handles an obstacle. | Obstacle detected during navigation. | Obstacle cleared and route verified, or a safety trigger occurs. |
| ST-04 | `DELIVERING` | Robot performs the authorised delivery at the destination. | Destination reached and all delivery guards pass. | Delivery completed or a safety trigger occurs. |
| ST-05 | `RETURNING` | Robot travels toward the warehouse without continuing the abandoned delivery. | Delivery completed or delivery abandoned due to critical battery. | Warehouse reached, or a safety trigger occurs. |
| ST-06 | `SAFE_MODE` | Robot inhibits hazardous operations and executes the configured emergency response. | Critical thermal, battery, or fault trigger. | Fault is cleared, conditions are verified safe, and authorised recovery is permitted. |
| ST-07 | `LINK_LOST` | Remote communication is unavailable or exceeds the defined timeout. | Communication heartbeat or link supervision fails. | Communication is restored and validated, or a critical safety trigger occurs. |
