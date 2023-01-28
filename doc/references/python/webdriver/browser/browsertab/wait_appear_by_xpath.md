---
sidebar_position: 12
sidebar_label: wait_appear_by_xpath
---
# BrowserTab.wait_appear_by_xpath
```python
def wait_appear_by_xpath(
        self,
        xpath: str,
        wait_timeout: int = 30
    ) -> WebElement
```  

In the active browser, wait for the element to appear by the given XPath.

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the XPath of the element to find.  
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object, or None if the element does not appear.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element appear by XPath
webelement = chrome_tab.wait_appear_by_xpath("//*[@id=\"sb_form_q\"]")
if webelement:
    webelement.highlight()

```