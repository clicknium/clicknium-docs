# set_focus
***set_focus(self, timeout: int = 30)***  

set focus for the target element

**Parameters:**  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.   

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    ui(locator.chrome.bing.search_sb_form_q).set_focus()
```