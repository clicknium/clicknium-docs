---
sidebar_position: 4
sidebar_label: find_element_by_css_selector
---
# BrowserTab.find_element_by_css_selector
***def find_element_by_css_selector(
        self,
        css_selector: str
    ) -> WebElement***  

In current opened browser, find element by the given CSS selector.

**Parameters:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; the CSS selector of the element to find.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# find element by CSS selector
webelement = chrome_tab.find_element_by_css_selector("#sb_form_q")
webelement.highlight()

```