# click <!-- {docsify-ignore-all} -->
***def click(
        self,
        click_type: Literal["click", "up", "down"] = ClickType.Click,
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

Click an element by single click, up click or down click.  

**Parameters:**  
    &emsp;**click_type**: ClickType   
        &emsp;&emsp; click type for single click, up and down  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; mouse button is set to define the mouse button to click. Default value is left. It will click the left mouse button. 
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; click location is set to define the element position to click. Default value is center. It will click the element's central position. 
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; click method is set to choose which method to use when clicking the element. Default vaule is default. 
        &emsp;&emsp; `mouseemulation`: perform mouse emulator, move the mouse to the target element and click  
        &emsp;&emsp; `controlinvocation`: invoke the action on the target element, for web element, perform through javascript; for windows application element, it should support the action, or it will be failed. 
        &emsp;&emsp; `default`: for web element, use `controlinvocation`; for desktop element, use `mouseemulation`  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; modifier key is set to click with the modifier key("alt", "ctrl", "shift","win"). Default vaule is none.    
    &emsp;**xoffset**: int   
        &emsp;&emsp; x offset sets the click position based on click_location. When default value is 0, it means no offset.  
    &emsp;**yoffset**: int  
        &emsp;&emsp; y offset sets the click position based on click_location. Default value is 0. 
    &emsp;**xrate**: int  
        &emsp;&emsp; x rate percent of the click position is based on click_location. When default value is 0, it means no offset. If xrate is 1, it means X of click postion move to right. The distance is 1*element's width pixsels.  
    &emsp;**yrate**: int  
        &emsp;&emsp; y rate percent sets the click position based on click_location. When default value is 0, it means no offset. If xrate is 1, it means Y of click postion move to right. The distance is element's height pixsels.   
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit is second. Default set is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**

- click left button
***
```python
    from clicknium import clicknium as cc, locator, ui
    ui(locator.chrome.bing.svg).click(mouse_button = "left")
    # same as
    cc.find_element(locator.chrome.bing.svg).click(mouse_button = "left")
    
```

- click with offset  
![sample1](../../../img/click_sample1.png)

By clicknium recorder, record '5' button as
default if we invoke click on button '5', `ui(locator.applicationframe.button_num5butto).click()`, and it will click on the central position of button '5'.  
We can set the xrate to 1, it will move the point from default(button '5' central position) to right button '6' central position
`ui(locator.applicationframe.button_num5butto).click(xrate=1)`
We can set the yrate to 1, it will move the point from default(button '5' central position) to down button '2' central position
`ui(locator.applicationframe.button_num5butto).click(yrate=1)`  

- click modifier_key  
For windows file explorer as follows:  
![sample2-1](../../../img/click_sample21.png)  
if we invoke click on control 'test3 folder' as  
`ui(locator.explorer.edit_system_item).click()`
the select item will be 'test3 folder', and 'test1 folder' will be deselected.  
![sample2-2](../../../img/click_sample22.png)  
If we want to add 'test3 folder' in selection list, click as follows:
`ui(locator.explorer.edit_system_item).click(modifier_key=ModifierKey.Ctrl)`
![sample2-3](../../../img/click_sample23.png) 