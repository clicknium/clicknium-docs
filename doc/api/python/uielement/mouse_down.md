# mouse_down <!-- {docsify-ignore-all} -->
***def mouse_down(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        click_location: ClickLocation = ClickLocation(),
        click_method: Union[Literal["default", "mouse-emulation", "control-invocation"], ClickMethod] = ClickMethod.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None***  

Mouse down on the target element.  

**Parameters:**  
     &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; The available values are: 'left', 'right' and 'center', default is 'left'.  
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; [ClickLocation](./doc/api/python/uielement/clicklocation.md) is set to define the element position to press down mouse button. Default position is center of element. 
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; Defines the method to perform pressing mouse button down.
        &emsp;&emsp; `mouse-emulation`: perform the action by simulating mouse.  
        &emsp;&emsp; `control-invocation`: perform the action by invoking its UI method. It may not be supported if it is a window desktop element.
        &emsp;&emsp; `default`: automatically choose method per element type. For Web element, use `control-invocation`; for Window element, use `mouse-emulation`.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; The modifier key("alt", "ctrl", "shift", "win") to be pressed along with the action, and default is none.        
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.chrome.bing.svg).mouse_down(mouse_button = "left")
```