# highlight
***def highlight(
        self,
        duration: int = 3,
        color: Union[str, Color] = Color.Yellow,
        timeout: int = 30
    ) -> None***  

Highlight the element with specified color.

**Parameters:**  
    &emsp;**duration**: int  
        &emsp;&emsp; the duration for highlighted the element. The unit of parameter is second. Default set is 3 seconds  
    &emsp;**color**: str | Color  
        &emsp;&emsp; the color of the highlighed rectangle. Default is Yellow.     
    &emsp;**timeout**: int  
        &emsp;&emsp;timeout for the operation. The unit of parameter is secon. Default set is 30 seconds.  

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