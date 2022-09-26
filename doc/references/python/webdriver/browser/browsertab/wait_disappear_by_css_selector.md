---
sidebar_position: 16
sidebar_label: wait_disappear_by_css_selector
---
# BrowserTab.wait_disappear_by_css_selector
***def wait_disappear_by_css_selector(
        self,
        css_selector: str,
        wait_timeout: int = 30
    ) -> bool***  

In the active browser, wait for the element to disappear by the given CSS selector.

**Parameters:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; The CSS selector to find the element.  
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;bool, return True if the element disappears within given timeout otherwise return False.  

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element disappear by CSS selector
result = chrome_tab.wait_disappear_by_css_selector("#sb_form_q", wait_timeout=5)
print(result)

```