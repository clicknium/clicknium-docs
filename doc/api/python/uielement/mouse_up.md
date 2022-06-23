# mouse_up <!-- {docsify-ignore-all} -->

***def mouse_up(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        click_location: ClickLocation = ClickLocation(),
        click_method: Union[Literal["default", "mouse-emulation", "control-invocation"], ClickMethod] = ClickMethod.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None***  

Mouse up on the target element.

**Parameters:**  
     &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; The available values are: 'left', 'right' and 'center', default is 'left'.  
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; [ClickLocation](./doc/api/python/uielement/clicklocation.md) is set to define the click of the element position.  
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; click method is set to choose which method to use when clicking the element. Default vaule is default.  
        &emsp;&emsp; `mouse-emulation`: perform mouse emulator, move the mouse to the target element and click  
        &emsp;&emsp; `control-invocation`: invoke operations on target elements, if it is a Web element, the action will be implemented by javascript. But actions may not be supported if it is a Windows element.  
        &emsp;&emsp; `default`: for Web element, use `control-invocation`; for Window element, use `mouse-emulation`  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; modifier key is set to click with the modifier key("alt", "ctrl", "shift", "win"). Default vaule is none.      
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    cc.find_element(locator.chrome.bing.svg).mouse_up(mouse_button = "left")
    ui(locator.chrome.bing.svg).mouse_up(mouse_button = "left")
```