---
sidebar_position: 3
sidebar_label: find_element_by_xpath
---
# BrowserTab.find_element_by_xpath
***def find_element_by_xpath(
        self,
        xpath: str
    ) -> WebElement***  

In current opened browser, find element by the given xpath.  

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the xpath of the element to find.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# find element by xpath
webelement = chrome_tab.find_element_by_xpath("//*[@id=\"sb_form_q\"]")
webelement.highlight()

```