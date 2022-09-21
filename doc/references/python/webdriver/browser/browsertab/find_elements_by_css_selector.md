---
sidebar_position: 7
sidebar_label: find_elements_by_css_selector
---
# BrowserTab.find_elements_by_css_selector
***def find_elements_by_css_selector(
        self,
        locator: str,
        timeout: int = 30
    ) -> List[WebElement]***  

In current opened browser, find elements by the given css selector locator.

**Parameters:**  
    &emsp;**locator[Required]**: str     
        &emsp;&emsp; the css selector locator of the element to find.   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;List of [WebElement](./webelement/webelement.md) objects.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by css selector
webelements = chrome_tab.find_elements_by_css_selector("IMG")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```