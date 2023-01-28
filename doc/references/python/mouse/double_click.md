---
sidebar_position: 2
sidebar_label: double_click
---

# clicknium.mouse.double_click

``` python 
def double_click(
        self, 
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey
    ) -> None
```  

Perform a double click with the specified mouse button.

**Parameters:**  
    &emsp;**x[Required]**: int  
        &emsp;&emsp; defines the X integer coordinate.  
    &emsp;**y[Required]**: int  
        &emsp;&emsp; defines the Y integer coordinate.  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; defines the position of the mouse button, and default is left button.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; the modifier key("alt", "ctrl", "shift", "win") to be pressed along with click, and default is none.   

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# preform double click on position (100,100)
cc.mouse.double_click(100,100)

```