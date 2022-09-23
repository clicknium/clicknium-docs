---
sidebar_position: 9
sidebar_label: is_existing_by_xpath
---
# BrowserTab.is_existing_by_xpath
***def is_existing_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> bool***  

In current opened browser, check whether the ui element exist or not by the given XPath.

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the XPath of the element to find.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;Return True if UI element exists, otherwise return False

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# check element if exist by XPath
result = chrome_tab.is_existing_by_xpath("//*[@id=\"sb_form_q\"]")
print(result)

```