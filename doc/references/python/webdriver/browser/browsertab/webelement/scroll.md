---
sidebar_position: 5
sidebar_label: scroll
---
# WebElement.scroll

***def scroll(
        self,
        delta_x: int = 0,
        delta_y: int = 0,
        timeout: int = 30
    ) -> None***  

Scroll the target element with the scroll bar.

**Parameters:**  
    &emsp;**delta_x**: int   
        &emsp;&emsp; Pixels to scroll horizontally.  
    &emsp;**delta_y**: int   
        &emsp;&emsp; Pixels to scroll vertically.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.clicknium.com")

# scroll the element
web_element = chrome_tab.find_element(locator.chrome.clicknium.products_panel)
web_element.scroll(0, 500)
```