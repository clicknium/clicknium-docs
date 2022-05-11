# get_size
***def get_size(self, timeout: int = 30) ***  

Get element's size(height and width)

**Parameters:**   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;ElementSize

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    from json
    
    size = ui(locator.chrome.bing.search_sb_form_q).get_size()
    print(json.dumps(size.__dict__))
```

- output: {"Width": 511, "Height": 45}