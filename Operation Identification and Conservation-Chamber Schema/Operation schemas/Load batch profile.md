| Field | Specification |
|---|---|
| Description | Loads the selected medicine batch identity and environmental limits. |
| Inputs | Batch ID, medicine type, permitted temperature range, permitted humidity range. |
| Outputs | Profile-load result and active batch profile. |
| Reads | Batch database, batch ID, chamber configuration. |
| Changes | Active batch profile and profile-validation status. |
| Sends/Alerts | Reports profile loaded or rejects invalid/missing profile. |
| Assumes (precondition) | A batch has been identified and the chamber is operational. |
| Result (postcondition) | A valid profile is stored and associated with the correct batch, or the load is rejected without activating conservation. |

