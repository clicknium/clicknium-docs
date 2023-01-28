---
sidebar_position: 1
sidebar_label: click
---

# clicknium.mouse.click

```python
def click(
        self, 
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        delay: int = 0
    ) -> None
```  

Perform a single click with the specified mouse button.

**Parameters:**  
    &emsp;**x[Required]**: int  
        &emsp;&emsp; defines the X integer coordinate.  
    &emsp;**y[Required]**: int  
        &emsp;&emsp; defines the Y integer coordinate.  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; defines the position of the mouse button, and default is left button.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; the modifier key("alt", "ctrl", "shift", "win") to be pressed along with click, and default is none.   
    &emsp;**delay**: int  
        &emsp;&emsp; defines the time to wait between mouse down and mouse up, the unit is second, and default is set to 0 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# preform click on position (100,100)
cc.mouse.click(100,100)

```