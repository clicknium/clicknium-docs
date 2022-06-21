# highlight
***def highlight(
        self,
        color: Union[str, Color] = Color.Yellow,
        duration: int = 3,        
        timeout: int = 30
    ) -> None***  

Highlight the element with specified color.

**Parameters:**  
    &emsp;**color**: str | Color  
        &emsp;&emsp; the color of the highlighed rectangle, and the default value is Yellow.  
    &emsp;**duration**: int  
        &emsp;&emsp; the duration for highlighted the element, the unit is second, and the default value is 3 seconds         
    &emsp;**timeout**: int  
        &emsp;&emsp;timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    ui(locator.chrome.bing.search_sb_form_q).highlight()
```

- The following item will be shown on the browser  
![highlight](../../../img/highlight.png)