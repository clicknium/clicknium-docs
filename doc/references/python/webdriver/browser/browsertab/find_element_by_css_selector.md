---
sidebar_position: 4
sidebar_label: find_element_by_css_selector
---
# BrowserTab.find_element_by_css_selector
***def find_element_by_css_selector(
        self,
        locator: str
    ) -> WebElement***  

In current opened browser, find element by the given css selector locator.

**Parameters:**  
    &emsp;**locator[Required]**: str     
        &emsp;&emsp; the css selector locator of the element to find.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# find element by css selector
webelement = chrome_tab.find_element_by_css_selector("#sb_form_q")
webelement.highlight()

```