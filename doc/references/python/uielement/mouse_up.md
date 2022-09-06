# mouse_up 

***def mouse_up(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        mouse_location: MouseLocation = MouseLocation(),
        by: Union[Literal["default", "mouse-emulation", "control-invocation"], MouseActionBy] = MouseActionBy.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None***  

Mouse button up on the target element.

**Parameters:**  
     &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; The available values are: 'left', 'right' and 'center', default is 'left'.  
    &emsp;**mouse_location**: MouseLocation  
        &emsp;&emsp; [MouseLocation](./mouselocation.md) is set to define the element position to release mouse button. Default position is center of element.  
    &emsp;**by**: MouseActionBy  
        &emsp;&emsp; Defines the method to perform releasing mouse button.  
        &emsp;&emsp; `mouse-emulation`: perform the action by simulating mouse.  
        &emsp;&emsp; `control-invocation`: perform the action by invoking its UI method. It may not be supported if it is a Windows desktop element.  
        &emsp;&emsp; `default`: automatically choose method per element type. For Web element, use `control-invocation`; for Window element, use `mouse-emulation`.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; The modifier key("alt", "ctrl", "shift", "win") to be pressed along with the action, and default is none.    
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.chrome.bing.svg).mouse_up(mouse_button = "left")
```