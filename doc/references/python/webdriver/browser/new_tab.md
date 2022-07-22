---
sidebar_position: 3
sidebar_label: new_tab
---
# browser.new_tab

***def new_tab(self, url: str, is_wait_complete: bool = True, timeout: int = 30) -> BrowserTab***  

Open a new tab in current browser.

**Parameters:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; url string, the target site url, eg.: <https://www.bing.com>.  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp; is_wait_complete, whether to wait for the tab to complete loading, the default value is True.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;[BrowserTab](./browsertab/browsertab.md) object, you can execute following operations in the browser tab: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
from clicknium import clicknium as cc

_tab = cc.chrome.open("https://www.bing.com/")

# get tab's browser
_browser = _tab.browser

# new tab
_browser.new_tab("https://www.bing.com/")

```