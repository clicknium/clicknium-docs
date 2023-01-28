---
sidebar_position: 3
sidebar_label: up
---

# clicknium.mouse.up

```python
def up(
        self,
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left
    ) -> None
```

Place the mouse at the desired location, and release the mouse button back up.

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

# release the mouse button up on position (100,100)
cc.mouse.up(100,100)

```