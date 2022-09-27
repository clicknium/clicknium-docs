---
sidebar_position: 21
sidebar_label: close
---
# BrowserTab.close

***def close(self) -> None***  

Close the browser tab. The browser will be closed too if no opened tab.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# close the tab
chrome_tab.close()
```