---
sidebar_position: 4
sidebar_label: down
---

# clicknium.mouse.down

***def down(
        self,
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left
    ) -> None***  

Place the mouse at the desired location, and press the mouse button down.

**Parameters:**  
    &emsp;**x[Required]**: int  
        &emsp;&emsp; defines the X integer coordinate.  
    &emsp;**y[Required]**: int  
        &emsp;&emsp; defines the Y integer coordinate.  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; defines the position of the mouse button, and default is left button.   

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# Press the mouse button down on position (100,100)
cc.mouse.down(100,100)

```