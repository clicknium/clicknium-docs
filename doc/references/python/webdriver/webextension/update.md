---
sidebar_position: 2
sidebar_label: update
---
# WebDriver.extension.update

```python
def update(self) -> None
``` 

Update browser extension.

**Example:**
***
```python
from clicknium import clicknium as cc

# update chrome extension
cc.chrome.extension.update()

# update edge extension
cc.edge.extension.update()

# update firefox extension
cc.firefox.extension.update()
```