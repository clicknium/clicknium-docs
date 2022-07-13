---
sidebar_position: 9
sidebar_label: refresh
---
# BrowserTab.refresh

***def refresh(self) -> None -> None***  

Refresh current web page.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# refresh browser tab
chrome_tab.refresh()
```