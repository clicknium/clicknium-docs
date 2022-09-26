---
sidebar_position: 8
sidebar_label: find_elements_by_css_selector
---
# WebElement.find_elements_by_css_selector
***def find_elements_by_css_selector(
        self,
        css_selector: str,
        timeout: int = 30
    ) -> List[WebElement]***  

In the active browser, find elements by the given CSS selector.

**Parameters:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; The CSS selector to find the element.   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;List of [WebElement](./webelement.md) objects.

**Example:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by CSS selector
element = chrome_tab.find_element_by_css_selector("#ilp_t")

# find sub elements by CSS selector
webelements = element.find_elements_by_css_selector("IMG")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```