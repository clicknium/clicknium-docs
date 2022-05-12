# highlight
***def highlight(
        self,
        duration: int = 3,
        color: Union[str, Color] = Color.Yellow,
        timeout: int = 30
    )***  

Get text of the element

**Parameters:** 
    &emsp;**duration**: int  
        &emsp;&emsp; The duration for highlighting the element. The unit of parameter is second. Default is set to 3 seconds.  
    &emsp;**color**: Union[str, Color]   
        &emsp;&emsp; The color of the highlighting rectangle, default is Yellow     
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    ui(locator.chrome.bing.search_sb_form_q).highlight()
```

- the following will be shown on browser  
![highlight](../../../img/highlight.png)