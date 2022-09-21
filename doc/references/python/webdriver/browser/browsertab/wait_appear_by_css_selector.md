---
sidebar_position: 13
sidebar_label: wait_appear_by_css_selector
---
# BrowserTab.wait_appear_by_css_selector
***def wait_appear_by_css_selector(
        self,
        locator: str,
        wait_timeout: int = 30
    ) -> WebElement***  

In current opened browser, wait for the element appear by the given css selector locator.

**Parameters:**  
    &emsp;**locator[Required]**: str     
        &emsp;&emsp; the css selector locator of the element to find. 
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object, or None if the element does not appear.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element appear by css selector
webelement = chrome_tab.wait_appear_by_css_selector("#sb_form_q")
if webelement:
    webelement.highlight()

```