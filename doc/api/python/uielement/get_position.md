# get_position
***def get_position(self, timeout: int = 30) -> ElementPosition***  

Get element's position.

**Parameters:**   
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is second. Default set is 30 seconds  

**Returns:**  
    &emsp;ElementPosition class, the class definition as follows: 
```python
    class ElementPosition:

    def __init__(self, left, top, right, bottom):
        self.Left = left
        self.Top = top
        self.Right = right
        self.Bottom = bottom
```

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    from json
    
    position = ui(locator.chrome.bing.search_sb_form_q).get_position()
    print(position.__dict__)
```

- output: {"Left": 420, "Top": 294, "Right": 931, "Bottom": 339}