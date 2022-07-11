# double_click
***def double_click(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        mouse_location: MouseLocation = MouseLocation(),
        by: Union[Literal["default", "mouse-emulation", "control-invocation"], MouseActionBy] = MouseActionBy.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None***  

Double click the target element.

**Parameters:**  
     &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; The available values are: 'left', 'right' and 'center', default is 'left'.  
    &emsp;**mouse_location**: MouseLocation  
        &emsp;&emsp; [MouseLocation](./mouselocation.md) is set to define the element position to click. Default position is center of element.  
    &emsp;**by**: MouseActionBy  
        &emsp;&emsp; Defines the method to click the UI element.  
        &emsp;&emsp; `mouse-emulation`: click the target UI element by simulating mouse.  
        &emsp;&emsp; `control-invocation`: click the target UI element by invoking its UI method. It may not be supported if it is a window desktop element.  
        &emsp;&emsp; `default`: automatically choose method per element type. For Web element, use `control-invocation`; for Window element, use `mouse-emulation`.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; The modifier key("alt", "ctrl", "shift", "win") to be pressed along with click, and default is none.    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

cc.find_element(locator.chrome.bing.svg).double_click(mouse_button = "left")
ui(locator.chrome.bing.svg).double_click(mouse_button = "left")
```