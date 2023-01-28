---
sidebar_position: 4
sidebar_label: maximize
---
# browser.maximize

```python
def maximize(self) -> None
```  

Maximize the browser window.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# get browser with type chrome
browser = cc.chrome.browsers[0]

# maximize the browser window
browser.maximize()
```