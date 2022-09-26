---
sidebar_position: 6
sidebar_label: find_elements_by_xpath
---
# BrowserTab.find_elements_by_xpath
***def find_elements_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> List[WebElement]***  

In the active browser, find elements by the given XPath.

**Parameters:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; the XPath of the element to find.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;List of [WebElement](./webelement/webelement.md) objects.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by XPath
webelements = chrome_tab.find_elements_by_xpath("//*[@id=\"ilp_t\"]/div[1]/div/*")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```