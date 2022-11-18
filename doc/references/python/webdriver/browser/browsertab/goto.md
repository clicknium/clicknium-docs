---
sidebar_position: 19
sidebar_label: goto
---
# BrowserTab.goto

***def goto(
        self,
        url: str,
        is_wait_complete: bool = True,
        timeout: int = 30
    ) -> None***  

Redirect current tab to the specified url.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; Web site url, eg: <https://www.bing.com>.  
    &emsp;**is_wait_complete**: bool = True  
        &emsp;&emsp; is_wait_complete is set to define whether to wait for a browser tab to load completely. Default value is True.   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# naviage to another website
chrome_tab.goto("https://google.com")
```