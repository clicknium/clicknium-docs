---
sidebar_position: 5
sidebar_label: close
---
# browser.close

***def close(self, is_force: bool = False) -> None***  

Close the browser.

**Parameters:**  
    &emsp;**is_force**: bool, force the browser to close.    

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# close the browser
chrome_tab.browser.close()

# open ie browser
ie_tab = cc.ie.open("https://www.bing.com")

# close the browser
ie_tab.browser.close(true)
```