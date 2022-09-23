---
sidebar_position: 13
sidebar_label: wait_appear_by_css_selector
---
# BrowserTab.wait_appear_by_css_selector
***def wait_appear_by_css_selector(
        self,
        css_selector: str,
        wait_timeout: int = 30
    ) -> WebElement***  

In current opened browser, wait for the element appear by the given css selector.

**Parameters:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; the css selector of the element to find.  
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object, or None if the element does not appear.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element appear by css selector
webelement = chrome_tab.wait_appear_by_css_selector("#sb_form_q")
if webelement:
    webelement.highlight()

```