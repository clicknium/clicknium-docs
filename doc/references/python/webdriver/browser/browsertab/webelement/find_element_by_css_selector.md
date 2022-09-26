---
sidebar_position: 5
sidebar_label: find_element_by_css_selector
---
# WebElement.find_element_by_css_selector
***def find_element_by_css_selector(
        self,
        css_selector: str,
        timeout: int = 30
    ) -> WebElement***  

In the active browser, find element by the given CSS selector.

**Parameters:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; The CSS selector to find the element.   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# find elements by CSS selector
element = chrome_tab.find_element_by_css_selector("#sb_form")

# find sub elements by CSS selector
webelement = element.find_element_by_css_selector("svg")
webelement.highlight()

```