---
sidebar_position: 4
sidebar_label: find_element_by_xpath
---
# WebElement.find_element_by_xpath
***def find_element_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> WebElement***  

In the active browser, find element by the given XPath.  

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the XPath of the element to find.   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;[WebElement](./webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by XPath
element = chrome_tab.find_element_by_xpath("//*[@id=\"ilp_t\"]")

# find sub element by XPath
subelement = element.find_element_by_xpath(".//*[@id=\"ilp_t\"]/div[1]/div/*")
subelement.highlight()

```