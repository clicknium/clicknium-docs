---
sidebar_position: 10
sidebar_label: is_existing_by_css_selector
---
# BrowserTab.is_existing_by_css_selector
***def is_existing_by_css_selector(
        self,
        locator: str,
        timeout: int = 30
    ) -> bool***  

In current opened browser, find elements by the given css selector locator.

**Parameters:**  
    &emsp;**locator[Required]**: str     
        &emsp;&emsp; the css selector locator of the element to find. 
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;Return True if UI element exists, otherwise return False

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# check element if exist by css selector
result = chrome_tab.is_existing_by_css_selector("#sb_form_q")
print(result)

```