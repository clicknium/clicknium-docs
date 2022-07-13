---
sidebar_position: 2
sidebar_label: disable_telemetry
---
# disable_telemetry

***def disable_telemetry(self) -> None*** 

Disable 'usage data and errors' to be sent to ClickCorp online service.

**Parameters:**  
    &emsp;None

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# disable 'usage data and errors' to be sent to ClickCorp online service
cc.config.disable_telemetry()

```