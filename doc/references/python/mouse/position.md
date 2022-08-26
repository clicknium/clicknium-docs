---
sidebar_position: 7
sidebar_label: position
---

# clicknium.mouse.position

***def position(
        self
    ) -> Tuple[int,int]***  

Get the position of the mouse cursor.

**Parameters:**  
    &emsp;None   

**Returns:**  
    &emsp;The current X and Y coordinates of the mouse cursor.

**Example:**
***
```python
from clicknium import clicknium as cc

# get the position of the mouse cursor
x,y = cc.mouse.position()
print("X integer coordinate is " + x)
print("Y integer coordinate is " + y)
```