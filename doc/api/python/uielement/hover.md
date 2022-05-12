# hover
***hover(self, timeout: int = 30)***  

hover on the element, the mouse will move upon the element for a while

**Parameters:**    
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    ui(locator.chrome.bing.search_sb_form_q).hover()
```

# TODO
show case for hover, for example on the popup menu