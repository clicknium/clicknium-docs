# get_position
***def get_position(self, timeout: int = 30) ***  

Get element's bounding rectangle  

**Parameters:**   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;ElementPosition

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    from json
    
    position = ui(locator.chrome.bing.search_sb_form_q).get_position()
    print(position.__dict__)
```

- output: {"Left": 420, "Top": 294, "Right": 931, "Bottom": 339}