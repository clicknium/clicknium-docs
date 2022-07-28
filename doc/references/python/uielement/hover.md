# hover
***def hover(self, timeout: int = 30) -> None***  

Hover over the element, and the mouse will move upon the element and stay for a while.

**Parameters:**    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
- Hover over a web element  
  
![sample](../../../img/hover_sample1.png)  

```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.li_dots_overflow).hover()
# the menu is displayed after hovering over the button
```
  
![sample](../../../img/hover_sample2.png) 