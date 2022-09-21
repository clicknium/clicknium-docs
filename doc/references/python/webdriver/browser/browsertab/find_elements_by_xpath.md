---
sidebar_position: 6
sidebar_label: find_elements_by_xpath
---
# BrowserTab.find_elements_by_xpath
***def find_elements_by_xpath(
        self,
        locator: str,
        timeout: int = 30
    ) -> List[WebElement]***  

In current opened browser, find elements by the given xpath locator.

**Parameters:**  
    &emsp;**locator[Required]**: str     
        &emsp;&emsp; the xpath locator of the element to find. 
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;List of [WebElement](./webelement/webelement.md) objects.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by xpath
webelements = chrome_tab.find_elements_by_xpath("//*[@id=\"ilp_t\"]/div[1]/div/*")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```