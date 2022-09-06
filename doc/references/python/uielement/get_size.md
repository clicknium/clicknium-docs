# get_size
***def get_size(self, timeout: int = 30) -> ElementSize***  

Get the size(height and width) of the target element.

**Parameters:**   
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;ElementSize object, the class definition as following: 
```python
    class ElementSize:

    def __init__(self, width, height) -> None:
        self.Width = width
        self.Height = height
```

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui
from json
    
size = ui(locator.chrome.bing.search_sb_form_q).get_size()
print(json.dumps(size.__dict__))

# output: {"Width": 511, "Height": 45}

```