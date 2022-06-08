# double_click<!-- {docsify-ignore-all} -->
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
        &emsp;&emsp; Mouse button is set to define the click of the mouse button. Default value is left, and it will click mouse left button. 
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; Click location is set to define the click of the element position. Default value is center, and it will click the element's center position.  
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; Click method is set to choose which method to use when clicking the element. Default vaule is default.  
        &emsp;&emsp; `mouseemulation`: perform mouse emulator, move mouse to the target element and click   
        &emsp;&emsp; `controlinvocation`: invoke the action on the target element, for web element, perform through javascript; for desktop element, it should support the action, or it will be failed  
        &emsp;&emsp; `default`: for web element, use `controlinvocation`; for desktop element, use `mouseemulation`  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; modifier key is set to click the modifier key("alt", "ctrl", "shift","win"). Default vaule is none.    
    &emsp;**xoffset**: int   
        &emsp;&emsp; x offset sets the click position based on click_location. When default value is 0, it means no offset.  
    &emsp;**yoffset**: int  
        &emsp;&emsp; y offset sets the click position based on click_location. Default value is 0.  
    &emsp;**xrate**: int  
        &emsp;&emsp; x rate percent of the click position is based on click_location. When default value is 0, it means no offset. If xrate is 1, it means X of click postion move to right, and the distance is 1*element's width pixsels. 
    &emsp;**yrate**: int  
        &emsp;&emsp; y rate percent sets the click position based on click_location. When default value is 0, it means no offset. If xrate is 1, it means Y of click postion move to right, and the distance is element's height pixsels.   
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit is second. Default set is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    cc.find_element(locator.chrome.bing.svg).double_click(mouse_button = "left")
    ui(locator.chrome.bing.svg).double_click(mouse_button = "left")
```