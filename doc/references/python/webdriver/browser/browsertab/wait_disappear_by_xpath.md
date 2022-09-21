---
sidebar_position: 15
sidebar_label: wait_disappear_by_xpath
---
# BrowserTab.wait_disappear_by_xpath
***def wait_disappear_by_xpath(
        self,
        locator: str,
        wait_timeout: int = 30
    ) -> bool***  

In current opened browser, check whether the ui element exist or not by the given xpath locator.

**Parameters:**  
    &emsp;**locator[Required]**: str     
        &emsp;&emsp; the xpath locator of the element to find. 
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;bool, return True if the element disappears within given timeout otherwise return False.  

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# wait element disappear by xpath
result = chrome_tab.wait_disappear_by_xpath("//*[@id=\"sb_form_q\"]", wait_timeout=5)
print(result)

```