---
sidebar_position: 15
sidebar_label: wait_disappear_by_xpath
---
# BrowserTab.wait_disappear_by_xpath
***def wait_disappear_by_xpath(
        self,
        xpath: str,
        wait_timeout: int = 30
    ) -> bool***  

In current opened browser, wait for the element disappear by the given XPath.

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the XPath of the element to find.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;bool, return True if the element disappears within given timeout otherwise return False.  

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# wait element disappear by XPath
result = chrome_tab.wait_disappear_by_xpath("//*[@id=\"sb_form_q\"]", wait_timeout=5)
print(result)

```