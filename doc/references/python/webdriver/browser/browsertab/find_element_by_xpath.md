---
sidebar_position: 3
sidebar_label: find_element_by_xpath
---
# BrowserTab.find_element_by_xpath
***def find_element_by_xpath(
        self,
        xpath: str
    ) -> WebElement***  

In the active browser, find element by the given XPath.  

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the XPath of the element to find.   

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# find element by XPath
webelement = chrome_tab.find_element_by_xpath("//*[@id=\"sb_form_q\"]")
webelement.highlight()

```