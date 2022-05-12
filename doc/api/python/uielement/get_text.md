# get_text
***get_text(self, timeout: int = 30)***  

Get text of the element

**Parameters:**    
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;str

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    text = ui(locator.chrome.bing.search_sb_form_q).get_text()
```

# TODO
show examples, for different applicaiton.control. the return value, to explain the usage