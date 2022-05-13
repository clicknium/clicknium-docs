# double_click
***def double_click(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        click_location: Literal["center", "lefttop", "leftbottom", "righttop","rightbuttom"] = ClickLocation.Center,
        click_method: Union[Literal["default", "mouseemulation", "controlinvocation"], ClickMethod] = ClickMethod.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        xoffset: int = 0,
        yoffset: int = 0,
        xrate: int = 0,
        yrate: int = 0,
        timeout: int = 30
    ) -> None***  

Click an element with double click.  

**Parameters:**  
     &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; mouse button is set to define the mouse button to click. Default value is left, it will click with mouse left button  
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; click location is set to define the element position to click. Default value is center, it will click the element's center position  
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; click method is set to which method to use when clicking the element. Default vaule is default  
        &emsp;&emsp; `mouseemulation`: perform mouse emulator, will move mouse to the target element and click   
        &emsp;&emsp; `controlinvocation`: invoke the action on the target element, for web element, perform through javascript; for desktop element, it should support the action, or will be failed  
        &emsp;&emsp; `default`: for web element, will use `controlinvocation`; for desktop element, will use `mouseemulation`  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; modifier key is set to click with the modifier key("alt", "ctrl", "shift","win"). Default vaule is none    
    &emsp;**xoffset**: int 
        &emsp;&emsp; x offset is set the click position based on element's center position. Default value is 0   
    &emsp;**yoffset**: int  
        &emsp;&emsp; y offset is set the click position based on element's center position. Default value is 0  
    &emsp;**xrate**: int  
        &emsp;&emsp; x rate percent is set the click position based on element's center position. Default value is 0  
    &emsp;**yrate**: int  
        &emsp;&emsp; x rate percent is set the click position based on element's center position. Default value is 0    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    cc.find_element(locator.chrome.bing.svg).double_click(mouse_button = "left")
    ui(locator.chrome.bing.svg).double_click(mouse_button = "left")
```