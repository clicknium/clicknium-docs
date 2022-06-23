# hover
***def hover(self, timeout: int = 30) -> None***  

Hover over the element, and the mouse will move upon the element for a while.

**Parameters:**    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**

- hover on the web element  
  
![sample](../../../img/hover_sample1.png)  

```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.li_dots_overflow).hover()
```
![sample](../../../img/hover_sample2.png) 