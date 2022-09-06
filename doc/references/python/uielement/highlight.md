# highlight
***def highlight(
        self,
        color: Union[str, Color] = Color.Yellow,
        duration: int = 3,        
        timeout: int = 30
    ) -> None***  

Highlight the target element.

**Parameters:**  
    &emsp;**color**: str | Color  
        &emsp;&emsp; The color of the highlighed rectangle, the default value is Yellow.  
    &emsp;**duration**: int  
        &emsp;&emsp; The duration for highlighting the element, the unit is second, and the default value is 3 seconds.  
    &emsp;**timeout**: int  
        &emsp;&emsp;Timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
- Highlight target web element  
```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.search_sb_form_q).highlight()
```

The following item will be shown on the browser:  
![highlight](../../../img/highlight.png)