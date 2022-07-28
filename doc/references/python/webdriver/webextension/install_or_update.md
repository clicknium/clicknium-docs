---
sidebar_position: 4
sidebar_label: install_or_update
---
# WebDriver.extension.install_or_update

***def install_or_update(self) -> bool*** 

Install or update browser extension based on the current status of the detected extension..

**Returns:** bool  
    &emsp;Return `True` means the extension is installed or updated. `False` means the latest version extension has already been installed before calling this function.

**Example:**
***
```python
from clicknium import clicknium as cc

# install or update chrome extension
cc.chrome.extension.install_or_update()

```