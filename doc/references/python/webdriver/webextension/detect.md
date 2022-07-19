---
sidebar_position: 3
sidebar_label: detect
---
# WebDriver.extension.detect

***def detect(self) -> ExtensionStatus*** 

Detect browser extension installation status.

**Returns:**  
    &emsp;ExtensionStatus object, import the module with `from clicknium.common.enums import ExtensionStatus`, and the class definition as following: 
```python
class ExtensionStatus:
    NotInstalled = "NotInstalled"
    NeedUpdate = "NeedUpdate"
    Installed = "Installed" 
```

**Example:**
***
```python
from clicknium import clicknium as cc
from clicknium.common.enums import ExtensionStatus

# detect chrome extension
chrome_status = cc.chrome.extension.detect()
if chrome_status == ExtensionStatus.NeedUpdate:
    cc.chrome.extension.update()
```