---
sidebar_position: 5
sidebar_label: move
---

# clicknium.mouse.move

```python
def move(
        self,
        x: int, 
        y: int
    ) -> None
```  

Move the mouse cursor to the X and Y integer coordinates.

**Parameters:**  
    &emsp;**x[Required]**: int  
        &emsp;&emsp; defines the X integer coordinate.  
    &emsp;**y[Required]**: int  
        &emsp;&emsp; defines the Y integer coordinate.    

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# Move the mouse to position (100,100)
cc.mouse.move(100,100)

```