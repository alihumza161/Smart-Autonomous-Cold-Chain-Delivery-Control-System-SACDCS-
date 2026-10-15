Let the following Boolean variables represent the observed system conditions:
- Train_Present: a train occupies the crossing.
- Train_Approaching: train detection indicates an approaching train.
- Barrier_Open, Barrier_Closed: barrier position indicators.
- Crossing_Clear: crossing occupancy has been confirmed clear.
- Robot_Enter: robot is entering the crossing.
- Rail_Sensors_Healthy: required railway sensors are healthy.
- Rail_Comms_OK: communication with the railway control system is valid.
- Destination_Reached: assigned destination has been reached.
- Door_Closed: chamber door is confirmed closed.
- Sensors_Healthy: essential chamber sensors are healthy.
- Conservation_Active: active conservation is enabled.
- Protection_Active: chamber protection response is active.
- Temp_In_Range, Humidity_In_Range: measured values satisfy the batch profile.
- Critical_Condition: critical battery or thermal condition is detected.
- Safe_Mode: robot Safe Mode is active.
- Operator_Authenticated, Role_Authorised: operator identity and permissions are valid.
- Command_Executed: the command has been executed.
The implication \(P \rightarrow Q\) means that if \(P\) is true, \(Q\) must also be true. The conjunction \(P \land Q\) requires both conditions to be true. The negation \(\neg P\) means \(P\) must be false.

| Constraint ID | Formal expression | Interpretation |
| --- | --- | --- |
| CON-01 | \\(\text{Robot\\\_Enter} \rightarrow (\text{Barrier\\\_Open} \land \neg\text{Train\\\_Approaching} \land \text{Crossing\\\_Clear})\\) | Entry requires all three safety conditions. |
| CON-02 | \\((\text{Train\\\_Present} \lor \text{Train\\\_Approaching}) \rightarrow \neg\text{Barrier\\\_Open}\\) | A train present or approaching prohibits an open barrier. |
| CON-03 | \\(\text{Train\\\_Present} \rightarrow \text{Barrier\\\_Closed}\\) | The barrier remains closed while a train occupies the crossing. |
| CON-04 | \\(\text{Barrier\\\_Open} \rightarrow (\text{Crossing\\\_Clear} \land \text{Rail\\\_Sensors\\\_Healthy})\\) | Opening requires confirmed clearance and healthy sensors. |
| CON-05 | \\(\text{Delivering} \rightarrow (\text{Destination\\\_Reached} \land \text{Delivery\\\_Authorised})\\) | Delivery requires the correct location and authorisation. |
| CON-08 | \\(\text{Conservation\\\_Active} \rightarrow (\text{Door\\\_Closed} \land \text{Sensors\\\_Healthy})\\) | Conservation requires a closed door and healthy sensors. |
| CON-09 | \\(\text{Recovery\\\_Declared} \rightarrow (\text{Temp\\\_In\\\_Range} \land \text{Humidity\\\_In\\\_Range})\\) | Recovery requires measured environmental compliance. |
| CON-10 | \\(\text{Delivering} \rightarrow (\text{Door\\\_Closed} \land \neg\text{Protection\\\_Active})\\) | Delivery cannot proceed with the door open or protection active. |
| CON-11 | \\(\text{Critical\\\_Condition} \rightarrow \mathbf{F}\_{\leq 3s}\text{Safe\\\_Mode}\\) | Safe Mode must be entered within 3 seconds of detection. |
| CON-13 | \\(\text{Robot\\\_Enter} \rightarrow (\text{Rail\\\_Sensors\\\_Healthy} \land \text{Rail\\\_Comms\\\_OK})\\) | Entry requires valid railway sensor and communication status. |
| CON-14 | \\(\neg\text{Rail\\\_Comms\\\_OK} \rightarrow \neg\text{Robot\\\_Enter}\\) | Communication loss prevents crossing entry. |
| CON-15 | \\(\text{Command\\\_Executed} \rightarrow (\text{Operator\\\_Authenticated} \land \text{Role\\\_Authorised})\\) | Executed commands require both authentication and authorisation. |
