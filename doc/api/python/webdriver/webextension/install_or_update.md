---
sidebar_position: 4
sidebar_label: install_or_update
---
# WebDriver.extension.install_or_update

***def install_or_update(self) -> bool*** 

Install or update browser extension based on current detected extension status.

**Returns:** bool  
    &emsp;Return `True` means the extension has been installed or updated, `False` means the extension has already installed the lastest version.

**Example:**
***
```python
from clicknium import clicknium as cc

# install or update chrome extension
cc.chrome.extension.install_or_update()

```